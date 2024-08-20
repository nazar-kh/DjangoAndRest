# Minute Marketing (Backend)
Author : `[Nazar Hussain]`
Email: `[nazar@zaltechapps.com]`
GitHub: https://github.com/nazar-kh

## Overview

This Django application is designed to restful backend apis for zaltechapps. It includes features such as companies registration, botmodules modules android/ios application integrations and generative ai implementations. This guide will help you set up the development environment, run the application, and configure it for your needs.

## Table of Contents

1. [Installation](#installation)
2. [Setup](#setup)
3. [Environment Setup](#environment-setup)
4. [Usage](#usage)
5. [Configuration](#configuration)
6. [Testing](#testing)
7. [Contributing](#contributing)
8. [License](#license)
9. [Author](#author)

## Installation

### Prerequisites

- Python 3.11 or later
- pip (Python package installer)
- Git

### Clone the Repository

Start by cloning the repository to your local machine:

```bash
https://github.com/nazar-kh/DjangoAndRest.git
cd MinuteMarketing
```

### Create a Virtual Environment
It’s recommended to use a virtual environment to manage project dependencies:
```bash
python -m venv venv
source venv/bin/activate
```
### Install Dependencies
Install the required Python packages listed in `requirements.txt`:
```bash
pip install -r requirements.txt
```
## Setup
### Environment Variables
Create a `.env` file in the root directory of the project with the following environment variables:

```dotenv
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=your-database-url
```
Replace your-secret-key with a secure, unique key and your-database-url with the connection string for your database.

### Database Migration
Apply the initial database migrations to set up the database schema:
```bash
python manage.py makemigrations
python manage.py migrate
```
### Create a Superuser
Create an admin user to access the Django admin interface:
```bash
python manage.py createsuperuser
```
Follow the prompts to enter a username, email, and password.

## Environment Setup
### Configuring Environment
Ensure that your `.env` file is correctly configured. You may need to adjust settings based on your development or production environment. Common adjustments include database settings and debugging options.

### Required Packages
If you need to update or add packages, modify requirements.txt and install them:
```bash
pip freeze > requirements.txt
```
If using Docker, follow the instructions in Dockerfile and docker-compose.yml to build and run the application in a containerized environment.

## Usage
### Run the Development Server
Start the Django development server to test the application locally:
```bash
python manage.py runserver
```
Navigate to http://127.0.0.1:8000/ in your web browser to view the application.

### Admin Interface
To access the Django admin interface, go to http://127.0.0.1:8000/admin/ and log in using the superuser credentials you created.

## Configuration
### Settings
Update the `settings.py` file to configure additional options such as allowed hosts, static files, and security settings. For production, ensure the following settings are properly configured:

*   ALLOWED_HOSTS - List of allowed hosts.
*   STATIC_ROOT - Directory for collected static files.
*   MEDIA_ROOT - Directory for media file uploads.

### Static and Media Files
Ensure that your `settings.py` file includes configuration for static and media files:

```python
STATIC_URL = '/static/'
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')

MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```
Create directories for static and media files if they don’t already exist:
```bash
mkdir staticfiles media
```
## Testing
### Run Tests
To run the test suite and ensure that your application works as expected, use the following command:
```bash
python manage.py test
```
## Contributing

We welcome contributions to this project! To contribute:

1.  Fork the repository on GitHub.
2.  Create a new branch for your feature or bugfix (`git checkout -b feature/your-feature`). 
3. Make your changes and commit them (`git commit -am 'Add some feature'`). 
4. Push your branch to GitHub (`git push origin feature/your-feature`). 
5. Create a `pull request` to merge your changes into the main repository.

## License
This project is sole property of *ZaltechApps.com*

## Contributors 
For any questions or feedback, feel free to reach out via email.
