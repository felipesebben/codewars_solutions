<h1><strong>Beginner Series #2 Clock</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>Clock shows <code>h</code> hours, <code>m</code> minutes and <code>s</code> seconds after midnight.

Your task is to write a function which returns the time since midnight in milliseconds.</p>

<h2><strong>Example:</strong></h2>

<pre>
 <code>
h = 0
m = 1
s = 1

result = 61000
    </code>
</pre>

<h2><strong>Input constraints:</strong></h2>
<ul>
    <li><code>0 <= h <=23</code></li>
    <li><code>0 <= m <=59</code></li>
    <li><code>0 <= s <=59</code></li>
</ul>

<h2><strong>Solution #1:</strong></h2>

``` python
def past(h, m, s):
    hour = h * 60 * 60 * 1000
    min = m * 60 * 1000
    sec = s * 1000 
    return hour + min + sec
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
    <li>Create one variable for each of the three arguments.</li>
    <li>It's easier to start first with seconds by multiplying by 1000.</li>
    <li>Then, multiply minutes by the number of seconds, which is 60 times 1000.</li>
    <li>Following, to get the converted hour measure, multiply the h argument by 60 (n of minutes), 60 once again (n of seconds) and 1000 (millisseconds).</li>
    <li>Finally, just sum the three arguments.</li>
    <li>That's it!</li>
    </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>That was more of a logical problem. Language-wise, basically you just had to create some variables, store values in each of them, and return the sum of them. But logic is an essential part of any programming language, right?</p>


<hr>
<a href='https://www.codewars.com/kata/55f9bca8ecaa9eac7100004a/train/python'>See on CodeWars.com</a>