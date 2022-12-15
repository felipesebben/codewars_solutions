<h1><strong>SQL Statistics: MIN, MEDIAN, MAX</strong></h1>

<h2><strong>Instructions:</strong></h2>

<p>For this challenge you need to PIVOT data. You have two tables, products and details. Your task is to pivot the rows in products to produce a table of products which have rows of their detail. Group and Order by the name of the Product.</p>

<h2><strong>Tables and relationship below:</strong></h2>
<img src= "http://i.imgur.com/81Ww3YH.png", alt="Table Scheme">

<h2><strong>Output:</strong></h2>
<p>You must use the CROSSTAB statement to create a table that has the schema as below:

<p><strong>CROSSTAB table</strong>
    <ul>
        <li>name</li>
        <li>good</li>
        <li>ok</li>
        <li>bad</li>
    </ul>
</p>

<h2><strong>Solution #1:</strong></h2>

``` SQL
CREATE EXTENSION tablefunc;

SELECT *
FROM CROSSTAB('SELECT p.name, d.detail, COUNT(d.id) 
              FROM products p
              JOIN details d
                ON p.id = d.product_id
              GROUP BY p.name, d.detail
              ORDER BY p.name, d.detail')
      AS final_result (name TEXT, bad BIGINT, good BIGINT, ok BIGINT);
```

<h3><b>How did I do it?</b></h3>
<p>
    <ol>
    <li> Create a <code>CROSSTAB</code> function. The input will be a query, which must be written in quotation marks.</li>
    <li> The <code>CROSSTAB</code> takes three necessary arguments as columns:</li>
        <ul>
            <li> The first is the <code>id</code> to be used; in this case, we'll pivot using <code>name</code>.</li>
            <li>Then, select the column that will be pivoted. It must be categorical, and, in this case, we'll pivot <code>detail</code>.</li>
            <li>Then, the third argument takes the measures column which will fill each pivoted column; here, we'll select the count of <code>id</code> observations from the <code>details</code> table.</li>
            <li>Since we are dealing with two different tables, we'll need to join them using <code>JOIN</code> on <code>product</code> <code>id</code> and <code>detail</code> <code>product_id</code>. Group the query by <code>name</code> and <code>detail</code>.
        </ul> 
        <li> Define the details of each pivoted column. You need to name each new feature, as well as its dtype. Be aware of the precise order requested by the challenge, or it won't result the expected query.</li>
    </ol>
</p>

<h3><strong>What did I learn?</strong></h3>
<p>I learned A LOT. I had no idea you could pivot tables in SQL. This only shows how it is such a powerful tool, with limitless possibilities!</p>
<hr>
<a href='https://www.codewars.com/kata/58126aa90ea99769e7000119'>See on CodeWars.com</a>