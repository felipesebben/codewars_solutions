<h1><strong>First and last IP in a network</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p> Given a table where users' connections are logged, find the first and the last address of the networks they connected from.</p>

<h2><strong>Notes:</strong></h2>
<p>
    <ul>
        <li>Order the result by the id column</li>
        <li>There's no need to validate anything - it's okay if the user connects from a private network</li>
        <li>(You don't need the connection_time field for this task but without it the input data looks too dull)</li>
        <li>You can read more about IPv4 on <a href='https://en.wikipedia.org/wiki/Internet_Protocol_version_4'>Wikipedia</a> (check the <a href='https://en.wikipedia.org/wiki/Internet_Protocol_version_4#First_and_last_subnet_addresses'>First and last</a> subnet addresses section if you need an example/explanation related to this task only)</li>
        
<h2><strong>Input table:</strong></h2>

<pre>
    <code>
---------------------------------------------
|    Table    |     Column      |   Type    |
|-------------+-----------------+-----------|
| connections | id              | int       |
|             | connection_time | timestamp |
|             | ip_address      | inet      |
---------------------------------------------
    </code>
</pre>

<h2><strong>Output table:</strong></h2>

<pre>
    <code>
------------------------
|    Column     | Type |
|---------------+------|
| id            | int  |
| first_address | text |
| last_address  | text |
------------------------
    </code>
</pre>

<h2><strong>Example:</strong></h2>
<p>For the IP address <code>182.240.42.115/24</code> the first address in the network is <code>182.240.42.0/24,</code> and the last one is <code>182.240.42.255/24</code>.</p>

<h2><strong>Solution:</strong></h2>

``` SQL
SELECT 
  id, 
  NETWORK(ip_address) AS first_address,
  BROADCAST(ip_address) AS last_address  
FROM connections
ORDER BY id ASC;
```

<h3><b>How did I do it?</b></h3>
<p> That was a tough cookie. Basically, you had to realize that the dtype for <code>ip_address</code> was a <code>inet</code>, which holds an Ipv4 or IPv6 network specification. It was clear, then, that we were not dealing with your normal data type. It was fundamental to look for the dtype-related functions. Once you got that, it became easy. I had to:
    <ol>
        <li> Use <code>NETWORK()</code> to extract the network part of the ip address.</li>
        <li> Apply the <code>BROADCAST()</code> function to obtain the broadcast address for the network
    </ol>
</p>
<p>Basically, you had to do some reading. If you followed the instructions (and did not rush into coding, like I always do), you'll see that you needed to understand the <em>meaning</em> of each ip address, and not its actual order.</p>

<h3><strong>What did I learn?</strong></h3>
<p>Well, I learned how to use some very unusual functions. But who knows, right? More importantly, I learned that, in every situation, the fundamental rule always stands: <strong>READ THE INSTRUCTIONS CAREFULLY!</strong>. It will save you tons of time!</p>
<hr>
<a href='https://www.codewars.com/kata/5db5ff03d10bfa001da9cf2e/train/sql'>See on CodeWars.com</a>