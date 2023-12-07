# Minutes to Meeting

**Minutes to Meeting** is a comprehensive solution designed to enhance the utility of virtual meetings by seamlessly integrating with Google Meet. The project includes a web extension for real-time transcript capturing and streamlined PDF summaries, as well as a web application for managing meeting details, transcripts, and summaries.

## Tech Stack

- **Frontend:** React, JavaScript
- **Backend:** Django
- **Database:** SQL

## Project Description

Minutes to Meeting provides a seamless integration with Google Meet, offering the following features:

1. **Real-time Transcript Capturing:**
   - The web extension captures subtitles and speaker names during a Google Meet session using a MutationObserver.
   - Speaker names and subtitles are processed and stored in Chrome's synchronized storage.

2. **Streamlined PDF Summaries:**
   - The web extension and web application work together to generate multilingual meeting summaries.
   - NLP and Google Translate are employed to create point-by-point summaries from the meeting transcript.

3. **Accessibility Options:**
   - Integration of translation and text-to-speech functionalities to provide accessibility options for diverse team members during meetings.

## Models

### User
- Fields: email, name, password, active

### MeetContent
- Fields: meet_id, owner, date, title, duration, transcript, summary

## MVT (Model-View-Template) Architecture

- **Model:** Represents the data (e.g., User, MeetContent).
- **View:** Handles requests and returns the relevant template and content based on user requests.
- **Template:** HTML files containing the layout of the web pages.

## Serializers

Serializers in Django REST Framework convert complex data types into formats understandable by JavaScript and front-end frameworks. They play a crucial role in data serialization, API development, data rendering, and deserialization.

## Extension

The Chrome extension handles user authentication, captures meeting details, subtitles, and speaker names, and sends the information to the backend. The manifest.json file provides important information about the extension.

## JWT Authentication

JSON Web Token (JWT) authentication is used for secure information transmission between parties. It consists of a header, payload, and signature. The workflow involves user login, token generation, token storage, user verification, and server response.

## Sending Data to the Backend

The extension sends data to the backend using JWT for authentication. An example POST request to the REST API is provided.

## MutationObserver

The MutationObserver interface is utilized to watch for changes in the DOM tree. The process involves selecting the DOM element containing subtitles, creating a MutationObserver, defining a callback function, and storing the captured script.

## Abstract

Minutes to Meeting is an application for generating meeting minutes for Google Meet. The web extension captures real-time subtitles, and the web application generates multilingual meeting summaries using NLP and Google Translate.

## Why Django?

Django, a high-level Python web framework, is chosen for its emphasis on reusability (DRY) and comes with built-in features such as a login system, database connection, and ORM (Object Relational Mapper) for simplified database interactions.

## ORM (Object Relational Mapper)

Django's ORM simplifies interactions with databases, automatically transferring data between databases and objects.

## Getting Started

To set up and run the Minutes_Of_Meetings on your local machine, follow these steps:

1. **Clone the Repository**:

    ```shell
    git clone https://github.com/Akshay1299/Minutes_Of_Meeting.git
    ```

2. **Install Dependencies Frontend (React)**:

    ```shell
    cd frontend
    npm install
    ```

3. **Install Dependencies Backend (Django)**:

    ```shell
    cd backend
    pip install -r requirements.txt
    ```

4. **Database Setup**:
   - Create a database in SQL.
   - Update the database configuration in backend/settings.py.

5. **Run the Application**:

    Frontend (React)

    ```shell
    cd frontend
    npm start
    ```

    Backend (Django)

    ```shell
    cd backend
    python manage.py migrate
    python manage.py runserver
    ```

6. ## Load the Extension

To use the Chrome extension, follow these steps:

1. Open Chrome.
2. Go to [chrome://extensions/](chrome://extensions/).
3. Enable "Developer mode" in the top right.
4. Click "Load unpacked" and select the extension directory in the project.
   

## Conclusion

Minutes to Meeting offers a comprehensive solution for improving virtual meetings, providing real-time transcription, multilingual summaries, and accessibility options. The project leverages a robust tech stack and the features of Django to ensure efficiency and reusability.
