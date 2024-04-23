# Connecting Azure SQL Database with Tableau and Power BI: A Comprehensive Guide


## Problem Statement

Connecting Azure SQL Database with Tableau or Power BI poses challenges like setting up correctly, which can lead to problems accessing data. People often lack clear instructions, causing time wasted on trial and error. We need a clear, easy process that ensures secure connections, enabling smooth data import and analysis in Tableau or Power BI. This will empower users to make informed decisions faster using their Azure SQL Database data


### Datasource
     Azure SQL Database
     server url: tcp:tbsdev.database.windows.net
     user: dockoptimizer
     pw: ***@Venus**
     
     IP Approved on Azure Account (Databse -> Networking) :
     Tableau Cloud: 18.176.203.97
     Local My IP Address: 122.170.11.199
     Power BI service account IP: 52.136.48.125
     
     Profile : Tableau Public Account/ Tableau Cloud
     sachin.soni@techcronus.com
     Sach#tableau123

### Requirement
     Need an Azure account to create a SQL Database, Tableau Cloud and Power BI desktop.
     





### Steps followed 

- #### Step 1: Create Azure Account

     (a) Visit the Azure portal at https://portal.azure.com/ and create an account if you haven't already.

![1 Azure Home](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/10083a55-8493-41f3-a227-18fdf32b1cc2)


- #### Step 2: Create Database
     
     (a) Create a Server:
     
     - Navigate to the Azure portal.
     - In the left-hand navigation pane, select "Create a resource," then select "Databases," and finally choose "SQL Database."
     - Follow the prompts to create a new server.

     (b) Create a Database:
     
     - Once the server is created, navigate to it in the Azure portal.
     - Select "New database" and provide the necessary details to create a new database.


- #### Step 3: Configure Server Settings

     (a) Note Database Information:
     - Make note of the server name, user name, and password set during the server creation process.



     (b) Configure IP Address for Access Rights:
     - In the Azure portal, navigate to your database server.
     - Under "Settings," select "Firewalls and virtual networks."
     - Click on "Add client IP" to allow access from your current IP address. If accessing from other IP addresses, add them accordingly.

     ![0 AzureConnectionError](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/d98059f0-4aa4-4559-8069-e80c9879424f)

     
     (c) Enable Public Accessibility:
     - Under "Settings" for your database server, navigate to "Connection security."
     - Set "Allow access to Azure services" to "Yes" if you want to allow connections from Azure services outside of Azure.



- #### Step 4: Connect with Tableau Cloud
     
     (a) Establishing the Connection
     - Navigate to "Add Data Source" within Tableau Cloud.
     - Select "Connect to Data" and choose "Azure SQL Database" from the available options.
     ![0 Tab Data Connectors](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/ff0ce4f2-2c67-400b-9235-31667f843064)

     - Provide the mandatory details for connecting to the Azure SQL Database, including:
          - Server Name
          - Database Name
          - Authentication Method
          - User Name
          - Password
     
     ![1 Tab Connection](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/e0459462-1b43-4d8a-bba1-dfe2cdd77da0)

     - Click on "Sign In" to initiate the connection process.



     
     (b) Post-Connection Actions
     - Upon successful connection, you'll be prompted to select the desired database and tables for import into Tableau Cloud.
     - Drag each required table into the data modeling space within Tableau Cloud
     - Establish relationships between the tables as needed for your analysis.

     ![2 Tab Datasource Screen](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/1fc35e4a-2e5c-4a37-8a7d-794227c21158)

- #### Step 5: Connect with Power BI
     
     (a) Get Data from Azure SQL Database
     - Navigate to the "Get Data" option and select "Azure" -> "Azure SQL Database.
     ![PBI 00 Get Data ](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/06820edf-4fa5-499c-aaf4-80c4792bb69d)

     - Provide server details such as the server name, database name (optional), and select the appropriate data connectivity mode.
     ![PBI 0 Connection](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/34f4c8ba-04b7-4eef-afff-288d41dade29)

     ![PBI 1 Server details](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/8ee33c00-a09d-4bc5-b047-c32dba9b6759)


     - Enter access credentials, including the username and password.

     ![PBI 2 UserPw ](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/47944f87-7e54-424d-a5a3-82e7ce1b397c)


     (b) Importing Data Tables
     - Choose the required tables from the available options and click on "Load" or "Load and Transform."

     ![PBI 3 Data Tables](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/3f261c85-bd20-4e4c-8a6e-59230a7662f0)



     - Utilize the imported data tables for creating insightful dashboards and visualizations.
     ![PBI 3 1 Import Data tables](https://github.com/Soni-Sachin-94240/MS-Fabric-Extract-and-Load-from-External-API/assets/132342151/4616dbfc-222c-4284-9703-999b4af17682)

- #### Step 6: Connect via Power BI Service Account
     - Publish the report to the designated workspace in the Power BI service account.
     ![PBI 5 1 Workspace](https://github.com/Soni-Sachin-94240/Connecting-Azure-SQL-Database-with-Tableau-and-Power-BI/assets/132342151/28e0fc70-eefa-4f9d-a29f-2af22eaa93c2)

     - Navigate to the settings for the published report.
     ![PBI 5 2 Settings ](https://github.com/Soni-Sachin-94240/Connecting-Azure-SQL-Database-with-Tableau-and-Power-BI/assets/132342151/f42d0dcb-99f9-4e18-b517-afaf00cf9065)

     - Access "Data Source Credentials" and select "Edit Credentials."
     ![PBI 5 3 Data Source Setting](https://github.com/Soni-Sachin-94240/Connecting-Azure-SQL-Database-with-Tableau-and-Power-BI/assets/132342151/bc83b4e3-015b-4a31-86ba-1c5670c05135)

     - Provide access credentials, specifying the Authentication Method, username, password, and Privacy Level as required.
     ![PBI 5 4 Data Source Credential](https://github.com/Soni-Sachin-94240/Connecting-Azure-SQL-Database-with-Tableau-and-Power-BI/assets/132342151/708ca160-a985-46ee-89db-9c9147f08c74)

     - Schedule Resfresh setting
     ![PBI 5 5 Schedule Refresh](https://github.com/Soni-Sachin-94240/Connecting-Azure-SQL-Database-with-Tableau-and-Power-BI/assets/132342151/c80c59f4-45cb-439d-8b3e-69125f3603f1)
 



### Conclusion

Establishing a datasource connection from Azure SQL Database to Tableau or Power BI is essential for effective data analysis and decision-making. This guide has provided clear steps for creating an Azure account, setting up a SQL Database, configuring server settings, and establishing connections with Tableau or Power BI. By following these guidelines, users can seamlessly integrate their Azure SQL Database data into their preferred visualization platform, enabling them to derive valuable insights and drive informed business decisions. This streamlined process ensures efficiency, security, and optimization in leveraging Azure SQL Database data for visual analysis.
