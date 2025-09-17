# Problem Box

[![Next.js](https://img.shields.io/badge/Next.js-black)](https://nextjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-green)](https://nodejs.org/)

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Environment Variables](#environment-variables)

## Project Overview

**Problem Box** is a web application designed to collect real-world problems from users, enabling innovative software solutions to address them. Built by Rishik Reddy, a passionate Software Developer, this project serves as a platform to spark creativity and solve everyday challenges through technology. Users can submit problems anonymously or with contact details, and submissions are sent to the developer's email for further exploration.

The application is built using **Next.js** for the frontend and backend, with **Nodemailer** for email notifications. It features a clean, responsive UI with a form for problem submissions and a confirmation system for successful submissions.

[Visit Live Project](https://www.rishik.tech/problemBox)

## Features

- **Problem Submission Form**: Users can submit problems with optional name and email fields.
- **Email Notifications**: Submitted problems are sent to the developer via email using Nodemailer.
- **Responsive Design**: Optimized for both desktop and mobile devices.
- **Success Feedback**: Visual confirmation with a checkmark icon upon successful submission.
- **Error Handling**: Displays user-friendly error messages for failed submissions.
- **Reusable Form**: Allows users to submit multiple problems with a reset option.
- **Footer Links**: Quick access to the developer's portfolio, GitHub, LinkedIn, and contact information.

## Technologies Used

- **Frontend**:
  - Next.js, React.js 
  - CSS Modules for styling
  - FontAwesome for icons
- **Backend**:
  - Next.js API Routes
  - Nodemailer for email notifications
- **Runtime**:
  - Node.js 
- **Dependencies**:
  - `@fortawesome/fontawesome`, `@fortawesome/react-fontawesome`, `@fortawesome/free-solid-svg-icons`
  - `nodemailer`

## Installation

To set up the project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/mrishikreddy/Problem-Box-RT6.git
   cd problem-box
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Set Up Environment Variables**:
   Create a `.env.local` file in the root directory and add the following:
   ```env
   EMAIL_USER=your-email@gmail.com
   EMAIL_PASS=your-app-specific-password
   ```
   > **Note**: Use an [App Password](https://support.google.com/accounts/answer/185833) for Gmail if 2FA is enabled.

4. **Run the Development Server**:
   ```bash
   npm run dev
   ```
   The application will be available at `http://localhost:3000`.

## Usage

1. **Access the Application**:
   Open the application in your browser (e.g., `http://localhost:3000` for local development).

2. **Submit a Problem**:
   - Fill out the form with a problem description (required).
   - Optionally provide your name and email.
   - Click the **Submit** button.
   - On success, a confirmation message with a checkmark icon will appear.
   - Click **Submit another problem** to reset the form and submit again.

3. **Error Handling**:
   If submission fails (e.g., due to network issues), an error message will display below the form.

4. **Navigation**:
   - Click **Rishik Tech** in the navbar to visit the developer's portfolio.
   - Use footer links to explore the developer's About page, GitHub, LinkedIn, or send an email.

## API Endpoints

The application includes one API endpoint for handling form submissions:

- **POST `/api/problemBox`**:
  - **Request Body**:
    ```json
    {
      "name": "string (optional)",
      "email": "string (optional)",
      "problem": "string (required)"
    }
    ```
  - **Responses**:
    - `200 OK`: `{ "success": "Message sent successfully" }`
    - `400 Bad Request`: `{ "error": "Problem statement is required" }`
    - `500 Internal Server Error`: `{ "error": "Failed to send email" }`

## Environment Variables

The following environment variables are required:

| Variable      | Description                              | Example Value                  |
|---------------|------------------------------------------|--------------------------------|
| `EMAIL_USER`  | Gmail address for sending emails         | `your-email@gmail.com`         |
| `EMAIL_PASS`  | Gmail App Password for authentication    | `your-app-specific-password`   |

 >**Security Note**: Never commit `.env` files to version control. Use `.gitignore` to exclude them.


Thank you for exploring Problem Box. Let's solve real-world challenges together.
