# FastapiOAuth

This is a minimal example of implementing Google OAuth 2.0 authentication in a Fastapi web application using the Authlib package.

## Features

* Google OAuth login via /login
* OAuth callback handling at /auth
* Session management using starlette
* Simple user profile display after login
* Logout support at /logout

## Requirements

* python 3
* Google Cloud Project with OAuth 2.0 credentials
* Environment variables set in .env

## Setup
### 1. Clone the repository

```
git clone https://github.com/paulebil/FastapiOAuth.git

cd FastapiOAuth

pip install -r requirements.txt
```
### 2. Create .env file
Create a .env file in the project root with your Google OAuth credentials:
````
GOOGLE_CLIENT_ID=your-google-client-id.apps.googleusercontent.com
GOOGLE_CLIENT_SECRET=your-google-client-secret
````

### 3. Register Redirect URI in Google Console
Set the authorized redirect URI to:
````
http://localhost:8000/auth
````

Run the Application
```
python main.go

```
Visit http://localhost:8000 and click Login with Google.