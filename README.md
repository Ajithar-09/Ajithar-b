# Backend Email Service

This is a Node.js backend using Express and Nodemailer to send emails via Gmail.

## Prerequisites

- Node.js (v14 or later recommended)
- npm (Node Package Manager)

## Installation

1.  Clone the repository or download the source code.
2.  Install dependencies:
    ```bash
    npm install
    ```

## Configuration

1.  Create a `.env` file in the root directory (if it doesn't already exist).
2.  Add your Gmail credentials:
    ```env
    GMAIL_USER=your-email@gmail.com
    GMAIL_PASS=your-app-password
    PORT=5000
    ```

    > **Note:** Use an **App Password**, not your regular Gmail password. You can generate one in your Google Account settings under Security > 2-Step Verification > App passwords.

## Running the Server

Start the server processing:
```bash
npm start
```
The server will run on port 5000 by default.

## API Endpoints

### 1. Test Server
Check if the server is running.
- **URL**: `http://localhost:5000/test`
- **Method**: `GET`
- **Response**:
  ```json
  {
    "success": true,
    "message": "Server is running perfectly!",
    "timestamp": "..."
  }
  ```

### 2. Send Message
Send an email using the configured Gmail account.
- **URL**: `http://localhost:5000/send-message`
- **Method**: `POST`
- **Body** (JSON):
  ```json
  {
      "name": "John Doe",
      "email": "johndoe@example.com",
      "subject": "Inquiry",
      "message": "I would like to know more about your services."
  }
  ```
- **Success Response**:
  ```json
  {
      "success": true,
      "message": "Message sent successfully!"
  }
  ```
