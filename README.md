# 📁 File System Watcher – Real-Time File Tracking App

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Swing](https://img.shields.io/badge/Swing-008080?style=for-the-badge)
![JavaMail](https://img.shields.io/badge/JavaMail-FF6F00?style=for-the-badge)
![WatchService](https://img.shields.io/badge/WatchService_API-4B8BBE?style=for-the-badge)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![JUnit](https://img.shields.io/badge/JUnit-25A162?style=for-the-badge)
![Checkstyle](https://img.shields.io/badge/Checkstyle-FFD43B?style=for-the-badge)

![MVC](https://img.shields.io/badge/MVC_Architecture-2C3E50?style=for-the-badge)
![Observer](https://img.shields.io/badge/Observer_Pattern-34495E?style=for-the-badge)
![Abstraction](https://img.shields.io/badge/Interface_Abstraction-7F8C8D?style=for-the-badge)

---

## 📌 Description

File System Watcher is a Java-based desktop application that monitors real-time file system events (**CREATE**, **MODIFY**, **DELETE**) using the **WatchService API**.  
It logs events into an **SQLite database**, supports **query filtering**, allows **CSV export**, and enables **secure email delivery** of reports.

Think of it like a **security camera for your files**, it watches a folder in real time, records what happens, and lets you search, export, and even email a report of those changes.

This project was developed as part of **TCSS 360 - Software Development & Quality Assurance** at the **University of Washington Tacoma**, following **MVC architecture** and incorporating the **Observer pattern** for responsive UI updates.

---

## 🚀 Features

- **Real-Time File Monitoring**: Detects when files are created, changed, or deleted.  
  &nbsp;&nbsp;&nbsp;&nbsp;Tracks file events (**CREATE**, **DELETE**, **MODIFY**) using Java’s **WatchService API**.  
  &nbsp;&nbsp;&nbsp;&nbsp;Supports monitoring for **custom file extensions** in addition to predefined ones.

- **Search, Filter & Save Records**: Find specific changes and store them for future reference.  
  &nbsp;&nbsp;&nbsp;&nbsp;Query filtering with **SQL** to retrieve events quickly.  
  &nbsp;&nbsp;&nbsp;&nbsp;Saves all events to an **SQLite database (JDBC)**.

- **Export & Email Reports**: Generate and share reports directly from the app.  
  &nbsp;&nbsp;&nbsp;&nbsp;Export filtered results to **CSV** with metadata.  
  &nbsp;&nbsp;&nbsp;&nbsp;Send CSV reports via **JavaMail API** + Gmail SMTP  
  &nbsp;&nbsp;&nbsp;&nbsp;(App Password authentication, TLS encryption).

- **Graphical User Interface (Easy to Use)**: Simple and intuitive desktop interface.  
  &nbsp;&nbsp;&nbsp;&nbsp;**Swing-based main window** to start/stop monitoring and view events in real time.  
  &nbsp;&nbsp;&nbsp;&nbsp;**Query window** with filters: Date, File Extension, Event Type, Top N results.  
  &nbsp;&nbsp;&nbsp;&nbsp;**Keyboard shortcuts** for quick actions (Start, Stop, Save).

- **Robust Architecture & Testing**: Designed for maintainability and reliability.  
  &nbsp;&nbsp;&nbsp;&nbsp;Follows **MVC architecture** for separation of concerns.  
  &nbsp;&nbsp;&nbsp;&nbsp;Implements **Observer pattern** for real-time UI updates.  
  &nbsp;&nbsp;&nbsp;&nbsp;Includes **JUnit tests** for export and email functionality.  
  &nbsp;&nbsp;&nbsp;&nbsp;Code style enforced using **Checkstyle**.

---

## 🛠 Tech Stack

- **Language:** Java 21  
- **Frameworks & APIs:** Swing, JavaMail, WatchService API  
- **Database:** SQLite (JDBC)  
- **Tools:** IntelliJ IDEA, JUnit, Checkstyle  
- **Architecture & Patterns:** MVC, Observer Pattern, Interface Abstraction  

---

## 📌 How It Works

1. **Select what to monitor** – Choose a folder and specify file types to track (e.g., `.docx`, `.pdf`).  
2. **Monitor in real time** – The application continuously detects and records file changes.  
3. **Search and filter results** – Locate specific events using filters such as date, type, or action.  
4. **Save and share reports** – Export results to CSV or send them directly via email.

---

## 👩‍💻 My Contributions

- Designed and implemented the **QueryWindow GUI**, event filtering, and CSV export functionality.  
- Integrated secure email reporting using **JavaMail API** + **Gmail SMTP**.  
- Developed core classes: `FileMonitor`, `FileEvent`, `EmailSender`, `IEmailSender`.  
- Wrote **JUnit test cases** for email and export features.  
- Applied **MVC architecture** and **Observer pattern** to ensure modularity and maintainability.

---

## 📂 Project Structure

```plaintext
src/
├── controller/
│   ├── FileMonitor.java
│   └── FileSystemMain.java
├── model/
│   ├── DatabaseManager.java
│   ├── FileEvent.java
│   ├── EmailSender.java
│   ├── IEmailSender.java
│   └── CSVExporter.java
├── view/
│   ├── MainWindowFile.java
│   └── QueryWindow.java
└── tests/
    ├── EmailSenderTest.java
    ├── CSVExporterTest.java
    └── DatabaseManagerTest.java
