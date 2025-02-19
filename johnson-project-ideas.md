# Johnson Project Ideas

## Prompt 1

**Prompt:**
What are good small projects that would allow me to demonstrate pytest for unit and integration testing, postman, selenium, playwright and robot framework testing. It needs to be able to be modularized so that 3 - 6 people can work on it and minimize having version control conflict using GitHub. The project needs to have at least 3 internal apis and use a free public one. The selenium needs to be able to test at least 6 of the following in the ui: Form Submissions: Test form filling, submissions, and validation messages. - Link and Button Clicks: Automate clicking on various links and buttons to ensure they lead to the correct actions or pages. - Dropdown Menus: Test interactions with dropdown menus, including selecting various options. - Mouse Actions: Simulate mouse actions like clicks, double-clicks, hover, and drag-and-drop. - Keyboard Inputs: Test keyboard interactions, including text input and keyboard shortcuts. - Layout Testing: Check the layout and positioning of UI components. - Page Navigation: Test navigation between different pages or sections of the application. - Data Entry and Retrieval: Test CRUD (Create, Read, Update, Delete) operations on data. - Data Validation: Ensure the correctness of data processing and output. - Error Messages: Test for correct error messages under various error conditions. - Handling Exceptions: Ensure the application handles unexpected exceptions gracefully.
**Response:**
A **Task Management System** would be a suitable project. It would allow users to create, update, delete, and manage tasks while integrating authentication and feedback systems. The backend would expose APIs for user management, task handling, and feedback. The UI would enable interactions such as form submissions, CRUD operations, and navigation testing. A free public API, such as a weather API, could be integrated for additional task planning features.

---

## Prompt 2

**Prompt:**
Create a project plan and structure for this

**Response:**
The project will be structured as follows:

```
project-root/
│-- app/
│   ├── models/
│   │   ├── user_model.py
│   │   ├── task_model.py
│   │   ├── feedback_model.py
│   ├── routes/
│   │   ├── user_routes.py
│   │   ├── task_routes.py
│   │   ├── feedback_routes.py
│   ├── static/
│   ├── templates/
│   ├── utils/
│   │   ├── database.py
│   │   ├── validators.py
│-- tests/
│   ├── unit/
│   │   ├── test_users.py
│   │   ├── test_tasks.py
│   ├── integration/
│   │   ├── test_api.py
│   ├── ui/
│   │   ├── test_selenium.py
│-- requirements.txt
│-- README.md
```

---

## Prompt 3

**Prompt:**
Break out the backend more so they can work and use Flask to develop with Python.

**Response:**
The backend will be modularized into individual microservices:
- **User Service**: Handles authentication and user management.
- **Task Service**: Manages tasks and their statuses.
- **Feedback Service**: Stores and retrieves feedback from users.
- **API Gateway**: Routes requests to appropriate services.

---

## Prompt 4

**Prompt:**
Revise to complete in 4 sprints, with each sprint being two weeks.

**Response:**
- **Sprint 1:** Set up project structure, user authentication, and initial database schema.
- **Sprint 2:** Implement task management API and UI elements.
- **Sprint 3:** Develop feedback system, complete integration, and testing.
- **Sprint 4:** Conduct UI automation testing and finalize documentation.

---

## Prompt 5

**Prompt:**
Create a detailed test plan with test cases.

**Response:**
- **Unit Tests:** Pytest for user authentication, task handling, and feedback.
- **Integration Tests:** Postman and pytest for API endpoint validation.
- **UI Tests:** Selenium and Playwright for:
  - Form submissions
  - Link and button clicks
  - Dropdown interactions
  - Mouse actions (hover, drag and drop)
  - Keyboard inputs
  - Page navigation

---

## Reflection

### Learning Outcomes
Through this assignment, I explored software design principles, including maintainability, scalability, and testability. The modular architecture helped in minimizing version control conflicts, and dependency injection facilitated better testability. AI-assisted collaboration provided structured project breakdowns and efficient task delegation.

### Challenges Faced
One major challenge was structuring the backend to enable parallel development while ensuring smooth integration. Defining clear responsibilities for different team members and maintaining synchronization was another challenge, especially when handling interdependent modules.

### Personal Growth
This assignment deepened my understanding of structured planning and test-driven development. It also highlighted the importance of designing modular and scalable applications, preparing me for real-world software development practices.

