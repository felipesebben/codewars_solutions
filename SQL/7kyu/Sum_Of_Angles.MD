<h1><strong>Sum of angles</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p> Find the total sum of internal angles (in degrees) in an n-sided simple polygon. N will be greater than 2.
</p>


<h2><strong>Solution:</strong></h2>

``` SQL
SELECT (n - 2) * 180 AS res FROM angle;
```

<h3><b>How did I do it?</b></h3>
<p>You need to know the formula to calculate the internal angles for a polygon.
<p>To find the sum of interior angles of a polygon, multiply the number of triangles in the polygon by 180°.
The number of triangles in each polygon is two less than the number of sides.</p>
<p>Hence, the formula is:</p>

$(n -2) * 180$

</p>

<h3><strong>What did I learn?</strong></h3>
<p>It was a good way to test my logic and do some research on trigonometry ahahah!</p>
<hr>
<a href='https://www.codewars.com/kata/5a03b3f6a1c9040084001765/train/sql'>See on CodeWars.com</a>