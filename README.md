# DATABASE-MIGRATION
This project will transfer a database data, objects and structure from one location to another while keeping it within the same instance.

**CASE SCENARIO**

**Microsft** needs to move some data in AdventureWorks2019 to another database on  different filegroup or drive, this is because they want to imporve performance and optimize storage

**SOLUTION**

Create a new database (Microsoft_Sales_DB) to move the data into from AdventureWorks

**PROCESS**

--> Open SQL Server Management Studio (SSMS) and connect to the SQL Server instance containing both databases.

--> Expand the "Databases" node to view the list of databases.

--> Right-click on the source database i.e (AdventureWorks2019) and select "Tasks" > "Export Data..." from the context menu. This will open the SQL Server Import and Export Wizard.

![Screenshot (20)](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/DATABASE-MIGRATION/assets/100750844/9a23c88d-4b59-480d-b11c-b1148c781577)

--> In the wizard, select the "Data source" as the source database (AdventureWorks2019) and provide the necessary authentication details.

![Screenshot (21)](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/DATABASE-MIGRATION/assets/100750844/a48392f1-76d5-4a6d-99cf-3784c76525fe)


--> Choose the "Destination" as the destination database (DestinationDB) and provide the required authentication information.

![Screenshot (22)](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/DATABASE-MIGRATION/assets/100750844/9860af7d-5fcd-41ad-b60d-03fbd240abd5)

--> Click on copy data from one or more tables or views

--> Click on Next

--> Select the tables or views you want to transfer from the source database to the destination database. (I selected everything under the sales schema)

--> Configure any necessary transformation or mapping options, such as column mapping, data type conversions, etc., if needed.

![Selecting tables to transfer to the destination DB](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/DATABASE-MIGRATION/assets/100750844/51d18a52-e481-4bf1-a14a-574e274767d0)

--> Review the summary of the transfer operation and click "Finish" to start the data transfer process.

![Migration Summary](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/DATABASE-MIGRATION/assets/100750844/be963927-3863-4f4f-a10c-5002d582ea94)


--> The wizard will show the progress of the data transfer, and once completed, you will see a summary of the operation.

--> Finally, you can connect to the destination database (DestinationDB) in SSMS to verify that the data has been successfully moved.
