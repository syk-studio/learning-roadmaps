
# Full-Stack Development — Complete Learning Guide

Welcome to full-stack development! A full-stack developer understands how the user interface, backend server, APIs, and database work together to create a complete application.

In this guide, you'll connect your existing HTML, CSS, JavaScript, frontend, backend, and database skills into one practical project.

**Goal:** Build, test, and prepare a full-stack application for deployment.

**Prerequisites:** Complete the previous guides, especially [Frontend Development](05-frontend-development.md), [Backend Development](06-backend-development.md), and [Databases](07-databases.md).

---

## How to Use This Guide

For each step:

1. Watch a relevant lecture.
2. Follow along by building the feature yourself.
3. Practice the concepts independently.
4. Test your work before moving forward.
5. Commit meaningful changes to Git.

**Video-link note:** YouTube links below open topic-specific searches, not individually verified videos. Choose a clear, up-to-date lesson covering the listed topics. Prefer one comprehensive lecture when it covers the requirements; use focused videos for gaps.

**Recommended stack for this guide:**
- Frontend: React
- Backend: Node.js and Express
- Database: PostgreSQL
- API style: REST
- Version control: Git and GitHub

You can substitute other technologies once you understand the fundamentals.

---

## Step 1: Understand Full-Stack Architecture

### Learn

- What frontend, backend, and database layers do
- How browsers communicate with servers
- Client-server architecture
- HTTP requests and responses
- APIs and REST
- JSON as a data-exchange format
- Authentication vs. authorization
- Development vs. production environments

### Watch

- [Full-Stack Web Development Explained](https://www.youtube.com/results?search_query=full+stack+web+development+frontend+backend+database+explained)

### Practice

1. Draw a diagram of a browser, frontend, backend API, and database.
2. Explain what happens when a user signs in.
3. Trace how a product is retrieved from a database and displayed on a page.
4. Explain why a frontend should not connect directly to a private production database.

**Checkpoint:** You can explain how the different layers communicate.

---

## Step 2: Prepare Your Project Structure

### Learn

- Organizing frontend and backend code
- Separating responsibilities
- Environment variables
- Package management
- Git branches and commits
- `.gitignore`
- Development scripts
- Configuration for local development

### Watch

- [React and Node.js Full-Stack Project Setup](https://www.youtube.com/results?search_query=React+Node.js+Express+PostgreSQL+full+stack+project+setup)

### Practice

Create a project structure such as:

```text
fullstack-project/
├── client/
├── server/
├── README.md
└── .gitignore
```

Inside `client`, create your React frontend. Inside `server`, create your Express backend.

### Practice tasks

1. Initialize Git.
2. Add suitable `.gitignore` files or entries.
3. Create separate development scripts for the frontend and backend.
4. Document installation and startup instructions.
5. Ensure `.env` files and credentials are excluded from Git.

**Checkpoint:** You can run the frontend and backend as separate parts of one project.

---

## Step 3: Build the Frontend

### Learn

- React components
- Props and state
- Forms and controlled inputs
- React hooks
- Conditional rendering
- Lists and keys
- Routing
- Loading, success, empty, and error states
- Responsive layouts
- Accessible forms and controls

### Watch

- [React Full Course for Beginners](https://www.youtube.com/results?search_query=React+full+course+for+beginners+components+props+state+hooks+routing)

### Practice

Build the interface for a task management application.

Include:

1. A task list.
2. A form to add a task.
3. Controls to mark tasks complete.
4. A way to filter tasks.
5. A loading indicator.
6. A helpful empty state.
7. Error messages for invalid input.
8. Responsive styling for mobile and desktop.

Initially, use local sample data. You'll connect the application to a real API later.

**Checkpoint:** Your interface works independently and handles user input correctly.

---

## Step 4: Build the Backend API

### Learn

- Node.js and Express
- Routes and HTTP methods
- REST API conventions
- Controllers and middleware
- Request parameters and query parameters
- Request-body validation
- Appropriate HTTP status codes
- Centralized error handling
- Separation of routes, services, and database logic

### Watch

- [Node.js and Express REST API Full Course](https://www.youtube.com/results?search_query=Node.js+Express+REST+API+full+course+validation+middleware+error+handling)

### Practice

Create endpoints for tasks:

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/tasks` | List tasks |
| GET | `/api/tasks/:id` | Retrieve one task |
| POST | `/api/tasks` | Create a task |
| PATCH | `/api/tasks/:id` | Update a task |
| DELETE | `/api/tasks/:id` | Delete a task |

Start with an in-memory array for learning, then replace it with PostgreSQL in the next step.

### Practice tasks

1. Test every endpoint using an API client.
2. Return the appropriate status codes.
3. Validate required fields.
4. Handle requests for nonexistent tasks.
5. Return consistent error responses.

**Checkpoint:** You can build and test a REST API independently of the frontend.

---

## Step 5: Connect the Database

### Learn

- PostgreSQL connection pools
- Database configuration
- SQL queries from backend code
- Parameterized queries
- Database constraints
- CRUD operations
- Database migrations
- Handling connection and query errors
- Data persistence

### Watch

- [Full-Stack React, Express, and PostgreSQL Integration](https://www.youtube.com/results?search_query=React+Express+PostgreSQL+full+stack+CRUD+application)

### Practice

Create a PostgreSQL `tasks` table with fields such as:

- `id`
- `title`
- `description`
- `is_completed`
- `created_at`

Update the backend so every task operation uses PostgreSQL instead of an in-memory array.

### Practice tasks

1. Configure the database connection using environment variables.
2. Create the table through a SQL script or migration.
3. Implement database-backed CRUD endpoints.
4. Use parameterized queries.
5. Verify that tasks remain available after restarting the backend.
6. Handle missing records and database failures.

**Checkpoint:** Your API stores and retrieves persistent data.

---

## Step 6: Connect the Frontend to the API

### Learn

- The Fetch API
- Asynchronous requests and `async`/`await`
- Loading and error states
- JSON serialization and parsing
- Sending POST, PATCH, and DELETE requests
- Handling unsuccessful HTTP responses
- CORS and allowed origins
- Environment-specific API URLs
- Avoiding stale or duplicated UI state

### Watch

- [React Fetch API and Express Backend Integration](https://www.youtube.com/results?search_query=React+fetch+API+Express+backend+integration+tutorial)

### Practice

Replace the frontend's sample task array with API requests.

Example:

```javascript
async function getTasks() {
  const response = await fetch(
    `${import.meta.env.VITE_API_URL}/api/tasks`
  );

  if (!response.ok) {
    throw new Error("Unable to load tasks.");
  }

  return response.json();
}
```

This example assumes a Vite frontend with `VITE_API_URL` configured. Adapt the URL to your environment.

### Practice tasks

1. Load tasks from the backend.
2. Display a loading indicator while waiting.
3. Show an error if the request fails.
4. Create a task through the API.
5. Update and delete tasks.
6. Confirm that the UI reflects successful changes.
7. Configure CORS for the frontend origin instead of allowing arbitrary origins in production.

**Checkpoint:** Users can manage database-backed tasks through the frontend.

---

## Step 7: Add Authentication and Authorization

### Learn

- Authentication vs. authorization
- Registration and sign-in flows
- Password hashing
- Sessions and cookies
- Token-based authentication
- Protected frontend routes
- Protected backend endpoints
- User-specific data access
- Logout and session expiration
- Common authentication vulnerabilities

### Watch

- [Node.js Authentication and Authorization for Beginners](https://www.youtube.com/results?search_query=Node.js+Express+authentication+authorization+password+hashing+sessions+JWT)

### Practice

Add user accounts to your task application.

1. Create a users table.
2. Hash passwords using a suitable password-hashing library.
3. Implement registration and login.
4. Choose a suitable session or token-based authentication strategy.
5. Protect task endpoints.
6. Associate each task with its owner.
7. Ensure users cannot access another user's tasks.
8. Implement logout and appropriate expiration behavior.

### Security requirements

- Never store plaintext passwords.
- Never put private secrets in frontend environment variables.
- Validate authorization on the backend, not only in the UI.
- Use secure cookie settings when using cookie-based sessions.
- Protect cookie-authenticated state-changing requests against CSRF where applicable.
- Use HTTPS in production.
- Never trust a user ID supplied by the client as proof of ownership.

**Checkpoint:** Users can sign in securely and access only the resources they're authorized to use.

---

## Step 8: Improve Validation, Errors, and Security

### Learn

- Client-side vs. server-side validation
- Input sanitization and output encoding
- SQL injection prevention
- Cross-site scripting (XSS)
- CORS configuration
- Rate limiting
- Secure HTTP headers
- Safe error messages
- Dependency updates
- Request-size limits

### Watch

- [Express API Security Best Practices](https://www.youtube.com/results?search_query=Express.js+API+security+input+validation+SQL+injection+rate+limiting)

### Practice

1. Validate request bodies on the server.
2. Reject invalid task titles and malformed IDs.
3. Use parameterized SQL queries.
4. Avoid exposing database credentials and internal stack traces.
5. Configure rate limiting for sensitive endpoints.
6. Review dependencies for known vulnerabilities.
7. Test requests with unexpected and invalid input.

**Checkpoint:** Your application rejects invalid input and follows basic secure-development practices.

---

## Step 9: Test the Full-Stack Application

### Learn

- Unit testing
- Integration testing
- API endpoint testing
- Frontend component testing
- End-to-end testing
- Test databases and fixtures
- Mocking external services
- Regression testing

### Watch

- [Full-Stack Application Testing — React and Node.js](https://www.youtube.com/results?search_query=React+Node.js+Express+API+testing+integration+end+to+end)

### Practice

Write tests for:

1. Task creation with valid data.
2. Rejection of invalid input.
3. Updating and deleting tasks.
4. Authentication and authorization.
5. Access restrictions between users.
6. Database errors.
7. Loading and error states in the frontend.

Use a dedicated test database and keep test data separate from production data.

**Checkpoint:** You can demonstrate that important application features work and security checks are enforced.

---

## Step 10: Improve User Experience and Performance

### Learn

- Responsive design
- Accessibility
- Pagination
- Search and filtering
- Database indexes
- API response sizes
- Avoiding unnecessary frontend requests
- Caching fundamentals
- Frontend code splitting
- Logging and monitoring

### Watch

- [Full-Stack Web Performance Optimization](https://www.youtube.com/results?search_query=full+stack+web+performance+optimization+React+Node.js+PostgreSQL)

### Practice

1. Add search and filtering.
2. Implement pagination for large task lists.
3. Add database indexes when query patterns justify them.
4. Improve keyboard navigation and accessible labels.
5. Measure slow queries and large frontend bundles.
6. Avoid logging passwords, access tokens, or other sensitive data.

**Checkpoint:** Your application remains usable as data grows and works across common screen sizes.

---

## Step 11: Deploy the Application

### Learn

- Build commands
- Hosting frontend and backend services
- Production environment variables
- Managed databases
- HTTPS and custom domains
- Database migrations during deployment
- CORS and allowed origins
- Deployment logs
- Health checks
- Backups and rollback plans

### Watch

- [Deploy React, Node.js, and PostgreSQL](https://www.youtube.com/results?search_query=deploy+React+Node.js+Express+PostgreSQL+full+stack+application)

### Practice

1. Choose suitable hosting for the frontend and backend.
2. Set up a managed PostgreSQL database or another appropriately secured database host.
3. Configure production environment variables.
4. Run database migrations.
5. Configure the frontend's production API URL.
6. Enable HTTPS and restrict CORS to trusted origins.
7. Test registration, login, CRUD operations, and authorization in production.
8. Inspect deployment logs and verify backup procedures.

**Checkpoint:** Your application is accessible online and its essential features work in the deployed environment.

---

## Step 12: Build the Final Project

Build a **Full-Stack Task Management Application** with real authentication and persistent data.

### Required features

- User registration and login
- Secure password handling
- Protected routes and API endpoints
- Create, read, update, and delete tasks
- User-specific task ownership
- PostgreSQL database
- Frontend validation and backend validation
- Loading, success, empty, and error states
- Responsive and accessible interface
- Automated tests for essential functionality
- Deployed frontend and backend
- Documented setup and deployment instructions

### Suggested development order

1. Create the repository and project structure.
2. Build the React interface using sample data.
3. Implement the Express API.
4. Design the PostgreSQL schema.
5. Connect the API to the database.
6. Integrate the frontend with the API.
7. Add authentication and authorization.
8. Implement validation and security protections.
9. Write tests.
10. Improve usability and performance.
11. Deploy the application.
12. Write a complete README with screenshots, architecture, features, and setup steps.

### Optional challenges

- Add task priorities and due dates.
- Add labels and categories.
- Support sorting and pagination.
- Add email notifications.
- Introduce role-based permissions.
- Add a dashboard with task statistics.
- Set up automated deployment.
- Add a basic audit trail for important changes.

**Project completion:** A new user can register, sign in, manage their own tasks, refresh the browser without losing data, and use the deployed application.

---

## Recommended Learning Resources

- [React Documentation](https://react.dev/learn) — frontend development.
- [Node.js Documentation](https://nodejs.org/en/learn) — server-side JavaScript.
- [Express Documentation](https://expressjs.com/) — backend routing and middleware.
- [PostgreSQL Documentation](https://www.postgresql.org/docs/) — database reference.
- [MDN Web Docs](https://developer.mozilla.org/) — web platform fundamentals.
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/) — application security.
- [Vitest Documentation](https://vitest.dev/guide/) — testing JavaScript and TypeScript.
- [Playwright Documentation](https://playwright.dev/docs/intro) — browser-based end-to-end testing.

---

## Final Completion Checklist

- [ ] Explain how frontend, backend, APIs, and databases work together.
- [ ] Set up a maintainable full-stack project structure.
- [ ] Build a responsive React frontend.
- [ ] Implement a REST API using Express.
- [ ] Connect PostgreSQL to the backend.
- [ ] Integrate frontend requests with backend endpoints.
- [ ] Implement authentication and authorization.
- [ ] Validate input and protect sensitive data.
- [ ] Test critical frontend, backend, and database behavior.
- [ ] Improve performance and accessibility.
- [ ] Deploy the application securely.
- [ ] Document the project and publish the repository.

## What's Next?

Continue to [Testing and Deployment](09-testing-and-deployment.md) for a deeper look at automated testing, production releases, CI/CD, monitoring, and reliable deployments.

---

**Remember:** Full-stack development is not about knowing every framework. It is about understanding how the pieces fit together, making sound engineering decisions, and building applications that people can use reliably.
