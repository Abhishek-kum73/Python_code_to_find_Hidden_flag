Web Login Automation Script

This project demonstrates how to automate and replicate a custom authentication process by reverse-engineering a login API. The script generates a valid auth_token, timestamp, and signature required by the server, and sends a POST request to authenticate successfully.

Features

Generates Base64-encoded auth_token in the format username::password

Creates a real-time UNIX timestamp

Builds a valid MD5-based signature using:
MD5(auth_token + timestamp + app_secret)

Sends a structured login request to the server

Displays server response with authentication status

How It Works

The authentication mechanism requires:

auth_token — Base64 encoding of username::password

timestamp — Current UNIX time

signature — MD5 hash combining the token, timestamp, and secret salt

The script reconstructs this logic and submits the correct payload to the endpoint.

Usage
Install Dependencies
pip install requests

Run the Script
python exploit.py

Output Example

The script prints the generated payload and server response, which includes the authentication message and flag (if valid).

Disclaimer

This project is intended only for learning, CTF challenges, and authorized security testing. Do not use this script on systems without permission.
