### Starting 
Clone all the repos needed:
- Frontend
- Knowledge base 
- Database
- Kpi-engine 
- Data preprocessing 
- Rag 

Include the **.env** file inside both the kpi-engine and the root folder. 

The **.env** should include these information:

``DB_HOST="kpi-database"``

``DB_NAME="KPI_database"``

``DB_USER="postgres"``

``DB_PASSWORD="password"``

Change every reference inside the ``main.py`` of the database, to the HOST ip. 
