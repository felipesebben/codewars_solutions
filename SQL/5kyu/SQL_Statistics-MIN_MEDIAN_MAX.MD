<h1><strong>SQL Statistics: MIN, MEDIAN, MAX</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>For this challenge you need to create a simple SELECT statement. Your task is to calculate the MIN, MEDIAN and MAX scores of the students from the results table.</p>

<h2><strong>Tables and relationship below:</strong></h2>
<img src= "http://i.imgur.com/Qdt9DqU.png", alt="Table Scheme">

<h2><strong>Output:</strong></h2>
<p>Resultant table:
    <ul>
        <li>min</li>
        <li>median</li>
        <li>max</li>
    </ul>
</p>

<h2><strong>Solution #1:</strong></h2>

``` SQL
SELECT 
  MIN(score) AS min,
  PERCENTILE_CONT(0.5) WITHIN GROUP(ORDER BY score) AS median,
  MAX(score) AS max
FROM result;
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
    <li> Get the MIN and MAX values using the <code>MIN</code> and <code>MAX</code> functions.</li>
    <li> Calculate the median value, as there is no native function for that.</li>
        <ul>
            <li> Use <code>PERCENTILE_CONT()</code> to define the required percentile to be calculated.</li>
            <li>Use <code>WITHIN GROUP</code> to tell PostgreSQL to calculate the percentile within the given group of values (in this case, <code>score</code>).</li>
            <li>Finally, apply <code>ORDER BY</code> to sort the values before calculating the median.</li>
    </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>I learned how to calculate median values in SQL. That was new to me. Also, I also learned how <em>not to</em> join tables at the first place; in this case, it was totally unnecessary to so.</p>
<hr>
<a href='https://www.codewars.com/kata/58167fa1f544130dcf000317'>See on CodeWars.com</a>