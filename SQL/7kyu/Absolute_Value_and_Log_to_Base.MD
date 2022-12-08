<h1><strong>Easy SQL: Absolute Value and Log to Base</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>Given the following table 'decimals':</p>

<p><strong>decimals table schema</strong></p>
<ul>
    <li>id</li>
    <li>number1</li>
    <li>number2</li>
</ul>

<p> Return a table with two columns (<code>abs</code>, <code>log</code>) where the values in abs are the absolute values of <code>number1</code> and the values in log are values from <code>number2</code> in logarithm to base 64.</p>

<h2><strong>Solution:</strong></h2>

``` SQL
SELECT ABS(number1) AS abs, LOG(64, number2) AS log
FROM decimals;
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
        <li> Use the <code>ABS()</code> to obtain the absolute value of <code>number1</code>.</li>
        <li> Apply the <code>LOG()</code> function to obtain the logarithm of <code>number2</code>. Here, the function take two arguments:</p></li>
        <ul>
            <li>The first argument (64) is the <strong>base</strong> of the logarithm. If ignored, it will return the base 10 as default.</li>
            <li>The second (<code>number2</code>)one is the actual number to apply the logarithm.</li>
        </ul>
    </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>I learned how to get the absolute values of a given column. More importantly, I learned how to obtain the log of different values using different log bases.</p>
<hr>
<a href='https://www.codewars.com/kata/594a8f2f7ca3c692a4000041/sql'>See on CodeWars.com</a>