# Go Web Server

This project is a basic web server written in Go. It demonstrates how to handle HTTP requests, serve static files, and create custom handlers for specific routes.

## Project Overview

The web server provides the following functionalities:
- Serves static files from the `./static` directory.
- Handles form submissions through a `/form` endpoint.
- Responds to a simple GET request at the `/hello` endpoint.

## Features

1. **Static File Server**:
   - The root path (`/`) serves static files from the `./static` directory.
   - This is useful for serving HTML, CSS, JavaScript, images, and other assets.

2. **Form Handling**:
   - The `/form` endpoint accepts POST requests and parses form data.
   - It extracts `name` and `address` from the form submission and responds with the provided values.

3. **Hello Handler**:
   - The `/hello` endpoint accepts GET requests.
   - It responds with a simple "Hello!" message.
   - If the path is incorrect or a method other than GET is used, an appropriate HTTP error is returned.

### Main Components

- **`formHandler` Function**:
  - Parses form data and extracts values for `name` and `address`.
  - Responds with the parsed data or an error message if parsing fails.

- **`helloHandler` Function**:
  - Handles requests to the `/hello` path.
  - Returns a "Hello!" response for GET requests and a 404 or method-not-allowed response for other cases.

- **`main` Function**:
  - Sets up the file server and maps the endpoints to their respective handler functions.
  - Starts the server on port 8080.
