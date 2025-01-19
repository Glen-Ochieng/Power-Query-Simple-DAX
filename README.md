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

## Merging Datasets
While appending joins datasets by joining the second at the bottom of the first one, merging joins the two side by side using a common column. 

The steps to merge are similar to those of append except in the Home Tab we click Merge in stead of Append.

![image](https://github.com/user-attachments/assets/81579a89-2379-45ec-b85d-1beb3755f1d4)

![image](https://github.com/user-attachments/assets/8a44940c-8a2f-4c78-9848-e976fbe43663)

![image](https://github.com/user-attachments/assets/d04599e6-f3c7-46ba-bdc2-3189aa68a1ea)


## Triming Rows by Character Size 
This is a simple task done by the Extract pane under the Transform Tab 

![image](https://github.com/user-attachments/assets/48377c3a-c2d4-4c70-821d-82a9a7eef97c)

NB: This automatically transforms this column data type to text.

Which luckily you can easily change back to the numeric data type.

![image](https://github.com/user-attachments/assets/21e4a691-4abc-4218-be37-4df967b4baf6)


## Spliting Columns By Delimiter
This is done by selecting the split column pane in the Home Tab. Or if there is a column with special characters present the option appears under the right-click pane.

![image](https://github.com/user-attachments/assets/9650e864-b866-44bf-9040-0c0ba4a99676)

![image](https://github.com/user-attachments/assets/4fad9daf-4112-4b74-b3f4-b274d41a5dcf)

![image](https://github.com/user-attachments/assets/5d9e9fdd-2d29-411f-9f4f-244a21484fb1)


![image](https://github.com/user-attachments/assets/312d6c0d-03e8-429c-8666-125813c17b89)


## Removing special characters

One shortcut to achieve this is to replace them with nothing.

<ins>Example

Replace the closing brackets in the rows of this column.

![image](https://github.com/user-attachments/assets/061a9a2a-ec43-4f76-8a39-8670f4014de7)

The two options to iniate a replace (Under the transform tab / Right Click)

![image](https://github.com/user-attachments/assets/37a02c09-7ead-4496-bc4f-746ac7a31916)

![image](https://github.com/user-attachments/assets/277ef3e0-4260-41db-b23f-c7224d01fcee)

![image](https://github.com/user-attachments/assets/80a0d552-2d9a-4fd7-bb26-a4ae2f1ede50)


## Triming 

Triming involves removing uncessary white space, usually at the end/the start of the row entry.

This is done by right-clicking, then transform then trim. 

![image](https://github.com/user-attachments/assets/68153ff1-5441-45cc-b2ec-a141bc4c4c3f)
