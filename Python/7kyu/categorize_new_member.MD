<h1><strong>Categorize New Member</strong></h1>

<h2><strong>Instructions:</strong></h2>
<hr>

<p>The Western Suburbs Croquet Club has two categories of membership, Senior and Open. They would like your help with an application form that will tell prospective members which category they will be placed.

To be a senior, a member must be at least 55 years old and have a handicap greater than 7. In this croquet club, handicaps range from -2 to +26; the better the player the lower the handicap.</p>

<h2><strong>Output:</strong></h2>
<hr>
<p>Output will consist of a list of string values (in Haskell and C: <code>Open</code> or <code>Senior</code>) stating whether the respective member is to be placed in the senior or open category.</p>

<h2><strong>Example:</strong></h2>
<hr>
<pre>
    <code>
input =  [[18, 20], [45, 2], [61, 12], [37, 6], [21, 21], [78, 9]]
output = ["Open", "Open", "Senior", "Open", "Open", "Senior"]
    </code>
</pre>

<h2><strong>Solution #1:</strong></h2>
<hr>

``` python
def open_or_senior(data):
    result = []
    for v in data:
        if v[0] >= 55 and v[1] > 7:
            result.append('Senior')
        else:
            result.append('Open')
    return result
```

<h3><strong>How did I do it?</strong><h3>
<p>
    <ol>
    <li> Create an empty list to store the string values.</li>
    <li> Iterate through <code>data</code> paired values with its indexes.</li>
    <li> Apply a conditional statement based on the instructions.</li>
    <li> If conditions apply, append the result to the empty list as <code>'Senior'</code>; if not, append it as <code>'Open'</code>.
    <li> Return the appended list.
    </ol>
</p>
<h3><strong>What did I learn?</strong>
<p>It was a good way to practice indexing with lists. Also, I reviewed the usage of <code>and</code> in multiple conditional statements</p>
<br>

<h2><strong>Solution #2</strong></h2>
<hr>

``` python
def open_or_senior(data):
    return ['Senior' if p[0] >= 55 and p[1] > 7 else 'Open' for p in data]
```

<h3><strong>How did I do it?</strong></h3>
<p>
    <ol>
        <li> Use list comprehension to shorten the code.</li>
        <li> Assign each individual value as <code>p</code>, which is applied in a for loop (<code>for p in data</code>).</li>
        <li> Use an <code>if</code> statement, just as before.</li>
        <li> If conditions are met, return <code>'Senior'</code>; otherwise, return <code>'Open</code>.</li>
        <li> Each value will be returned as a list.</li>
    </ol>
</p>
<h3><strong>What did I learn?</strong></h3>
I learned how to use list comprehensions together with comparing values with indexation. Mastering list comprehensions requires practice, as it is a unique pythonic language.
<hr>
</body>
<style>
a:link {
  color: rgb(70, 30, 163);
  background-color: transparent;
  text-decoration: none;
}
</style>
<a href='https://www.codewars.com/kata/5502c9e7b3216ec63c0001aa/train/python'>See on CodeWars.com</a>
