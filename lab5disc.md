Mark Johnson
mpjohnson1

1. **User Story 1: Borrowing Books**

  - As a **registered library member**, I want to borrow up to **5 books** at a time so that I can read them at home.

#Part 1
    **Acceptance Criteria:**
  
    - A registered library member can borrow up to 5 books at a time.
    - The system should prevent borrowing if the user has already reached the 5-book limit.
    - A book marked as borrowed should not be available for other members until returned.
    - The system should record the borrow date and automatically assign a due date (e.g., 14 days from the borrow date).
    - If a user tries to borrow a book that is not available, an appropriate error message should be displayed.
 
 #Part 2 **Test Case**
   
  #Boundary Value Analysis
  
  Test Scenario: Validate book borrowing limits at boundary values (0, 1, 5, and 6).

**Boundary Values:**

- 0 books (Minimum) → Valid, no borrowing.
- 1 book → Valid borrowing.
- 5 books (Maximum allowed) → Valid borrowing.
- 6 books (Above limit) → Invalid, borrowing should be rejected.

**Test Case ID:** TC_BVA_01
**Title:**	Verify borrowing limits using boundary values
**Preconditions:**	User is registered and logged into the system.
**Test Steps:**
1. Try borrowing 0 books (should be allowed but does nothing).
2. Try borrowing 1 book (should be successful).
3. Try borrowing 5 books (should be successful).
4. Try borrowing 6 books (should be rejected with an error).
**Expected Result:**
- 0 books: Allowed but no action taken.
- 1-5 books: Successful borrowing.
- 6 books: Error message "Borrowing limit exceeded (max 5 books)" displayed.

---

2. **User Story 2: Returning Books**

  - As a **library member**, I want to return borrowed books before the **due date** so that I can avoid fines.

 #Part 1
 
    **Acceptance Criteria:**
    
    - A library member should be able to return books they have borrowed before the due date.
    - Upon return, the book status should be updated to available in the system.
    - The system should calculate if the book is returned on time or overdue.
    - If returned late, the system should calculate and display any fines due (e.g., $1 per day).
    - Members should receive a confirmation message upon successfully returning a book.

 #Part 2  **Test Case**

   #Decision Table Testing

**Test Scenario:** Validate system responses based on book return timing and overdue fines.  

| **Condition** | **Book Returned?** | **Due Date Passed?** | **Expected Outcome** |
|--------------|-----------------|----------------|----------------|
| **Case 1** | Yes | No | Successful return, no fine |
| **Case 2** | Yes | Yes | Successful return, fine applied |
| **Case 3** | No | Yes | Overdue notification sent, fine accumulating |
| **Case 4** | No | No | No action needed |

**Test Case:**  
| **Test Case ID** | TC_DT_01 |
|-----------------|--------------------------------|
| **Title** | Verify book return with and without overdue fine |
| **Preconditions** | A user has borrowed a book, and due date tracking is enabled. |
| **Test Steps** | 1. Borrow a book.<br> 2. Try returning it **before the due date (Case 1)**.<br> 3. Try returning it **after the due date (Case 2)**.<br> 4. Keep it unreturned after the due date (Case 3). |
| **Expected Result** | - If returned **before** due date, return is successful, no fine.<br> - If returned **after** due date, return is successful, but a fine is applied.<br> - If not returned **past due**, an overdue notification is sent, and fines accumulate. |

---


3. **User Story 3: Overdue Notifications**

  - As a **library admin**, I want to automatically notify members of overdue books by email, so they can return books promptly.

#Part 1

    **Acceptance Criteria:**

    - The system should automatically check for overdue books daily.
    - If a book is overdue, an email notification should be sent to the member.
    - The notification should include details such as book title, due date, number of overdue days, and any applicable fine.
    - The system should escalate notifications if the book remains overdue beyond a set period (e.g., 7 days, 14 days).
    - Library admins should have access to a report of overdue books and fines.
    - The system should log all notifications sent for record-keeping.

 
 #Part 2  **Test Case**

  #Transition Testing
  
**Test Scenario:** Validate state transitions from "book borrowed" to "book overdue" to "book returned."  

**State Transitions:**  
1. **Book Borrowed → Before Due Date → No notification sent.**  
2. **Book Borrowed → After Due Date → Overdue notification sent.**  
3. **Book Overdue → Returned → Status updated to available, fine calculated if applicable.**  


**Test Case ID:** TC_TT_01
**Title:**	 Verify overdue notifications and state transitions 
**Preconditions:**	User has borrowed a book.
**Test Steps:**
 1. Borrow a book.
 2. Keep it until the due date passes.
 3. Verify that an overdue email is sent
 4. Return the book after receiving the notification.
 5. Verify that the book status changes to **available** and fines (if any) are recorded.
**Expected Result:**
 - If the due date **has not passed**, no notification is sent.
 - If the due date **has passed**, an overdue email is sent.
 - If the book is **returned**, its status updates, and any fine is recorded.

---


4. **User Story 4: Membership Registration**

  - As a **new user**, I want to register for a library membership by providing my name, age (should be **12 or above**), and address so I can borrow books.

  #Part 1: **Acceptance Criteria:**

    - A new user should be able to register by providing their name, age, and address.
    - The system should validate that the age is 12 or above. If below 12, registration should be denied with an appropriate message.
    - The system should store user information securely and assign a unique membership ID.
    - Upon successful registration, the user should receive a welcome email confirming their membership.
    - Members should be able to log in using their credentials after registration.
    - The system should prevent duplicate memberships using the same name and address.

#Part 2: Test case

  #Equivalence Partitioning

**Test Scenario:** Validate state transitions from "book borrowed" to "book overdue" to "book returned."  

**Partitions:**  
- **Valid: Age (12 and above):** Registration should be successful.  
- **Invalid: Age (Below 12):** Registration should be rejected with an error message.

**Test Case ID:** TC_EP_01 
**Title:**	 Validate age restriction for membership registration
**Preconditions:**	System is online, and the registration page is accessible.
**Test Steps:**
1. Navigate to the registration page.
2. Enter a name, address, and age **(e.g., 10 - invalid, 12 - valid, 15 - valid)**.
3. Submit the form. 

**Expected Result:**
- If the age is **12 or above**, registration succeeds, and the user receives a welcome email.
- If the age is **below 12**, registration is rejected, and an error message **"Minimum age requirement is 12 years"** is displayed. 



---
