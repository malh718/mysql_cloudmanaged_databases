# mysql_cloudmanaged_databases
Week 4 Homework Assignment: MySQL on Cloud Platforms - Azure and GCP


GCP and MySQL
In order to do this process you got to google console and sign in. From there you once you have created a project and are in the correct folder you must make sure that you are on the lowest possible cost option. To do that on GCP you have to go to the enterprise option, make sure that you are on 10 GB and also put no backups. From here make note of your IP address that is loaded. From here you can go to the MYSQL workbench and create a new connection. For the connection name, I put gcp scratch instance and for the hostname I inserted in my IP address. From here I was able to create my own tables. My foreign key connecting the two table was the insurnace ID. And my primary key for insurance AETNA was insurance_ID. From there once I had my column names saved and succesfully run, which I was able to see through the green checkmarks once I had clicked the lightening icon, I then created another file where I selected all(*) from my insuranceAETNA table. From ther I went to databases and reverse engineer and I was able to see my ERD Diagram.
Errors:Initially, I had tried to create a new MYSQL connection, however everytime I ran it, it did not go through. Thankfully, once I had returned to my first connection, all my tables executed and ran fine. 

For the ERD for GCP, I created two tables. One called insuranceAETNA and one called Health Insurance Plan. In insuranceAETNA, I had insurance_ID and SCRIP. For HealthInsurancePlan I had insurance_ID, plan_name, Provider_name, date_enrolled, address, phone number and email. The foreign key that connects my two tables is insurance_id. And in the insuranceAETNA table the primary key is insurnace_ID. 

<img width="918" alt="Screen Shot 2023-10-01 at 3 57 55 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/3ff06342-abcb-45ce-8ce5-c4e59d399964">



A screen shot showing a successlly run command against your database in MySQL Work Bench
<img width="945" alt="Screen Shot 2023-10-01 at 4 05 22 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/b0e6cff0-f8ea-4cc6-9b4c-6d2490b1b041">



Azure and MySQL

As shown in the microsoft azure website: 

"To connect with MySQL workbench client, follow the steps below.
1. Click the + symbol in the MySQL Connections tab to add a new connection.
2. Enter a name for the connection in the Connection name field.
3. Select Standard (TCP/IP) as the Connection Type.
4. Enter mnh.mysql.database.azure.com in hostname field.
5. Enter mnh as username and then enter your Password.
6. Go to the SSL tab and update the Use SSL field to Require.
7. In the SSL CA File field, enter the file location of the DigiCertGlobalRootCA.crt.pem file.
8. Click Test Connection to test the connection.
9. If the connection is successful, click OK to save the connection."


<img width="1294" alt="Screen Shot 2023-10-01 at 8 24 12 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/5733ca4d-4752-4ab1-8bfa-381536971f61">

<img width="1234" alt="Screen Shot 2023-10-01 at 8 25 09 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/2d9b337a-4189-4271-a898-d24cdcf8f63f">



In this example, I used the patients and demographics code that was given in week4.
For demographics, there was demographic_id, patient_id, first_name, last name date of birth, address, phone number and email. And for patient there was mrn and patient_id. The primary key for patients was patient_id and for demographics it was demographic_id.The foreign key is patient_id.
<img width="1200" alt="Screen Shot 2023-10-01 at 8 33 46 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/7ce4a513-9fe8-497d-9646-a1b50da47549">


*** I really did not think it was going to work for a couple hours, but then after my like 12th attempt it worked. Below are some of the errors I got, when i thought it wasnt going to work. 

I made approximately 8 different resource groups and I got a multitude of errors. I included errors that I had gotten in screenshot 2 and 3 when trying to connect. I am unsure why this did not work, I tried making about 15 connections on workbench and it was just not connecting for some reason. I followed the connection instructions they had on the website and still got either one of the two errors listed below. I looked the errors up online and tried multiple varaitions and still am not getting it to connect. It is definitly not a password issue, as I made sure to put the correct information the multiple times I tried. 

I created added in code from class 4 that had to do with patients and demographics and created my databases. However I kept getting errors as shown in screenshot 1. I have been the past 4 hours trouble shooting this and it is just not connecting. I have public access allowed, I also have allow all for the firewall portion. 


screenshot 1
<img width="1176" alt="Screen Shot 2023-10-01 at 7 54 36 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/837aa28b-c553-4973-8f9c-74054a4f030b">

Screenshot 2 and 3
<img width="400" alt="Screen Shot 2023-10-01 at 6 48 26 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/c784b818-7959-4770-bdf9-6280915f676a">

<img width="419" alt="Screen Shot 2023-10-01 at 7 29 00 PM" src="https://github.com/malh718/mysql_cloudmanaged_databases/assets/102617334/494555ab-6e1d-4b5b-83cc-1a2fbf3e6885">


***But then it worked!!!!!! and the issue was the stuff on the ssl tab. When I took that out, and then put in the code shown on in week4, it went through and I was able to succesfully reverse engineer and show my ERD with patients and demographics. 
