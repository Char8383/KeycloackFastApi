# Keycloak FastAPI Integration

![Keycloak FastAPI](https://img.shields.io/badge/Keycloak-FastAPI-blue?style=for-the-badge&logo=python&logoColor=white)

Welcome to the **Keycloak FastAPI** repository! This project combines the power of Keycloak, an open-source Identity and Access Management (IAM) solution developed by Red Hat, with FastAPI, a modern web framework for building APIs with Python. This README will guide you through the setup, usage, and features of this project.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [API Endpoints](#api-endpoints)
6. [Contributing](#contributing)
7. [License](#license)
8. [Releases](#releases)

## Introduction

Keycloak provides a robust solution for managing user identities and access control. By integrating it with FastAPI, developers can create secure APIs quickly and efficiently. This project aims to simplify the setup process and provide a clear example of how to use Keycloak with FastAPI.

## Features

- **Easy Integration**: Seamlessly connect FastAPI with Keycloak for user authentication.
- **JWT Support**: Utilize JSON Web Tokens for secure API access.
- **Role-Based Access Control**: Manage user roles and permissions effectively.
- **SQLite Database**: Store user data and application settings in a lightweight SQLite database.
- **RESTful API**: Follow REST principles for clear and consistent API design.
- **Comprehensive Documentation**: Clear guidelines on setup and usage.

## Installation

To get started, you need to have Python 3.6 or higher installed on your machine. Follow these steps to set up the project:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Char8383/KeycloackFastApi.git
   cd KeycloackFastApi
   ```

2. **Create a Virtual Environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set Up Keycloak**:
   - Download and install Keycloak from the [official website](https://www.keycloak.org/downloads).
   - Start the Keycloak server and create a new realm, client, and user as per your application needs.

5. **Configure FastAPI**:
   - Update the configuration file with your Keycloak server details.
   - Ensure the FastAPI application can connect to Keycloak.

## Usage

Once you have completed the installation, you can start the FastAPI server:

```bash
uvicorn main:app --reload
```

Visit `http://127.0.0.1:8000/docs` to access the automatically generated API documentation. This will give you an overview of all available endpoints.

### Authentication Flow

1. **Login**: Use the `/login` endpoint to authenticate users against Keycloak.
2. **Access Protected Routes**: After successful login, users can access protected routes using the JWT token received.

## API Endpoints

### Authentication

- **POST /login**
  - Description: Authenticates a user with Keycloak.
  - Request Body:
    ```json
    {
      "username": "user",
      "password": "pass"
    }
    ```

- **GET /protected**
  - Description: Access a protected resource.
  - Headers:
    ```
    Authorization: Bearer <JWT_TOKEN>
    ```

### User Management

- **GET /users**
  - Description: Retrieves a list of users.
  - Authentication required.

- **POST /users**
  - Description: Creates a new user.
  - Request Body:
    ```json
    {
      "username": "new_user",
      "password": "new_pass"
    }
    ```

## Contributing

We welcome contributions to enhance the functionality of this project. To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

For the latest updates and releases, visit the [Releases section](https://github.com/Char8383/KeycloackFastApi/releases). Here, you can download and execute the latest version of the project.

## Conclusion

Thank you for checking out the Keycloak FastAPI project. We hope this repository helps you implement secure APIs with ease. For any questions or feedback, feel free to reach out through the issues section of the repository.

![Keycloak](https://img.shields.io/badge/Keycloak-Integration-orange?style=for-the-badge&logo=redhat&logoColor=white)

Remember to visit the [Releases section](https://github.com/Char8383/KeycloackFastApi/releases) for updates. Happy coding!