# Software Development Plan

## Project Name
Automated Email Sender Web Application

## Project Objectives and Requirements
*Purpose
	*To develop an automated email sender web application in Python using Flask and integrate with the GPT-3 API for email content generation.
*Functionality
	*The application should allow users to enter an email recipient's address and a prompt for the email content. The GPT-3 API will be used to generate the email's subject and body based on the 
provided prompt. The application will then send the email to the specified address via the Gmail SMTP server.

## System Specifications
* WebFramework
	*The application will be built using the Flask web framework.
*Frontend:
	*The frontend will be built using HTML, CSS, and possibly a bit of JavaScript.
*Backend:
	*The backend will use Python and the Flask web framework to handle form submissions, communicate with the GPT-3 API, and send emails through the Gmail SMTP server.
*Hosting and Domain:
	*The web application will be hosted on a web host (to be determined) and accessible via a custom domain.
## Constraints
*The GPT-3 API isn't free and comes with usage restrictions.
*The email account used must have "Less secure app access" enabled, or an App Password should be generated.
*The GPT-3 API key and email credentials must be handled securely.
## Risk Assessment
*There is a risk of the GPT-3 API key or email credentials being exposed if not stored and handled securely.
*There is a risk of hitting the GPT-3 API usage limits, leading to unexpected costs or service disruptions.
*If used for spamming or sending sensitive data, there could be legal and ethical risks.
