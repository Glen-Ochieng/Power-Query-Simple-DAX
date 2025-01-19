# Power-Query-Simple-DAX

## To create a new column that's a multiple of two columns

Columnname= table1name[columnname]* table2name[columnname ] 

Example
> salesamount= products[unitprice]* products[quantityordered]


## It is possible to create a new column from two seperate tables/datasets related by a unique column shared by both tables.

To achieve this first of all under the Power Pivot pane an existing relationship between the two tables must be existing.

<img width="615" alt="image" src="https://github.com/user-attachments/assets/376fd175-1362-4a25-9407-decf8a9d4d5d" />

Proceeding, we use a similar syntax to the previous but we enclose the second table in this syntax**Related()**

>salesamount= products[unitprice]*Related([products[quantityordered])


## Appending datasets 

Similar to SQL we can merge two or more datasets together. In SQL, the syntax would be UNION.

And just like with the UNION syntax similar rules of a merge carry over. The two datasets being merged must have the same structure ie. same column names and same number of columns.

<ins>Example
Merge the top categories of movies from the following website: 

https://www.boxofficemojo.com/chart/top_lifetime_gross/?area=XWW

![image](https://github.com/user-attachments/assets/32cfc165-3a76-42ee-ac5e-d4f2bc2be960)

<b> Step 1 

Upload the datasets from the web using the URL from each categrories of the top shows starting with the top 200 of all time.

![image](https://github.com/user-attachments/assets/5c5f4f17-ad54-4111-9d05-2c7fda5b9d5a)

Use the New Source pane to quickly add the other datasets

![image](https://github.com/user-attachments/assets/478735b4-0d9f-4cde-af93-02bf818349f2)

<b> Step 2 

Set the first dataset as a reference. And it will be picked up as the dataset the others will be joined to.
Do this by right-clicking the dataset and clicking reference 

![image](https://github.com/user-attachments/assets/43649e8b-df82-40cd-a928-133f724b3786)

After the dataset has been set as a reference, it will be added as a duplicate dataset at the bottom of the page. It is wise to rename it ; in this case it will be renamed Top Sales.

<b> Step 3 

Click the Append Option in the Home Page of Power Query

![image](https://github.com/user-attachments/assets/8b9124c6-398c-4e81-9c9a-65eb32faa193)

Select the other datasets and perform the append.
