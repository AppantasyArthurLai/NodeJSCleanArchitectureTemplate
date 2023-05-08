# NodeJS Clean Architecture Template

This repository is a boilerplate for building scalable Express applications using Clean Architecture. It offers a well-organized structure, separating concerns into logical components like controllers, domain logic, and services. This template streamlines the development of robust web applications with built-in testing and configuration management.

## 1. Directory Structure

The project is structured as follows:

``` console
my-express-app/
│
├── src/
│   ├── config/            # Contains application configurations, such as database connections and environment variables
│   ├── controllers/       # Contains controllers related to routes and HTTP requests/responses
│   ├── domain/            # Contains the core logic and entities of the application (e.g., business logic, models)
│   ├── use_cases/         # Contains logic for implementing specific features (use cases)
│   ├── repositories/      # Contains data access abstractions for accessing databases or other external data sources
│   ├── services/          # Contains code related to external services, such as sending emails, payment processing, etc.
│   ├── middleware/        # Contains middleware, such as authentication, authorization, and error handling
│   ├── helpers/           # Contains various helper functions and utilities
│   └── app.js             # The main entry point of the application
│
├── tests/
│   ├── controllers/       # Controller tests
│   ├── domain/            # Domain logic tests
│   ├── use_cases/         # Use case tests
│   ├── repositories/      # Data access logic tests
│   └── services/          # Service tests
│
├── .env                   # File for storing environment variables
├── .gitignore             # Git ignore rules
├── package.json           # Contains project dependencies and metadata
└── README.md              # Project documentation
```

## 2. Usage

To use this template for your own project, follow these steps:

1. Clone the repository into your desired project directory (replace `my-express-app` with your preferred directory name): `git clone https://github.com/AppantasyArthurLai/NodeJSCleanArchitectureTemplate.git my-express-app`
2. Navigate to the project directory: `cd my-express-app`
3. Remove the original remote and add your own repository as the new remote origin: 
``` console
git remote remove origin
git remote add origin https://github.com/yourusername/your-repo.git
```
4. Install dependencies: `npm install`
5. Create a `.env` file and configure the required environment variables.
6. Start the development server: `npm run dev`
7. Run tests: `npm test`


## 3. Changelog

### v1.0.0 (2023-05-08)

- Initial release

## 4. Contributors

- [Arthur Lai](https://github.com/AppantasyArthurLai)

## 5. License

This project is open-sourced under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use, modify, and distribute the code as you see fit, according to the terms of the license.
