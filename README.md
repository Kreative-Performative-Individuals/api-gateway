# Project Setup Guide

## Prerequisites
- **Docker**: Ensure you have Docker installed and running.
- **Nvidia GPU**: Required to run the model.
- **Windows Operating System**: The tested environment for this setup.

---

## Setup Instructions

### Clone Required Repositories
Run the following commands to clone the necessary repositories:

```bash
git clone git@github.com:Kreative-Performative-Individuals/KB.git
git clone git@github.com:Kreative-Performative-Individuals/smart-industrial-database.git
git clone git@github.com:Kreative-Performative-Individuals/data-preprocessing-.git
git clone git@github.com:Kreative-Performative-Individuals/RAG5.git
git clone git@github.com:Kreative-Performative-Individuals/KPI-Engine.git
git clone git@github.com:Kreative-Performative-Individuals/frontend.git
```

---

### Run Docker Compose

1. Build and start all services:
    ```bash
    docker compose up --build
    ```

2. Stop all services:
    ```bash
    docker compose down
    ```

3. Rebuild and start again (the first build may take some time):
    ```bash
    docker compose up --build
    ```

---

### Test Integration

Ensure that all services communicate properly after the initial setup. 

To test the **GUI**, follow these steps:

1. Navigate to the `frontend` folder:
    ```bash
    cd frontend
    ```

2. Build the frontend Docker container:
    ```bash
    docker build -t frontend .
    ```

3. Run the container:
    ```bash
    docker run -d --name frontend -p 3000:3000 frontend
    ```

4. Open your browser and visit [http://localhost:3000](http://localhost:3000) to interact with the GUI.

---

## ⚠️ Important Notes

1. **Resource-Heavy Components**:
   - Comment out configurations related to **RAG** and **Ollama** if you're experiencing performance issues. 
   - Running **Ollama** requires an Nvidia GPU, and it may not function correctly on Linux, even with proprietary drivers.

2. **Database Initialization**:
   - If the database fails to start, rerun the compose command to ensure the initialization script executes properly:
     ```bash
     docker compose up --build
     ```
---

Happy coding! 🚀
