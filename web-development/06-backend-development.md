
# Backend Development — Complete Learning Guide

Welcome to backend development! The backend is responsible for processing requests, applying business rules, accessing databases, and returning data to frontend applications.

In this guide, you'll learn how servers work, build APIs with Node.js and Express, handle errors, introduce authentication, and develop a backend project.

**Goal:** Build a reliable, secure backend API that can communicate with a frontend application.

**Prerequisites:** Complete the [JavaScript Fundamentals](03-javascript-fundamentals.md), [Git and GitHub](04-git-and-github.md), and [Frontend Development](05-frontend-development.md) guides.

---

## How to Use This Guide

For each step:

1. Watch the recommended lecture or search for a suitable lesson.
2. Write and run the code yourself.
3. Complete the practice tasks.
4. Test your endpoints and inspect the results.
5. Commit meaningful changes to Git.

**Video-link note:** These links open YouTube searches for the relevant topics, not individually verified videos. Choose a clear, up-to-date lecture covering the listed concepts. Prefer one comprehensive lecture per step when it covers everything required.

---

## Step 1: Understand How the Web Works

### Learn

- Client-server architecture
- What a server does
- Requests and responses
- HTTP and HTTPS
- HTTP methods: `GET`, `POST`, `PUT`, `PATCH`, and `DELETE`
- Request headers and response headers
- Status codes such as `200`, `201`, `400`, `401`, `403`, `404`, and `500`
- JSON as a data exchange format
- The difference between frontend and backend responsibilities

### Watch

- [HTTP and Client-Server Architecture for Beginners](https://www.youtube.com/results?search_query=HTTP+client+server+request+response+web+development+beginner)

### Practice

1. Open browser developer tools and inspect the Network tab.
2. Visit a website and examine some requests.
3. Identify request methods, status codes, and response content.
4. Explain what happens when a frontend requests information from a server.

**Checkpoint:** You can describe how a browser communicates with a backend.

---

## Step 2: Learn Node.js Fundamentals

Node.js lets you run JavaScript outside the browser, including on a server.

### Learn

- What Node.js is
- How Node.js differs from browser JavaScript
- Installing and checking Node.js and npm
- Running a JavaScript file with Node
- Using built-in modules
- Understanding npm packages
- The `package.json` file
- Environment variables at a basic level

### Watch

- [Node.js Full Course for Beginners](https://www.youtube.com/results?search_query=Node.js+full+course+for+beginners+npm+modules)

### Practice

Install a current supported Node.js LTS release, then check your versions:

```bash
node --version
npm --version
```

Create a new project:

```bash
mkdir backend-practice
cd backend-practice
npm init -y
```

Create `index.js`:

```javascript
const message = "Hello from Node.js!";
console.log(message);
```

Run it:

```bash
node index.js
```

### Additional practice

1. Import a built-in Node.js module.
2. Read command-line arguments.
3. Create a small reusable module.
4. Install a package using npm and learn how to remove it.

**Checkpoint:** You can run JavaScript with Node.js and manage a basic npm project.

---

## Step 3: Understand Asynchronous JavaScript in Node.js

Server applications frequently handle multiple operations that take time, including database queries and network requests.

### Learn

- The event loop at a conceptual level
- Callbacks
- Promises
- `async` and `await`
- Non-blocking I/O
- Handling rejected promises
- Why CPU-intensive work can block a server
- Reading and writing files asynchronously

### Watch

- [Node.js Async Programming and Event Loop](https://www.youtube.com/results?search_query=Node.js+async+await+promises+event+loop+beginner)

### Practice

1. Read a file asynchronously.
2. Convert a promise-based function to use `async` and `await`.
3. Handle an error from a failed asynchronous operation.
4. Compare a simple synchronous task with an asynchronous task.

**Checkpoint:** You can write asynchronous JavaScript and handle expected failures.

---

## Step 4: Build Your First HTTP Server

### Learn

- Creating a server using Node.js
- Listening on a port
- Handling incoming requests
- Sending responses
- Understanding request URLs and methods
- Setting response headers
- Returning JSON
- Why a development server needs appropriate error handling

### Watch

- [Create an HTTP Server with Node.js](https://www.youtube.com/results?search_query=Node.js+create+HTTP+server+http+module+beginner)

### Practice

Create `server.js`:

```javascript
const http = require("node:http");

const server = http.createServer((req, res) => {
  res.setHeader("Content-Type", "application/json");

  if (req.method === "GET" && req.url === "/") {
    res.writeHead(200);
    res.end(JSON.stringify({ message: "Welcome to the API!" }));
    return;
  }

  res.writeHead(404);
  res.end(JSON.stringify({ error: "Route not found" }));
});

server.listen(3000, () => {
  console.log("Server running at http://localhost:3000");
});
```

Run it:

```bash
node server.js
```

Visit `http://localhost:3000` in your browser.

**Checkpoint:** You can run an HTTP server and return a JSON response.

---

## Step 5: Learn Express.js

Express is a widely used framework for creating Node.js web servers and APIs.

### Learn

- Installing Express
- Creating an Express application
- Defining routes
- Route parameters
- Query parameters
- Request bodies
- Middleware
- Serving JSON
- Organizing routes and controllers
- Development tools such as `nodemon`

### Watch

- [Express.js Full Course for Beginners](https://www.youtube.com/results?search_query=Express.js+full+course+beginner+routes+middleware)

### Practice

Install Express:

```bash
npm install express
```

Create `server.js`:

```javascript
const express = require("express");

const app = express();
const PORT = process.env.PORT || 3000;

app.use(express.json());

app.get("/", (req, res) => {
  res.json({ message: "Welcome to the Express API!" });
});

app.get("/api/health", (req, res) => {
  res.json({ status: "ok" });
});

app.listen(PORT, () => {
  console.log(`Server listening on port ${PORT}`);
});
```

Run it:

```bash
node server.js
```

### Practice tasks

1. Add a `/api/about` route.
2. Create a route that reads a URL parameter.
3. Create a route that reads a query parameter.
4. Return appropriate status codes and JSON responses.

**Checkpoint:** You can create an Express server with several working routes.

---

## Step 6: Build REST APIs and CRUD Operations

CRUD stands for Create, Read, Update, and Delete.

### Learn

- REST API design principles
- Resource-based URLs
- HTTP methods and their purposes
- Request body validation
- Route parameters
- Query parameters
- Appropriate HTTP status codes
- Consistent JSON response formats
- Basic pagination, filtering, and sorting
- The difference between `PUT` and `PATCH`

### Watch

- [REST API and CRUD with Node.js and Express](https://www.youtube.com/results?search_query=Node.js+Express+REST+API+CRUD+complete+tutorial)

### Practice

Create a temporary in-memory API for managing tasks.

Example routes:

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/tasks` | List tasks |
| GET | `/api/tasks/:id` | Get one task |
| POST | `/api/tasks` | Create a task |
| PATCH | `/api/tasks/:id` | Update a task |
| DELETE | `/api/tasks/:id` | Delete a task |

Start with an array of tasks. Validate input and return appropriate errors for invalid data or missing task IDs.

**Important:** In-memory data disappears when the server restarts. This is a learning exercise, not a production storage solution.

**Checkpoint:** You can implement the main CRUD operations and test them using an API client.

---

## Step 7: Middleware, Validation, and Error Handling

### Learn

- What middleware does
- How middleware order affects requests
- Logging requests
- Parsing request bodies
- Validating input
- Centralized error-handling middleware
- Handling unknown routes
- Returning consistent error responses
- Avoiding accidental exposure of internal error details

### Watch

- [Express Middleware and Error Handling](https://www.youtube.com/results?search_query=Express.js+middleware+centralized+error+handling+validation+tutorial)

### Practice

1. Create a request-logging middleware.
2. Validate required fields before creating a resource.
3. Return `400 Bad Request` for invalid input.
4. Return `404 Not Found` for missing resources.
5. Add centralized error handling.
6. Ensure unexpected errors don't expose secrets or internal stack traces to clients.

**Checkpoint:** Your API handles expected errors consistently and doesn't crash on ordinary invalid requests.

---

## Step 8: Databases and Data Persistence

A backend usually stores information in a database rather than relying on temporary in-memory arrays.

### Learn

- Why databases are necessary
- Relational vs. NoSQL databases
- Tables, documents, and records
- Database connections
- CRUD queries
- Data validation and constraints
- Environment-based connection settings
- Database indexes at a basic level
- Why passwords and connection strings must not be committed

### Watch

- [Node.js Database Integration for Beginners](https://www.youtube.com/results?search_query=Node.js+Express+database+integration+PostgreSQL+MongoDB+beginner)

### Practice

Choose one database for your first project:

- **PostgreSQL:** a relational database suitable for structured data and relationships.
- **MongoDB:** a document database that stores records as documents.

Then:

1. Create a database for your application.
2. Connect your Node.js server.
3. Store a new record through an API route.
4. Read the saved records.
5. Update and delete a record.
6. Restart the server and verify that data persists.

Use a supported database driver or ORM/ODM and follow its current documentation.

**Checkpoint:** Your API reads and writes persistent data successfully.

**Next roadmap:** Continue to [Databases](07-databases.md) for a deeper study of database design and queries.

---

## Step 9: Authentication and Authorization

Authentication verifies who a user is. Authorization determines what that user is allowed to do.

### Learn

- Authentication vs. authorization
- Registration and login workflows
- Password hashing
- Sessions and cookies
- Token-based authentication
- The basics of JSON Web Tokens (JWT)
- Protected routes
- User roles and permissions
- Logout and session invalidation
- Password reset concepts

### Watch

- [Node.js Authentication and Authorization](https://www.youtube.com/results?search_query=Node.js+Express+authentication+authorization+password+hashing+sessions+JWT)

### Practice

Build a learning-only authentication flow that:

1. Accepts registration details.
2. Validates input.
3. Stores passwords using a reputable password-hashing library.
4. Allows users to log in.
5. Protects a private route.
6. Checks whether a user is allowed to access a resource.

**Security requirements**

- Never store plaintext passwords.
- Never hardcode production secrets.
- Use HTTPS in deployed applications.
- Apply secure cookie settings when using cookie-based sessions.
- Validate authorization on the server for every protected resource.
- Use established libraries and follow current security guidance rather than implementing cryptographic systems yourself.

**Checkpoint:** You understand the distinction between authentication and authorization and can protect a basic route.

---

## Step 10: Backend Security Fundamentals

### Learn

- Input validation and sanitization
- SQL injection and safe parameterized queries
- Cross-site scripting (XSS) risks
- Cross-site request forgery (CSRF) risks
- CORS and its purpose
- Rate limiting
- Secure headers
- Secrets and environment variables
- Dependency updates and vulnerability audits
- Least-privilege access
- Logging without exposing sensitive information

### Watch

- [Node.js and Express API Security for Beginners](https://www.youtube.com/results?search_query=Node.js+Express+API+security+OWASP+beginner)

### Practice

1. Validate all user-controlled input.
2. Use parameterized database queries or safe ORM methods.
3. Configure CORS for the frontend origins that need access.
4. Add rate limiting to sensitive endpoints.
5. Store secrets in environment variables or an appropriate secrets manager.
6. Review dependencies for known vulnerabilities.
7. Ensure error responses don't expose passwords, tokens, or internal details.

**Checkpoint:** You can identify common API risks and apply basic defensive practices.

---

## Step 11: File Uploads and External Services

This step is optional for a first API but useful for real-world applications.

### Learn

- Handling multipart form data
- Upload size limits
- Validating file types and content
- Safe file naming
- File storage options
- Calling external APIs
- API keys and secrets
- Network timeouts and retries
- Why untrusted uploads need special care

### Watch

- [Node.js File Uploads and External APIs](https://www.youtube.com/results?search_query=Node.js+Express+file+upload+external+API+beginner+tutorial)

### Practice

1. Call a public API from your backend.
2. Add a timeout and handle failed requests.
3. If implementing file uploads, limit size and validate accepted formats.
4. Avoid placing private API keys in frontend code.
5. Store uploaded files in an appropriate storage service rather than trusting arbitrary filenames.

**Checkpoint:** You can integrate an external service and understand the basic risks of handling uploads.

---

## Step 12: Testing Backend APIs

### Learn

- Why API tests matter
- Unit tests vs. integration tests
- Testing route status codes
- Testing response bodies
- Testing invalid input
- Testing authentication and authorization
- Using a test database
- Avoiding destructive operations against production data

### Watch

- [Node.js API Testing with Jest and Supertest](https://www.youtube.com/results?search_query=Node.js+Express+API+testing+Jest+Supertest+beginner)

### Practice

1. Write a test for a health endpoint.
2. Test a successful resource-creation request.
3. Test invalid input.
4. Test a missing resource.
5. Test access to a protected route.
6. Run tests automatically before merging important changes.

Use current compatible testing tools and follow their official documentation.

**Checkpoint:** You can verify normal API behavior and important failure cases through automated tests.

---

## Step 13: Environment Configuration and Deployment

### Learn

- Development, testing, and production environments
- Environment variables
- Port configuration
- Production start scripts
- Logging and monitoring
- Health-check endpoints
- Database migrations
- HTTPS and domain configuration
- Deployment platforms
- Why local development settings may differ from production

### Watch

- [Deploy a Node.js Express API](https://www.youtube.com/results?search_query=deploy+Node.js+Express+REST+API+production+beginner)

### Practice

1. Add a production start script to `package.json`.
2. Move secrets and environment-specific settings out of source code.
3. Configure a production database.
4. Deploy your API to a suitable hosting platform.
5. Test its public health endpoint.
6. Inspect logs and troubleshoot one deployment issue.
7. Document required environment variables without publishing their secret values.

**Checkpoint:** Your backend runs outside your local machine and can be monitored and maintained.

---

## Step 14: Build a Complete Backend Project

Build a **Task Management API** that combines the concepts from this guide.

### Required features

- REST API endpoints for tasks
- CRUD operations
- Persistent database storage
- Input validation
- Consistent error responses
- User registration and login
- Password hashing
- Authentication-protected routes
- Authorization so users can access only their own tasks
- Pagination or filtering
- Automated tests
- Environment-based configuration
- Deployment
- API documentation

### Suggested development order

1. Initialize the project and configure Git.
2. Create the Express server and health endpoint.
3. Design the task resource and routes.
4. Add input validation and error handling.
5. Connect the database.
6. Implement task CRUD operations.
7. Add authentication and authorization.
8. Write tests for successful and failed requests.
9. Document the API.
10. Deploy the backend.
11. Connect it to a frontend application.
12. Update the README with setup instructions and example requests.

### Optional challenges

- Add task priorities and due dates.
- Add search and sorting.
- Add rate limiting.
- Add email notifications through a legitimate email service.
- Add an automated deployment workflow.
- Add request IDs and structured logging.

**Project completion:** You can explain your API design, demonstrate its endpoints, verify authorization, run tests, and deploy it without blindly copying a tutorial.

---

## Recommended Learning Resources

- [Node.js Official Documentation](https://nodejs.org/en/learn) — Node.js learning materials.
- [Express Documentation](https://expressjs.com/) — routing, middleware, and application setup.
- [MDN HTTP Overview](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview) — understand HTTP.
- [OWASP Top 10](https://owasp.org/www-project-top-ten/) — common application security risks.
- [OWASP API Security Project](https://owasp.org/www-project-api-security/) — risks specific to APIs.
- [PostgreSQL Documentation](https://www.postgresql.org/docs/) — relational database reference.
- [MongoDB Documentation](https://www.mongodb.com/docs/) — document database reference.
- [npm Documentation](https://docs.npmjs.com/) — package management.

---

## Final Completion Checklist

- [ ] Explain client-server architecture and HTTP.
- [ ] Run JavaScript with Node.js.
- [ ] Create an HTTP server.
- [ ] Build an Express application with routes and middleware.
- [ ] Design and test CRUD API endpoints.
- [ ] Validate requests and handle errors.
- [ ] Connect a database and persist data.
- [ ] Understand authentication and authorization.
- [ ] Apply fundamental API security practices.
- [ ] Write automated API tests.
- [ ] Configure and deploy a backend application.
- [ ] Document and demonstrate the Task Management API.
- [ ] Connect the API to a frontend application.

## What's Next?

Continue to [Databases](07-databases.md) to learn how to model, query, and manage data effectively.

---

**Remember:** A working endpoint is only the beginning. A good backend also validates data, protects user information, handles errors, tests important behavior, and remains maintainable.
