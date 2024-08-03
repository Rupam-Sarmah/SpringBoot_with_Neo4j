https://www.udemy.com/course/graph-database-neo4j-with-java-spring-boot-nosql-cypher-query-graphdb/learn/lecture/24468582?start=0#overview <br>
https://www.markdownguide.org/hacks/#:~:text=If%20your%20Markdown%20processor%20supports,these%20words%20will%20be%20underlined%20.
<h4>Section 1: Introduction</h4>
<h5>1: Introduction</h5>
<p>-Introduction</p>
<h4>Section 2: Intorduction to Neo4j Part-1</h4>
<h5>2: What is Neo4j?</h5>
<p>-
  Nosql, graph is collection of nodes and relationshio between nodes.
</p>
<h5>3: Node & Relationship</h5>
<p>-
  node: student, subject, department. A node can have multiple label.<br> 
  relationship: belongs, is_learning.It is also known as path between two nodes. But relationship can have only one label.<br>
  <ins>A node can have multiple lab</ins>
</p>
<h5>4: Properties in Neo4j</h5>
<p>-
  Properties: say a node <b>Student</b>. Property will be {name:"John",birth_year:1990;}. <br> Say a property is <b>Is_learning</b>, property will be {marks:80;}.<br><ins> we can't have a nested property.</ins>
</p>
<h4> Section3: Getting started with Neo4j</h4>
<h5>5. Installing Neo4j Desktop</h5>
<p>
  https://neo4j.com/download/
</p>
<h5>6. Create Project & DBMS</h5>
<p>
  create project, create new "local DBMS". "Student DBMS"-studentdbms(pass). Start the DBMS. It will first stop the default/sample movie DBMS after that it will start the newly created "Student DBMS".
</p>
<h5>7. Neo4J Browser Overview</h5>
<p>
  to write our query (or cypher). Queries are write in neo4j browser.
</p>
<h5>8. Creating First Database in Neo4j</h5>
<p>
  <li>Query to create Database: <ins>create database student</ins>. Now select the newly created database.or to use via command type <ins>:use student</ins>(: mention here is important.)</li>
  <li>drop the database: <ins>drop database temp</ins> </li>
</p>
<h4>Section4: CRUD Operations with Neo4j Cypher Query Language</h4>
<h5>9. Create Node</h5>
<p>
  <ins>create ()</ins> A empty node.<br>
  <ins>create(:Student)</ins> Here, "Student" is a label.<br>
  <span>To retireve added nodes, we use <ins>match</ins> keyword.</span>
<!--   <span>3.12</span> -->
  ()--> refer to a node<br>
  abc --> alias. We can give any name.<br>
  <ins>match (abc) return *</ins>  or <ins>match (abc) return abc</ins> -> it will give us the node. In this version, * is mandetory to get answer.Otherwise, this will appear ""Invalid input '': expected "*", "DISTINCT" or an expression (line 1, column 19 (offset: 18))
"match (abc) return"""<br>
  > Create Node with multiple labels:
  <ins>create (:Ram:krishna)</ins>->simple just create node. If I want to create a node and return/view also, command will be <ins>create (st:Ram:krishna) return st
</ins>...Here "st" is a alias.<br>
  >{} is used to give properties. e.g., <ins>create (st:Home:House{Owner: 'John Cena'}) return st</ins> here "name" is a property.<br>
  <ins>create (st:Home:House{Owner: 'John Cena', country:'USA'}) return st</ins><br>
  <ins> create (st:Home:House{Owner: 'Peter', country:'UK'}) return st </ins>
  <ins> match (node) return node </ins> -- get all node<br>
  <ins> match (node:Home) return node </ins> --  get all the nodes whose label is "Home"<br>
</p>

<h5>10. Find Node By Property</h5>
<p>
  <ins> match (node:Home {Owner: 'Peter'}) return node </ins> -- if we add 'peter' instead of 'Peter', it will not show any result.<br>
  <ins> match (node:Home {Owner: 'Peter'}) return node limit 1 </ins> -- limit cql used .<br>
  <ins> match (node:Home {Owner: 'Peter', country:'UK'}) return node </ins> --here "," comma used as "AND" Operator.
</p>

<h5>11. AND operator with Where clause</h5>
<p>
  <ins> match (node:Home)
where node.Owner='John Cena' AND node.country="USA"
return node </ins> -- syntax as same as SQL.
</p>

<h5>12. OR and IN query</h5>
<p>
  <ins> match (node:Home) 
where node.Owner="John Cena" or node.Owner="Peter"
return node </ins> -- OR operator.
  <ins> match (node:Home) where node.Owner IN ["John Cena","Peter"]
return node </ins> -- IN operator.
</p>

<h5>13. Find node by ID</h5>
<p>
  
</p>
