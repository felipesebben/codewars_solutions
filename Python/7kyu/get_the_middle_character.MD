<h1><strong>Get the Middle Character</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>You are going to be given a word. Your job is to return the middle character of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters.</p>

<h2><strong>Input:</strong></h2>
<p>A word (string) of length <code>0 < str < 1000</code> (In javascript you may get slightly more than 1000 in some test cases due to an error in the test cases). You do not need to test for this. This is only here to tell you that you do not need to worry about your solution timing out.</p>
<h2><strong>Output:</strong></h2>

<p>The middle character(s) of the word represented as a string.</p>

<h2><strong>Example:</strong></h2>

<pre>
    <code>
Kata.getMiddle("test") should return "es"

Kata.getMiddle("testing") should return "t"

Kata.getMiddle("middle") should return "dd"

Kata.getMiddle("A") should return "A"
    </code>
</pre>

<h2><strong>Solution:</strong></h2>

``` python
def get_middle(s):
    if len(s) % 2 == 0:
        return s[(len(s) -1)//2 : (len(s) -1)//2 +2]
    else:
        return s[len(s)//2]
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
    <li> Create an if statement to distinguish between words with even and odd lengths.</li>
        <ul>
            <li>Use the modulo (%) operator. If it returns <code>0</code>, it means we're dealing with a string with an even length; otherwise, it as an odd one. </li>
            </ul>
    <li> Get the middle index number for each case.</li>
        <ul>
            <li>For even cases, get the length of the string, subtract 1 and divide it by 2 using the floor operator (<code>//</code>).</li>
            <li>To get the following letter, just use the same calculation used before and add 1.
            <li>For odd cases, you just need to get the length of the string and divide it by 2.
        </ul>
    </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>Learning how to get indexes with calculations was a tough cookie! But it was a good way to practice indexing and thinking about how to get specific indexes. The even part of the challenge was particularly tricky for me. I know that this is not the best solution for the challenge, but well, what can we do?</p>
<br>

<hr>
<a href='https://www.codewars.com/kata/5502c9e7b3216ec63c0001aa/train/python'>See on CodeWars.com</a>