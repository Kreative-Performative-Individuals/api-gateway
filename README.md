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

Right after this, execute: 

``docker compose up --build``

After the database container is running, follow the procedure to execute the ``.sh`` script to initialize the database by running: 

``./build_db.sh smart-database-container exports.sql KPI_database``

Then open a terminal inside the RAG container and execute:

``ollama pull llama3.2``
``ollama pull nomic-embed-text``
