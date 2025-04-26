# cse370-lab-2-sql-subqueries-aggregate-functions-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/course-code-cse-370-3/

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;131315&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE370 Lab 2-SQL Subqueries \u0026amp; Aggregate Functions Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">
            
<div class="kksr-stars">
    
<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
    
<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>
                

<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
Course Name: Database Systems Semester: Summer 24

Lab 02: SQL Subqueries &amp; Aggregate Functions

Activity List

● All commands are shown in the red boxes.

● In the green box, write the appropriate query/answer.

● All new queries should be typed in the command window after mysql&gt;

● Start by connecting to the server using: mysql -u root -p [password: &lt;just press enter&gt;] ● For more MySQL queries, go to www.w3schools.com/sql or google it!

Initial Table: It’s a bit different than Lab 01!

std_id name major section days_present project_mark s cgpa submission_date

Link for Table Data: https://docs.google.com/document/d/1ZFFMN863k9GOjTG6ibbCAEEdqF3ExJzug-ymPON6ofA/

The purpose of the SELECT statement is to retrieve and display data from one or more database tables. It is an extremely powerful command. SELECT is the most frequently used SQL command and has the following general form:

SELECT [DISTINCT | ALL] {* | [columnExpression [AS newName]] [, . . .]}

FROM TableName [alias] [, . . .]

[WHERE condition]

[GROUP BY columnList] [HAVING condition]

[ORDER BY columnList]

columnExpression represents a column name or an expression, TableName is the name of an existing database table or view that you have access to, and alias is an optional abbreviation for TableName.

The sequence of processing in a SELECT statement is:

↓

FROM specifies the table or tables to be used

WHERE filters the rows subject to some condition

GROUP BY forms groups of rows with the same column value

HAVING filters the groups subject to some condition

SELECT specifies which columns are to appear in the output

ORDER BY specifies the order of the output

The order of the clauses in the SELECT statement cannot be changed. The only two mandatory clauses are the first two: SELECT and FROM; the remainder are optional. The SELECT operation is closed: the result of a query on a table is another table.

Task 1: Aggregate Functions, Group By and Having:

● What is the purpose of the group by keyword? In the above command, if we group by sub_date, instead of major, what will be the output?

● The having and where clauses are both used to specify a condition when selecting rows. What is the difference between them?

Task 2: Sub Queries/Nested Queries, Any and All:

Now, try the nested/sub query on the right

SELECT name FROM Lab_Grades

WHERE project_marks=(SELECT MAX(project_marks)

FROM Lab_Grades);

● Did you understand the role of “any” and “all” in the above queries? Explain below.

Task 3: Correlated Subqueries and Exists:

● L1 and L2 are temporary aliases and create two separate instances for Lab_Grades; why are they required?

● Please identify the difference between the above two queries. [Hint: 1 asks for unique-only 1 student got the highest and the other didn’t]

Retrieve the major which has the highest number of students enrolled.

Task 4: Take a Quiz

SELECT major FROM Lab_Grades GROUP BY major HAVING count(*) &gt;= ALL (SELECT count(*) FROM Lab_Grades GROUP BY major);

Go to https://sqlzoo.net/wiki/Nested_SELECT_Quiz to test your understanding of the queries taught in class.
