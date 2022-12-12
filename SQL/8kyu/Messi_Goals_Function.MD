<h1><strong>Grasshopper - Messi goals function</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>Messi is a soccer player with goals in three leagues:</p>
<ul>
    <li>LaLiga</li>
    <li>Copa del Rey</li>
    <li>Champions</li>
</ul>

<p> You will be given a table, <code>goals</code>, with columns <code>la_liga_goals</code>, <code>copa_del_rey_goals</code>, and <code>champions_league_goals</code>. Return a table with a column, <code>res</code>.</p>

<p>Complete the function to return his total number of goals in all three leagues.

Note: the input will always be valid.</p>



<h3><p><strong>Example</strong></p></h3>
<pre>
    <code>
5, 10, 2  -->  17
    </code>
</pre>

<h2><strong>Solution:</strong></h2>

``` SQL
SELECT la_liga_goals + copa_del_rey_goals + champions_league_goals AS res
FROM goals
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
        <li> Just use the <code>+</code> operator to concatenate every column. No need to do anything else, as we are concatenating strings.</li>
    </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>It was a nice way of learning how to easily concatenate strings, although, in real life, you'd probabily have to use other functions, as your data won't be formatted as this challenge.</p>
<hr>
<a href='https://www.codewars.com/kata/55f73be6e12baaa5900000d4/train/sql'>See on CodeWars.com</a>