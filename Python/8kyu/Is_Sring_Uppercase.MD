<h1><strong>Is the string uppercase?</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>Create a method to see whether the string is ALL CAPS. In this Kata, a string is said to be in ALL CAPS whenever it does not contain any lowercase letter so any string containing no letters at all is trivially considered to be in ALL CAPS.
</p>

<h2><strong>Example (input - output):</strong></h2>
<pre>
 <code>
"c" -> False
"C" -> True
"hello I AM DONALD" -> False
"HELLO I AM DONALD" -> True
"ACSKLDFJSgSKLDFJSKLDFJ" -> False
"ACSKLDFJSGSKLDFJSKLDFJ" -> True
    </code>
</pre>

<h2><strong>Solution #1:</strong></h2>

``` python
def is_uppercase(inp):
    return False if any(l for l in inp if l.islower()) else True
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
    <li>Use a boolean logic (True/False).</li>
    <li>Since we need to check each character in a given string, use list comprehension to do a for loop.</li>
    <li>Use <code>any()</code> to check if any of the items in a list are true.</li>
    <li>If any lower case letter is detected, return <code>False</code>; otherwise, return <code>True</code></li>
    <li>That's it!</li>
    </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>What a good way to learn about the <code>any()</code> function! Although there are probably easier ways to solve this kata, this is the one that I came across while researching online and I found it very easy to understand!</p>


<hr>
<a href='https://www.codewars.com/kata/56cd44e1aa4ac7879200010b/train/python'>See on CodeWars.com</a>