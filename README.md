# mysql_cloudmanaged_databases
Week 4 Homework Assignment: MySQL on Cloud Platforms - Azure and GCP


GCP and MySQL
In order to do this process you got to google console and sign in. From there you once you have created a project and are in the correct folder you must make sure that you are on the lowest possible cost option. To do that on GCP you have to go to the enterprise option, make sure that you are on 10 GB and also put no backups. From here make note of your IP address that is loaded. From here you can go to the MYSQL workbench and create a new connection. For the connection name, I put gcp scratch instance and for the hostname I inserted in my IP address. From here I was able to create my own tables. My foreign key connecting the two table was the insurnace ID. And my primary key for insurance AETNA was insurance_ID. From there once I had my column names saved and succesfully run, which I was able to see through the green checkmarks once I had clicked the lightening icon, I then created another file where I selected all(*) from my insuranceAETNA table. From ther I went to databases and reverse engineer and I was able to see my ERD Diagram.
Errors:Initially, I had tried to create a new MYSQL connection, however everytime I ran it, it did not go through. Thankfully, once I had returned to my first connection, all my tables executed and ran fine. 

Azure and MySQL
To connect with MySQL workbench client, follow the steps below.
1. Click the + symbol in the MySQL Connections tab to add a new connection.
2. Enter a name for the connection in the Connection name field.
3. Select Standard (TCP/IP) as the Connection Type.
4. Enter 4hw504.mysql.database.azure.com in hostname field.
5. Enter mnh as username and then enter your Password.
6. Go to the SSL tab and update the Use SSL field to Require.
7. In the SSL CA File field, enter the file location of the DigiCertGlobalRootCA.crt.pem file.
8. Click Test Connection to test the connection.
9. If the connection is successful, click OK to save the connection.



For the ERD for GCP, I created two tables. One called insuranceAETNA and one called Health Insurance Plan. In insuranceAETNA, I had insurance_ID and SCRIP. For HealthInsurancePlan I had insurance_ID, plan_name, Provider_name, date_enrolled, address, phone number and email. The foreign key that connects my two tables is insurance_id. And in the insuranceAETNA table the primary key is insurnace_ID. 

<img width="918" alt="Screen Shot 2023-10-01 at 3 57 55 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/3ff06342-abcb-45ce-8ce5-c4e59d399964">



A screen shot showing a successlly run command against your database in MySQL Work Bench
<img width="945" alt="Screen Shot 2023-10-01 at 4 05 22 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/b0e6cff0-f8ea-4cc6-9b4c-6d2490b1b041">
