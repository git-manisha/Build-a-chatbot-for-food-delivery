# Build-a-chatbot-for-food-delivery

# Project Setup Guide

## Directory Structure
```
backend/              # Contains Python FastAPI backend code
db/                   # Contains the dump of the database (to be imported into MySQL)
dialogflow_assets/     # Training phrases and intents for Dialogflow
frontend/             # Website code
```

## Installation
### Install Required Modules
Run the following commands to install necessary dependencies:
```sh
pip install mysql-connector
pip install "fastapi[all]"
```
Or, install all dependencies in one shot using:
```sh
pip install -r backend/requirements.txt
```

## Starting the FastAPI Backend Server
1. Open the command prompt and navigate to the `backend` directory:
   ```sh
   cd backend
   ```
2. Run the following command to start the FastAPI server:
   ```sh
   uvicorn main:app --reload
   ```

## Importing Database Dump
1. Open **MySQL Workbench**.
2. Create a new database or use an existing one.
3. Import the database dump located in the `db` directory.
4. Ensure the database connection is properly configured in the backend.

## Setting up ngrok for HTTPS Tunneling
1. Download ngrok from [https://ngrok.com/download](https://ngrok.com/download) and install the appropriate version for your OS.
2. Extract the zip file and place `ngrok.exe` in a folder.
3. Open the command prompt, navigate to the folder where `ngrok.exe` is located, and run the following command:
   ```sh
   ngrok http 8000
   ```
   (Ensure that the FastAPI server is running on port 8000.)

### Note
- **ngrok sessions can expire**. If you see a session expired message, restart ngrok using the above command.

## Additional Notes
- Ensure MySQL is running before starting the backend.
- Update the `.env` file or configuration settings as needed.
- The frontend should be configured to interact with the backend API endpoint provided by ngrok or localhost.

