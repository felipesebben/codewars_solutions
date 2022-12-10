<h1><strong>Even or Odd</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>You will be given a table, <code>numbers</code>, with one column <code>number</code>.

Return a table with a column <code>is_even</code> containing <code>"Even"</code> or <code>"Odd"</code> depending on <code>number</code> column values.</p>

<h3><p><strong>numbers table schema</strong></p></h3>
<ul>
    <li>number INT</li>
   </ul>

<h3><p><strong>output</strong></p></h3>
<ul>
    <li>is_even STRING</li>
</ul>

<h2><strong>Solution:</strong></h2>

``` SQL
SELECT CASE number % 2
            WHEN 0 THEN 'Even'
            ELSE 'Odd'
            END AS is_even
                    
FROM numbers
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
        <li> Use <code>CASE()</code> to make a conditional statement.</li>
        <li>Apply the modulo (<code>%</code>) operator as the condition to be met. In this case, we are checking if <code>number</code> returns any remaining value if divided by 2.</li>
        <li>In case the result is 0, we know that the number is even, so we return <code>'Even'</code>; else, return <code>'Odd'</code></li>
    </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>It was a good way to review the modulo operator on SQL while combining it with a CASE statement.</p>
<hr>
<a href='https://www.codewars.com/kata/53da3dbb4a5168369a0000fe/train/sql'>See on CodeWars.com</a>