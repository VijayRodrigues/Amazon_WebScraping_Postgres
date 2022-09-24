# Amazon_WebScraping_Postgres 


## Description

The idea is to extract the required data from Amazon.in (in this case, all laptop details) by Web Scraping and saving the results on PostgreSQL database.
Based on the most common searches, I have segregated the search string to the the folloing keywords: gaming laptops, student laptops, business laptops, tocuhscreen laptops, programming laptops, fingerprint laptops, convertible laptops and video editing laptops

### Dependencies

* You would require Selenium Webdriver suitable for your browser.
* Kindly use Google Chrome - as this code is built on this driver.
* Please install the following python packages using pip
<br>

  ![pack](https://user-images.githubusercontent.com/72039550/192081245-d3b0c7e6-329c-454f-a141-5b23e0dafa92.png)
<br>
* Install PgAdmin latest version and all other dependencies that come along with it. You can refer to this link
    https://www.pgadmin.org/download/pgadmin-4-windows/
    <br>
* I have 6.12 verison installed.
<br>

![pgadmin](https://user-images.githubusercontent.com/72039550/192081464-22354ec5-e009-4fbe-9657-01b936b0d2f9.png)

<br><br>
NOTE:  By default, a new verion of Selenium get's installed (4+ onwards).  The tags **find_element_by_xpath** and **find_elements_by_xpath** have been deprecated in these version and the code may not run if you have newer version of selenium. To avoid such issues, kindly use the above given verison (any version less than 4.0)
<br>

## Getting Started

* 1) A database by the name "amazon_products" is already created (manually) in PgAdmin
* <br>
![db_name](https://user-images.githubusercontent.com/72039550/192081173-5af21c9a-634b-4228-b65c-dcd308f559f2.jpg)

<hr>

* 2) a table by the name "Amazon_Laptops" is created through the script itself - using SqlAlchemy package.
* <br>

![tabl](https://user-images.githubusercontent.com/72039550/192104858-c019320d-cb70-4c1d-9899-156ceb4e123d.png)
<br>
<hr>


## Executing program

* The following query displays all the records that were appended to the table "Amazon_Laptops"
<br>
![tabquery](https://user-images.githubusercontent.com/72039550/192105067-e884df42-39cf-478c-a13a-11a08ba03ede.png)

<br><br>
![querytab](https://user-images.githubusercontent.com/72039550/192105060-ded88e7f-b170-4c0f-9bfd-1df9b946ffc7.png)

<hr>

