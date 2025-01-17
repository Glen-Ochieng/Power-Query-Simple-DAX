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
