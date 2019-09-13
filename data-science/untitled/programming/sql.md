# SQL

SQL

Search tutorials

Database normalization

Indexing  [https://www.reddit.com/r/programming/comments/7no4pc/my\_site\_use\_the\_index\_luke\_about\_sql\_indexing\_was/](https://www.reddit.com/r/programming/comments/7no4pc/my_site_use_the_index_luke_about_sql_indexing_was/)



Practice where?**SQL**

#### **Postgresql**

**psql -h**[ **xenos-db.omadahealth.net**](http://xenos-db.omadahealth.net/) **-U xenos\_app -d xenos\_production**  


**\d &lt;table&gt;**

**\d+**  
  


**ALTER TABLE case\_annotations DROP COLUMN multi\_user\_overlap;**  


**ALTER TABLE labeled\_weights ADD COLUMN created\_at TIMESTAMP DEFAULT now\(\);**

**ALTER TABLE case\_annotations ADD COLUMN created\_at TIMESTAMP DEFAULT now\(\);**  


**DELETE FROM labeled\_weights WHERE labeler = 'banana';**  


**UPDATE labeled\_weights SET labeler = 'new.name' where labeler = 'old.name';**  


#### **NoSQL**

