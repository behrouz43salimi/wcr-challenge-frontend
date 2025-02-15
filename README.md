# WCR Challenge Front-end

Inspired by the established WCR website, this app maintains a consistent visual identity by adopting the site's color scheme and title font, Rokkitt from Material Design 3. This design choice mirrors the website’s look and feel, ensuring brand continuity across platforms.

Built with modern technologies—Angular 19, Ionic, and CapacitorJS—and fully Dockerized, the mobile application adheres to Material Design 3 principles for a clean and responsive interface. It features engaging interactive 3D Spline animations and intuitive tabbed authentication flows for Sign Up and Login. Leveraging Angular Material components, the app delivers a seamless cross-platform experience on both iOS and Android devices.

## Table of Contents
- [Features](#features)
- [Technologies & Dependencies](#technologies--dependencies)
- [Setup Instructions](#setup-instructions)
- [Implementation Details](#implementation-details)
- [Dependency Rationale](#dependency-rationale)
- [Simplification Techniques](#simplification-techniques)
- [Known Issues & Limitations](#known-issues--limitations)
- [Resources & Credits](#resources--credits)

## Features

### Interactive Spline Animation
An engaging 3D animation integrated on the Login & Signup page using Spline.

### Tabbed Authentication
- **Sign Up Tab:** New user registration with Google and Facebook SSO styled buttons.
- **Login Tab:** Existing user authentication with Google and Facebook SSO styled buttons.

### Swagger API Integration
Simplified integration for user authentication via provided Swagger endpoints.

### Responsive Design
Adheres to Material Design 3 guidelines for a clean, responsive UI.

### Cross-Platform Support
Ensured through Ionic and CapacitorJS for seamless performance on both iOS and Android.

### Containerization
Dockerized environment for easy deployment and consistency across different setups.

## Technologies & Dependencies

- **Angular 19:** Application framework.
- **Angular Material 19:** UI components following Material Design 3 guidelines.
- **Ionic & CapacitorJS:** Cross-platform mobile compatibility.
- **Spline:** For creating interactive 3D web animations.
- **Docker:** Containerization for deployment.
- **Swagger JSON Integration:** For simplified user authentication APIs.

## Setup Instructions

### Prerequisites
- Node.js (version 16 or above)
- Angular CLI (v18+)
- Docker
- Git

### Local Development Setup
1. **Clone the Repository:**
    ```bash
    git clone https://github.com/homayoun43salimi/wcr-challenge-frontend.git
    cd wcr-challenge-frontend
    ```

### Docker Deployment

#### Backend
1. **Build the Docker Image of Backend:**
    - Navigate to the Backend folder within the cloned repository.
    ```bash
    docker build -t wcr-challenge .
    ```
2. **Run the Image:**
    ```bash
    docker run -d -p 3030:3030 wcr-challenge
    ```

#### Frontend
1. **Build the Docker Image of Frontend:**
    - Navigate to the Frontend folder within the cloned repository.
   ```bash
   npm run build
   ```
    ```bash
    docker build -t wcr-challenge-fe .
    ```
2. **Run the Image:**
    ```bash
    docker run --name wcr-challenge-fe -p 80:80 --network bridge wcr-challenge-fe
    ```

### Usage and Docs
Find Back-end in : 
https://github.com/WECANRACE/wcr-challenge-backend


**API KEY:**
I'M_A_FRONTEND_DEVELOPER_AND_I_WANT_TO_JOIN_THE_TEAM

**Email:**
new_frontend_developer@wecanrace.it

**Password:**
A_TUTTO_GAS_!

### Running the App

#### Using Docker
Open [http://localhost:80](http://localhost:80) in your browser to test the app.

#### Using Angular CLI
```bash
cd your-frontend-path
ng serve
```

Then visit http://localhost:4200 to test your app

> ⚠️ **Warning:** Ensure the back-end Docker container is running before starting the front-end container to guarantee proper functionality.


## Implementation Details

### Interactive Animation
The animation component (located in src/app/components.ts) uses Spline’s API to embed and control a 3D interactive animation on the Welcome page.

### Tabbed Authentication Section
#### Utilizing Angular Material Tabs located in src/app/login & src/app/signup, the application offers:

Two tabs: "Sign Up" and "Login".
Each tab contains a form for user input and Google/Facebook SSO styled buttons.
Calls to the Swagger API for authentication are handled by AuthService in src/app/login/login.component.ts & src/app/signup/signup.component.ts.

### Authentication Flow
The AuthService abstracts HTTP calls to the Swagger API endpoints, managing login and signup logic. This includes simplified error handling and basic form validation for a streamlined user experience.

# Dependency Rationale

### Angular & Angular Material: 
Provide a structured framework and pre-built UI components adhering to Material Design 3, reducing the need for custom UI work.
### Ionic & CapacitorJS:
Facilitate cross-platform mobile development, allowing the Angular web app to run natively on iOS and Android.
### Spline: 
Enhances the user experience with modern, interactive 3D animations without requiring heavy custom code.
### Docker: 
Ensures consistency across development, testing, and production environments, simplifying deployment.

# Simplification Techniques

#### Leveraged Angular Material components to minimize custom UI code.
#### Integrated Swagger APIs directly using Angular’s HTTP client, reducing complexity in API integration.
#### Employed Docker to encapsulate environment dependencies, eliminating local setup issues.
#### Used Ionic components and CapacitorJS to streamline mobile compatibility, avoiding the need for separate codebases.

# Known Issues & Limitations

### SSO Buttons: 
Currently non-functional stubs; they are styled to match Google and Facebook branding but do not perform actual OAuth flows.
### Swagger Integration: 
Simplified; advanced error handling, token management, and security considerations are minimal.
### Animation Performance: 
May vary across devices, particularly on older models with limited hardware capabilities.

# Resources & Credits

### WECANRACE Website
### Material Design 3 Guidelines
### Figma
https://www.figma.com/design/cZF1amxpx8sVcWnkg3rODq/Untitled?node-id=0-1&t=g7Zjmuc08hNeW7WI-1
### Angular Documentation
### Angular Material
### Ionic Framework
### CapacitorJS
### Spline
### Swagger API Documentation
### ChatGPT & Gemini
https://chatgpt.com/share/6788c31d-6aa0-8006-a09d-08b38fe67647
https://gemini.google.com/app/3cabbe085f7ac9ac
https://gemini.google.com/app/a14f75c619fcc32c
https://gemini.google.com/app/40e3606adcafa955
https://gemini.google.com/app/dd6a16600e265f1e



