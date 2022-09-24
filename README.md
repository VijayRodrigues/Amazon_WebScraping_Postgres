# Amazon_WebScraping_Postgres 


## Description

The idea is to extract the required data from Amazon.in (in this case, all laptop details) by Web Scraping and saving the results on PostgreSQL database.
Based on the most common searches, I have segregated the search string to the the folloing keywords: gaming laptops, student laptops, business laptops, tocuhscreen laptops, programming laptops, fingerprint laptops, convertible laptops and video editing laptops

### Dependencies

* You would require Selenium Webdriver suitable for your browser.
* Kindly use Google Chrome - as this code is built on this driver.
* Please install the following python packages using pip



![pack](https://user-images.githubusercontent.com/72039550/192081245-d3b0c7e6-329c-454f-a141-5b23e0dafa92.png)

* Install PgAdmin latest version and all other dependencies that come along with it. You can refer to this link
    https://www.pgadmin.org/download/pgadmin-4-windows/
    
* I have 6.12 verison installed.


![pgadmin](https://user-images.githubusercontent.com/72039550/192081464-22354ec5-e009-4fbe-9657-01b936b0d2f9.png)

<br><br>
NOTE:  By default, a new verion of Selenium get's installed (4+ onwards).  The tags **find_element_by_xpath** and **find_elements_by_xpath** have been deprecated in these version and the code may not run if you have newer version of selenium. To avoid such issues, kindly use the above given verison (any version less than 4.0)


## Getting Started

* 1) A database by the name "amazon_products" is already created (manually) in PgAdmin
![db_name](https://user-images.githubusercontent.com/72039550/192081173-5af21c9a-634b-4228-b65c-dcd308f559f2.jpg)

<hr>

* 2) a table by the name "Amazon_Products" is created through the script itself - using SqlAlchemy package.
![U2](https://user-images.githubusercontent.com/72039550/149824922-b33593d5-cede-42b3-96fe-b971c7c208a1.png)

<hr>

* 3) An example of how to create **items_table**. Google BigQuery does not allow to manually add files above 10 mb and rows above 100. If the files size is high and numbers of rows are more then we may need to add from **google drive**. SInce my file sie's are more than 600MB I have added through the drive as mentioned.

![U3](https://user-images.githubusercontent.com/72039550/149825407-04f85b70-8937-444d-a260-d7fb8debad98.png)

* 4)  The following scrrenshot shows all the created tables

![U4](https://user-images.githubusercontent.com/72039550/149825639-9c515d32-4698-43c2-8817-2359a855a233.png)


<hr>
<hr>
<hr>


## Executing program

* The following query joins all the tables i.e. **region_table**, **items_table**, **order_table**, **total_table** and **items_table** (a total of 5 tables)

![Untitled1_query](https://user-images.githubusercontent.com/72039550/149822131-14191a12-8f65-4b7a-bee0-ed62a33fe5bb.png)

![Untitled1_output](https://user-images.githubusercontent.com/72039550/149822139-b799e5d6-6764-49db-9ff4-7a9ad1040529.png)


<hr>


* The following query joins both **sales_table** and **region_table**, with an aggregate function COUNT  on **sales_channel**

![Untitled2](https://user-images.githubusercontent.com/72039550/149822824-72d1b654-93d5-4cc7-94af-12dac1374a07.png)


<hr>


* The following query shows the country **"Rwanda"** has higher total_revenue and the data is sorted in descending order by **total_revenue** with an alias **TotalRevenue**

![Untitled3](https://user-images.githubusercontent.com/72039550/149823424-385d8b31-a996-4aee-986d-6cc55bbbdea3.png)


<hr>

* The following query shows **sales channel preference** between **"online"** and **"offline"**. It shows that although there is no much difference between the total profit, but **offline** channel seems to be a little higher. 
![Untitled4](https://user-images.githubusercontent.com/72039550/149823932-066ef6c0-1891-4b8a-b03b-dfa9aeeb70ae.png)

<hr>

* The following query gives the Average total cost of units that come across the regions (continent / division of continent).

![Untitled5](https://user-images.githubusercontent.com/72039550/149824349-9ecccabd-d2f1-4f70-82bd-1f21cab2c9d0.png)


<hr>

