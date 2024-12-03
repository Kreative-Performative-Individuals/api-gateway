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

Change every reference inside the ``main.py`` of the database, to the HOST ip with the database service name, so change from the hardcoded IP address to ``kpi-database``.

Put the docker compose file, inside the root folder.

If not present already (waiting for merge of the pull request), put the provided docker file inside the frontend folder.

Run: 

``docker compose up --build``

The first build will take a lot of time. 

Right after test the integration among different services.
