# 🗓️ Staff Scheduling System – CVIP Project

This project is a web-based **Staff Scheduling System** built to help manage staff assignments, work shifts, and scheduling easily.  
It is developed using HTML, CSS, JavaScript, PHP and MySQL — allowing admin users to add staff, assign schedules, and view or update work timing records.

---

## 🔧 Features

- Add and manage staff information  
- Assign work schedules and shift timings  
- View all scheduled work in a structured format  
- Update or delete schedule entries  
- Fully responsive and user-friendly UI  
- Persistent data stored in MySQL database  

---

## 🛠 Technologies Used

| Technology   | Purpose |
|--------------|---------|
| **HTML5**    | Page layout and content structure |
| **CSS3**     | Styling and responsive design |
| **JavaScript** | Front-end interaction |
| **PHP**      | Server-side operations and form handling |
| **MySQL**    | Database for storing staff and schedules |
| **XAMPP**    | Local server environment |

---

## 📁 Project Structure

```text
Staff-Scheduling-System/
│
├── index.php             # Main dashboard / homepage
├── add_staff.php         # Add new staff members
├── add_schedule.php      # Assign schedules / shifts
├── view_schedule.php     # View scheduled work
├── update_schedule.php   # Update schedule entries
├── delete_schedule.php   # Delete schedules
├── css/                  # Stylesheets
├── js/                   # JavaScript files
└── db/                   # Database config / connection files
```

---

## 🗄 Database Design

**Database Name:** `staff_db`  
**Tables Used:**

```sql
CREATE TABLE `staff` (
  `staff_id` INT(11) NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(255) NOT NULL,
  `email` VARCHAR(255),
  `phone` VARCHAR(50),
  PRIMARY KEY (`staff_id`)
);

CREATE TABLE `schedule` (
  `schedule_id` INT(11) NOT NULL AUTO_INCREMENT,
  `staff_id` INT(11) NOT NULL,
  `work_date` DATE NOT NULL,
  `shift_start` TIME NOT NULL,
  `shift_end` TIME NOT NULL,
  PRIMARY KEY (`schedule_id`),
  FOREIGN KEY (`staff_id`) REFERENCES `staff`(`staff_id`) ON DELETE CASCADE
);
```

---

## 🚀 How to Run Locally

1. Install and run **XAMPP** or any PHP-MySQL environment.  
2. Copy the project folder into:

```
C:\xampp\htdocs\
```

3. Open browser and go to:

```
http://localhost/phpmyadmin
```

4. Create a database named:

```
staff_db
```

5. Create the required tables using the SQL given above.  
6. Check database connection settings in project files:

```php
$connection = mysqli_connect('localhost', 'root', '', 'staff_db');
```

7. Run the project:

```
http://localhost/Staff-Scheduling-System/index.php
```

---

## 🧠 What I Learned

- Backend form handling using PHP  
- CRUD operations using PHP and MySQL  
- Designing relational databases and foreign keys  
- Full-stack workflow: UI → Form → Database → Display  
- Debugging database queries and user input validation  

---

## 👤 Author

Developed by **Sanika Tole**

