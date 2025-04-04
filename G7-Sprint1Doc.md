# **Sprint 1 Documentation**

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
| **Task ID** | **Task Description** | **Assigned To** | **Status** |
|------------|----------------|------------|--------|
| T-101 | Implement Employee Creation API | [Reena Shrestha] | Done |
| T-102 | Develop UI for Employee CRUD | [Reena Shrestha] | Done |
| T-103 | Write Unit Tests for Employee API | [Sarah White] | Done |

---

## **5. Sprint Retrospective**
### **What went well?** ✅
- [API development completed as planned]
- [Effective communication between backend and frontend teams]

### **What could be improved?** ⚡
- [More communication from absent team members (Like Mark Johnson)]
- [More contributions from absent team members (Like Mark Johnson)]


---


