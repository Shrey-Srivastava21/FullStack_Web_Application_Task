
---

# Assessment Management System

This project is a full-stack web application built using Node.js, Angular, and MongoDB. The application is designed to manage assessments, including accounts, questions, and candidates. The backend is powered by Node.js with Express, and MongoDB is used as the database. The frontend is a Single Page Application (SPA) built with Angular and Angular Material.

## Features

### Backend (Node.js, Express, MongoDB)
- **CRUD Operations**: 
  - Manage accounts, questions, and candidates with RESTful APIs.
- **Authentication & Authorization**: 
  - Basic role-based access control with roles like Admin and Delivery Admin.
- **Pagination**: 
  - Implemented for listing questions and candidates.
- **Error Handling**: 
  - Graceful handling of errors with appropriate HTTP status codes.
- **Filtering & Searching**: 
  - Filter and search questions by tags, text, and key fields.
- **Role Management**: 
  - Admin can access and manage questions and candidates, while Delivery Admin can only manage candidates.

### Frontend (Angular)
- **Single Page Application**: 
  - Built with Angular and Angular Material for a responsive and user-friendly interface.
- **Role-Based Access Control**: 
  - Different views and permissions for Admin and Delivery Admin.
- **Question Management**: 
  - View, add, edit, and delete questions with an integrated editor.
- **Candidate Management**: 
  - View and manage candidates with sorting and filtering options.
- **Routing & Navigation**: 
  - Seamless navigation between different views using Angular routing.
- **Asynchronous Operations**: 
  - Proper handling of asynchronous API calls and error responses.
- **Advanced Angular Concepts**: 
  - Implementation of RxJS, lazy loading, and other advanced features.

## Technologies Used

- **Backend**: 
  - Node.js, Express, MongoDB, TypeScript
- **Frontend**: 
  - Angular 15, Angular Material, TinyMCE Editor, RxJS
- **Database**: 
  - MongoDB Atlas (M0 Cluster)

## Project Structure

```bash
├── node-js-server
│   ├── src
│   │   ├── controllers
│   │   ├── models
│   │   ├── routes
│   │   └── services
│   ├── app.ts
│   ├── server.ts
│   └── ...
├── angular-15-client
│   ├── src
│   │   ├── app
│   │   │   ├── components
│   │   │   ├── services
│   │   │   ├── models
│   │   │   ├── guards
│   │   │   └── app.module.ts
│   │   ├── assets
│   │   └── environments
│   ├── angular.json
│   ├── package.json
│   └── ...
└── README.md
```

## Setup Instructions

### Backend (Node.js Server)

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/assessment-management-system.git
   ```

2. **Navigate to the server directory**:
   ```bash
   cd node-js-server
   ```

3. **Install dependencies**:
   ```bash
   npm install
   ```

4. **Create a `.env` file** in the root directory with the following content:
   ```env
   PORT=5000
   MONGO_URI=<Your MongoDB Atlas Connection String>
   JWT_SECRET=<Your JWT Secret>
   ```

5. **Run the server**:
   ```bash
   npm run start
   ```

### Frontend (Angular Client)

1. **Navigate to the client directory**:
   ```bash
   cd angular-15-client
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Run the Angular application**:
   ```bash
   ng serve --port 8081
   ```

4. **Open the application in your browser**:
   ```bash
   http://localhost:8081/
   ```

## API Endpoints

### Authentication
- **POST /api/auth/login**: User login

### Account Management
- **POST /api/accounts**: Create a new account
- **GET /api/accounts/:id**: Get account details
- **PUT /api/accounts/:id**: Update account details
- **DELETE /api/accounts/:id**: Delete an account

### Question Management
- **POST /api/questions**: Create a new question
- **GET /api/questions**: List all questions (with pagination and filtering)
- **GET /api/questions/:id**: Get question details
- **PUT /api/questions/:id**: Update question details
- **DELETE /api/questions/:id**: Delete a question

### Candidate Management
- **POST /api/candidates**: Create a new candidate
- **GET /api/candidates**: List all candidates (with pagination and filtering)
- **GET /api/candidates/:id**: Get candidate details
- **PUT /api/candidates/:id**: Update candidate details
- **DELETE /api/candidates/:id**: Soft delete a candidate

## Role-Based Access Control

- **Admin**:
  - Full access to Question and Candidate modules.
- **Delivery Admin**:
  - Access to Candidate module only.

## Testing

1. **Unit Tests**:
   - Write unit tests using Jest (for Node.js) and Jasmine/Karma (for Angular).
   - Run tests using:
     ```bash
     npm run test
     ```

2. **End-to-End Tests**:
   - Write e2e tests using Protractor for Angular.

## Deployment

- **Backend**: Deploy the Node.js server to a cloud platform like Heroku or AWS.
- **Frontend**: Deploy the Angular application to a static hosting service like Netlify or Vercel.

## Contributing

- Fork the repository.
- Create a new branch (`git checkout -b feature-branch`).
- Commit your changes (`git commit -m 'Add some feature'`).
- Push to the branch (`git push origin feature-branch`).
- Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### Notes

- Ensure the project is well-documented and follows best practices for both Node.js and Angular development.
- Proper commit history should be maintained throughout the development process.

Happy Coding!
