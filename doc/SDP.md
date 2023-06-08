# Automated Email Sender Web Application

# Software Development Plan



# Phase 1: Analysis
### Purpose
	* To develop an automated email sender web application in Python using Flask and integrate with the GPT-3 API for email content generation.
###  Functionality
	* The application should allow users to enter an email recipient's address and a prompt for the email content. The GPT-3 API will be used to generate the email's subject and body based on the 
provided prompt. The application will then send the email to the specified address via the Gmail SMTP server.

### System Specifications
* WebFramework:
	* The application will be built using the Flask web framework.
* Frontend:
	* The frontend will be built using HTML, CSS, and possibly a bit of JavaScript.
* Backend:
	* The backend will use Python and the Flask web framework to handle form submissions, communicate with the GPT-3 API, and send emails through the Gmail SMTP server.
*  Hosting and Domain:
	* The web application will be hosted on a web host (to be determined) and accessible via a custom domain.
### Constraints
* The GPT-3 API isn't free and comes with usage restrictions.
* The email account used must have "Less secure app access" enabled, or an App Password should be generated.
* The GPT-3 API key and email credentials must be handled securely.
### Risk Assessment
* There is a risk of the GPT-3 API key or email credentials being exposed if not stored and handled securely.
* There is a risk of hitting the GPT-3 API usage limits, leading to unexpected costs or service disruptions.
* If used for spamming or sending sensitive data, there could be legal and ethical risks.

# Phase 2: Design

## Functional Requirements:
### 1. User Input

The application should provide a user-friendly interface for collecting the following user inputs:

- **Recipient's Email Address**: An input field should allow the user to enter the recipient's email address. The application should validate this input to ensure it's in a correct email format (e.g., 
username@example.com).

- **Email Content Prompt**: A text area should be provided for the user to input the prompt for generating the email content.
### 2. GPT-3 Integration

Once the user input is provided, the application should interact with the GPT-3 API:

- **API Request**: The application must construct a valid request to the GPT-3 API, including necessary headers, the user prompt, and any required API parameters.

- **API Response Handling**: The application must correctly interpret the API response, extracting the generated content.

### 3. Email Sending

With the generated email content, the application should send an email to the specified recipient:

- **SMTP Configuration**: The application must interface with an SMTP server to send emails, requiring the correct setup of server details, port number, and sender's credentials.

- **Email Composition**: The application should construct a valid email, including the recipient's address, an appropriate subject, and the body containing the generated content.

- **Send Email**: The application should handle the email sending process, ensuring successful delivery or providing clear error messages in case of failure.

### 4. User Feedback

The application should provide feedback to the user:

- **Operation Status**: The application should display a status message on the web page indicating the success or failure of the email sending operation.

## System Architecture:
### 1. Frontend

The frontend is responsible for presenting the user interface and gathering user inputs. It's built using HTML, CSS, and JavaScript:

- **HTML**: Defines the structure and layout of the application's web pages.
- **CSS**: Styles the HTML elements, making the web pages visually appealing.
- **JavaScript**: Handles the dynamic aspects of the interface, including form validation and AJAX calls to the server.

The Frontend sends HTTP requests to the Backend and renders the responses. It's deployed on a web server and accessed by users through their web browsers.

### 2. Backend

The backend is built using Python and the Flask framework. It handles incoming requests from the frontend and interacts with the External APIs. It's comprised of:

- **Routes**: Flask routes receive incoming HTTP requests from the frontend, call the appropriate business logic functions, and return HTTP responses.
- **Business Logic**: This layer takes care of processing the user inputs, interacting with the GPT-3 API to generate email content, and sending the email via the SMTP server.
- **Environment Variables**: The backend will use environment variables to securely store sensitive data like the OpenAI API key and the SMTP server credentials.

The Backend is deployed on a server that can process Python code and handle HTTP requests.

### 3. External APIs

The system interacts with two external services:

- **GPT-3 API**: Used to generate the email content based on the user's input. The API key is stored as an environment variable in the backend for security.
- **SMTP Server**: Used to send emails. The server details and credentials are stored as environment variables in the backend.

