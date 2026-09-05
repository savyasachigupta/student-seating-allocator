# 🪑 Student Seating Allocator

A console-based **C application** for managing student seating assignments in a configurable examination/classroom hall.

The project demonstrates practical use of **structures, dynamic memory allocation, file handling, arrays, searching, and logging** in C.

---

## 🎯 Overview

The Student Seating Allocator allows a user to initialize a seating hall, allocate seats to students, remove allocations, search for students, display the current seating layout, and maintain persistent student data.

The application supports both:

- **Automatic seat allocation**
- **Manual seat allocation by specifying row and column**

The program supports halls of up to **20 × 20 seats**.

---

## ✨ Features

- 🏫 Configurable hall dimensions
- 🪑 Automatic seat allocation
- 🎯 Manual seat allocation
- ❌ Seat deallocation
- 🔎 Student search by roll number
- 📋 Seating-hall visualization
- 💾 Persistent student data using binary file storage
- 📝 Timestamped allocation/deallocation logs
- 🧠 Dynamic memory allocation for student records
- 🔄 Loading previously saved student data

---

## ⚙️ How It Works

```text
             Start Program
                   │
                   ▼
          Initialize Seating Hall
                   │
                   ▼
          Load Saved Student Data
                   │
                   ▼
              Main Menu
                   │
       ┌───────────┼────────────┐
       │           │            │
       ▼           ▼            ▼
   Allocate     Search       Display
       │           │            │
       ├───────────┤            │
       │                        │
       ▼                        ▼
   Deallocate              View Log
       │
       ▼
    Save Data
       │
       ▼
       Exit
```

---

## 🧩 Main Operations

### 1. Automatic Seat Allocation

The program searches the seating matrix for the first available seat and assigns it to the student.

The student's:

- Roll number
- Name
- Row
- Column

are stored in memory and recorded in the allocation log.

### 2. Manual Seat Allocation

A user can specify the exact row and column for a student.

The program validates:

- Whether the requested position is within the hall
- Whether the selected seat is already occupied

### 3. Deallocation

Students can be removed from their assigned seats using their roll number.

The corresponding seat becomes available again.

### 4. Student Search

The program searches stored student records by roll number and displays the student's assigned row and column.

### 5. Hall Display

The current seating arrangement is represented as a matrix:

```text
O - O - -
- O - - -
O O - - -
```

Where:

- `O` = Occupied seat
- `-` = Available seat

### 6. Logging

Important operations are recorded with timestamps in:

```text
allocationlog.txt
```

Examples include:

- Seat allocation
- Manual allocation
- Deallocation
- Session start/end

---

## 💾 Data Persistence

The application uses two local files:

| File | Purpose |
|---|---|
| `students.dat` | Binary storage for student records |
| `allocationlog.txt` | Human-readable operation log |

Student records contain information such as:

- Roll number
- Name
- Row
- Column

The program loads saved records when starting and writes updated records when data is saved.

> **Privacy note:** Runtime data files should not contain real student information in a public repository. Use synthetic/sample data for demonstration.

---

## 🧠 Concepts Demonstrated

This project applies several fundamental C programming concepts:

### Data Structures

- `struct`
- Two-dimensional arrays
- Dynamic arrays using pointers

### Memory Management

- `malloc()`
- `realloc()`
- `free()`

### File Handling

- `fopen()`
- `fread()`
- `fwrite()`
- `fgets()`
- `fprintf()`
- `fclose()`

### Algorithms & Logic

- Linear search
- Matrix traversal
- Seat availability checking
- Record insertion and deletion

### Standard Libraries

- `stdio.h`
- `stdlib.h`
- `string.h`
- `time.h`

---

## 📂 Project Structure

```text
student-seating-allocator/
│
├── C_Project.c
├── README.md
├── .gitignore
│
└── Runtime Files
    ├── students.dat
    └── allocationlog.txt
```

The runtime files are generated/used by the application and should preferably be excluded from a public repository when they contain local or personal data.

---

## 🚀 Getting Started

### Prerequisites

You need a C compiler such as:

- GCC
- MinGW
- Clang

### Compile

Using GCC:

```bash
gcc C_Project.c -o student-seating-allocator
```

### Run on Windows

```bash
student-seating-allocator.exe
```

### Run on Linux/macOS

```bash
./student-seating-allocator
```

---

## 🖥️ Application Menu

The program provides options for:

```text
=== Student Seating Allocator ===

1. Allocate Seat from student choice
2. Deallocate Seat
3. Display Hall
4. Search Student
5. View Log
6. Save & Exit
7. Allocate Seat from user choice
0. Exit
```

---

## 📌 Example Workflow

```text
Initialize Hall
     ↓
Enter Student Details
     ↓
Allocate Seat
     ↓
Display Seating Arrangement
     ↓
Search / Deallocate if Required
     ↓
Save Student Data
     ↓
Exit
```

---

## 🔐 Data & Security Considerations

Although this is an educational C project, the application handles student-related records.

For a production implementation, additional controls would be appropriate:

- Input validation
- Bounds checking
- Safer string handling
- Duplicate roll-number detection
- Secure storage of student records
- Access control
- Data encryption
- Backup and recovery
- Audit-log protection

---

## 🛠️ Future Improvements

- [ ] Add stronger input validation
- [ ] Prevent duplicate student roll numbers
- [ ] Improve memory/error handling
- [ ] Add configurable seating patterns
- [ ] Add random seat allocation
- [ ] Add teacher/admin authentication
- [ ] Export seating plans to CSV
- [ ] Improve terminal UI
- [ ] Add automated test cases
- [ ] Separate source code into modules

---

## 👨‍💻 Author

**Savyasachi Gupta**

Cybersecurity · Software Development · Machine Learning

- GitHub: [savyasachigupta](https://github.com/savyasachigupta)
- LinkedIn: [Savyasachi Gupta](https://www.linkedin.com/in/savyasachi-gupta-a03211374/)
- LeetCode: [code-kht](https://leetcode.com/u/code-kht/)

---

<p align="center">

### 🪑 Allocate. Manage. Organize.

</p>
