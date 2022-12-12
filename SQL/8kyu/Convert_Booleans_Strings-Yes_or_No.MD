<h1><strong>Even or Odd</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>Complete the method that takes a boolean value and return a <code>"Yes"</code> string for <code>true</code>, or a <code>"No"</code> string for <code>false</code>.

You are given a table <code>booltoword</code> with column <code>bool</code>, return a table with column <code>bool</code> and your result in a column named <code>res</code>.
</p>

<h2><strong>Solution:</strong></h2>

``` SQL
SELECT bool,
CASE 
    WHEN bool = true THEN 'Yes'
    WHEN bool = false THEN 'No'
    END 
AS res FROM booltoword;
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
        <li> Use <code>CASE()</code> to make a conditional statement.</li>
        <li>If the observation is <code>true</code>, convert it into <code>'Yes'</code>. Do the same with a <code>false</code> value</li>
            </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>It was a good way of applying a CASE statement to a boolean and converting it into a string.</p>
<hr>
<a href='https://www.codewars.com/kata/53369039d7ab3ac506000467/train/sql'>See on CodeWars.com</a>