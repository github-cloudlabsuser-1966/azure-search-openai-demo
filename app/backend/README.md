# Backend Application Documentation

## Overview
The backend application is built using Quart, a Python framework for asynchronous web applications. It is part of an AI Chat App and communicates with the frontend using the AI Chat App HTTP Protocol. The main purpose of the backend is to handle requests from the frontend, process them, and return the appropriate responses.

## Installation
The backend application is deployed using Azure services. The infrastructure is defined in the `infra/main.bicep` file. The application is hosted on an Azure App Service with Python 3.11 runtime.

## Configuration
The backend application is configured through environment variables. These variables include settings for various features and services such as Azure AI Search, OpenAI, and Azure Cognitive Services. The `config()` function in `app/backend/app.py` provides an overview of these configuration options.

## Usage
The backend application provides several endpoints for the frontend to interact with. These include:

- `/:` The root endpoint.
- `/redirect:` An empty page used for login redirect.
- `/favicon.ico:` The favicon for the application.
- `/assets/<path:path>:` Serves static assets.
- `/content/<path>:` Serves content.

## Dependencies
The backend application uses several external libraries, including:

- `azure.cognitiveservices.speech:` For speech synthesis.
- `azure.core:` For handling Azure-specific exceptions.
- `azure.identity.aio:` For Azure identity and authentication.
- `azure.monitor.opentelemetry:` For monitoring and telemetry.
- `azure.search.documents.aio:` For interacting with Azure AI Search.
- `azure.storage.blob.aio:` For interacting with Azure Blob Storage.
- `quart:` For building the web application.
- `quart_cors:` For handling Cross-Origin Resource Sharing (CORS).
- `openai:` For interacting with OpenAI.

## File Structure
The backend application consists of the following main files:

- `app/backend/core/:` This directory contains core functionalities such as authentication.
- `app/backend/decorators/:` This directory contains decorators used in the application.
- `app/backend/error/:` This directory contains error handling code.
- `app/backend/prepdocs/:` This directory contains code for preparing documents for processing.
- `app/backend/prepdocslib/:` This directory contains libraries used in document preparation.

## Contributing
Please refer to the `CONTRIBUTING.md` file in the root of the repository for guidelines on contributing to this project.

## License
The backend application is distributed under the license specified in the `LICENSE.md` file in the root of the repository.

## Contact
For any queries or issues, please refer to the `CODE_OF_CONDUCT.md` file in the root of the repository for contact information.