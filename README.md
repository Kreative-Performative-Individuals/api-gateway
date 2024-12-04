### Starting 
Clone all the repos needed:
- Frontend
- Knowledge base 
- Database
- Kpi-engine 
- Data preprocessing 
- Rag 

``git clone git@github.com:Kreative-Performative-Individuals/KB.git``

``git clone git@github.com:Kreative-Performative-Individuals/smart-industrial-database.git``

``git clone git@github.com:Kreative-Performative-Individuals/data-preprocessing-.git``

``git clone git@github.com:Kreative-Performative-Individuals/RAG5.git``

``git clone git@github.com:Kreative-Performative-Individuals/KPI-Engine.git``

``git clone git@github.com:Kreative-Performative-Individuals/frontend.git``

Run: 

``docker compose up --build``

``docker compose down``

``docker compoes up --build``

The first build will take a lot of time. 

Right after test the integration among different services.

If you want to test, the GUI as well, navigate inside the fronted folder and start the container by running:

``docker build -t frontend . ``

``docker run -d --name frontend -p 3000:3000 frontend``

To interact with the gui go to [http://localhost:3000](http://localhost:3000)

### ⚠️ Important Information
Comment out the part that concers RAG and ollama since it's really heavy. To run ollama you need to have an Nvidia GPU and things didn't work on out tests on linux even with proprietary drivers and nvidia card.
