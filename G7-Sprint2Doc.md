# **Sprint 2 Documentation**

## **1. Project Charter**
### **Objectives**
- Goal is to create employee directory management system.
- Centralized Employee management system with user-friendly UI
- Project uses python, MariaDB, and flask.

### **Scope**
- **In-Scope:** Comprehensive building and testing of features such as create users, build and manage databases of employees, error handling, and the UI
- **Out-of-Scope:** Deployment of fully functional system

### **Technologies**
- Backend: [Flask & Python]
- Frontend: [HTML & CSS]
- Database: [MariaDB]
- Other Tools: [Postman, Selenium, CI/CD Pipelines]

---

## **2. User Stories for Employee Management (CRUD Operations)**
| **ID** | **User Story** | **Acceptance Criteria** | **Priority** |
|--------|--------------|----------------------|------------|
| EM-001 | As an admin, I want to create an employee profile so that new hires can be managed in the system. | Given an admin user, when they submit a valid employee form, then a new employee is created in the database. | High |
| EM-002 | As an admin, I want to read employee details so that I can view relevant information. | Given an admin user, when they search for an employee, then the system returns the employee’s details. | High |
| EM-003 | As an admin, I want to update an employee record so that I can modify their details if needed. | Given an admin user, when they update employee data and submit, then the changes are saved in the database. | Medium |
| EM-004 | As an admin, I want to delete an employee record so that outdated records are removed from the system. | Given an admin user, when they delete an employee, then the employee record is permanently removed. | Medium |

---

## **3. API Specifications**
### **Employee Management API Endpoints**
#### **Create Employee**
- **Endpoint:** `POST /api/employees`
- **Request Body:**
```json
{
  "name": "John Doe",
  "email": "johndoe@example.com",
  "position": "Software Engineer",
  "department": "IT"
}
```
- **Response:**
```json
{
  "id": 1,
  "name": "John Doe",
  "email": "johndoe@example.com",
  "position": "Software Engineer",
  "department": "IT",
  "status": "Employee created successfully"
}
```

#### **Read Employee**
- **Endpoint:** `GET /api/employees/{id}`
- **Response:**
```json
{
  "id": 1,
  "name": "John Doe",
  "email": "johndoe@example.com",
  "position": "Software Engineer",
  "department": "IT"
}
```

#### **Update Employee**
- **Endpoint:** `PUT /api/employees/{id}`
- **Request Body:**
```json
{
  "email": "john.doe@company.com"
}
```
- **Response:**
```json
{
  "id": 1,
  "name": "John Doe",
  "email": "john.doe@company.com",
  "position": "Software Engineer",
  "department": "IT",
  "status": "Employee updated successfully"
}
```

#### **Delete Employee**
- **Endpoint:** `DELETE /api/employees/{id}`
- **Response:**
```json
{
  "status": "Employee deleted successfully"
}
```

---

## **4. Sprint Progress Tracking**
| **Task ID** | **Task Description** | **Assigned To** | **Status** | **Estimate** |
|------------|----------------|------------|--------|----------|
| T-101 | Implement Employee Creation API | [Developer] | In Progress | 3 days |
| T-102 | Develop UI for Employee CRUD | [Frontend Dev] | To Do | 4 days |
| T-103 | Write Unit Tests for Employee API | [Tester] | To Do | 2 days |
| T-104 | Ensure GitHub issues & milestones reflect Sprint 2 tasks | [Project Manager] | In Progress | 2 days |
| T-105 | Assign peer reviews for pull requests | [Lead Developer] | To Do | 1 day |

---

## **5. Test Plan**
### **Expected Coverage Areas**
- **Unit Tests:** Cover all API endpoints (Create, Read, Update, Delete Employee).
- **Integration Tests:** Ensure smooth interaction between frontend and backend.
- **UI Tests:** Validate form submission, error messages, and role-based access.
- **Performance Testing:** Measure response time for API calls.
- **Security Testing:** Verify authentication and data access control.

---

## **6. Sprint Retrospective**
### **What went well?** ✅
- [Example: API development completed as planned]
- [Example: Effective communication between backend and frontend teams]

### **What could be improved?** ⚡
- [Example: More structured test planning]
- [Example: Improve response handling in the API]

### **Action Items for Next Sprint** 🎯
- [Example: Implement authentication for Employee Management API]
- [Example: Automate API testing with Postman or Pytest]

---

This template provides a structured approach to documenting the sprint while incorporating project objectives, user stories, API specifications, test planning, and peer reviews. 🚀

