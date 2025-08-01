# 🎓Mentora-Smart-Learning-Exam-Platform
Mentora is an integrated, intelligent, and secure platform for learning, assessment, and performance tracking, built with Java, MySQL, and a strong foundation in Data Structures &amp; Algorithms (DSA). It empowers both students and educators with adaptive learning tools, robust exam security features, and actionable analytics for academic growth.
## 📌Overview

Mentora is an integrated, intelligent, and secure platform for learning, assessment, and performance tracking, built with Java, MySQL, and a strong foundation in Data Structures & Algorithms (DSA). It empowers both students and educators with adaptive learning tools, robust exam security features, and actionable analytics for academic growth.

---

## 📌Problem Statement

In the current educational landscape, students and educators struggle with fragmented study resources, inefficient assessment methods, academic dishonesty, and lack of personalized performance tracking. Traditional systems fail to offer an integrated approach that seamlessly connects learning, examinations, and progress analysis in a structured and adaptive manner.

To address these challenges, we propose a DSA-driven Smart Learning & Exam Platform, built using Java, Data Structures & Algorithms (DSA), and MySQL.

With the rise of online assessments, there’s a growing need for systems that:
- Ensure fair examinations through cheating detection (like tab switching and inactivity monitoring),
- Provide adaptive assessments that dynamically adjust difficulty and timer based on performance,
- Offer insightful post-exam analysis to help students improve over time.

---

## 📌Tech Stack

- Programming Language: Java (Swing for GUI)
- Database: MySQL
- Backend Connectivity: JDBC
- Core Concept: Implementation of real-world systems using Data Structures & Algorithms

---
###  📌Data Structures Used (DSA-Centric Implementation)

| Data Structure                   | Purpose                                                      |
|----------------------------------|--------------------------------------------------------------|
| `PriorityQueue<Question>`        | Max Heap for showing top 3 performers in leaderboard         |
| `HashSet<Integer>`               | Tracks already asked questions in a test session             |
| `Stack<QuestionState>`           | Enables ‘Previous’ question functionality                    |
| `ArrayList<Question>`            | Stores all questions from database                           |
| `HashMap<String, ArrayList<?>>`  | Maps difficulty to its corresponding list of questions       |
| `ArrayList<QuestionState>`       | Used for storing responses for review functionality          |
| `HashMap<String, Integer>`       | Aggregates per-topic scores for post-exam analysis           |



###  📌Smart Question Generator – Data Structures Used

| Data Structure                   | Purpose                                                      |
|----------------------------------|--------------------------------------------------------------|
| `ArrayList<Question>`            | Storing & filtering questions (filters, suggestions, etc.)   |
| `HashMap<String, String[]>`      | Mapping topic to subtopics for dropdowns                     |
| `HashSet<Integer>`               | Tracking already suggested/asked questions                   |



###  📌Anti-Cheating & Plagiarism Detection

| Data Structure / Algorithm       | Used For                                                     |
|----------------------------------|--------------------------------------------------------------|
| `HashMap<String, Integer>`       | Maps student ID to number of cheating attempts               |
| `Queue<String>` (`LinkedList`)   | Stores latest 10 suspicious actions in FIFO order            |
| `LinkedList<CheatingLog>`        | Dynamic log structure for real-time cheating entries         |
| `ArrayList<CheatingLog>`         | Used for populating admin JTable from DB                     |
| `KMP Algorithm`                  | Efficient plagiarism detection in subjective answers         |



---

## 📌Key Features

###  Student Module
- Login Authentication (Student/Admin)
- Dashboard:
  - Personalized greeting
  - Top 3 scorers leaderboard (DSA-based Max Heap)
  - Actions: `Revise` or `Start Test`

- Revise Section:
  - Filter questions by Topic, Subtopic, and Difficulty
  - “Suggest Questions” based on past performance
  - Show Answers
  - Load All Questions
  - Reset Filters
  - Back Navigation

- Start Test:
  - Adaptive Difficulty based on responses - where in for every right answer, the next question is of higher difficulty, and on the contrary for every wrong answer, the difficulty of the next question drops accordingly.
  - Adaptive Timer based on difficulty level - timer changes dynamically according to the difficulty of the question. 
  - Power-Up System: Upon pressing this button, 2x points for correct answers, -1 for incorrect. (special feature)
  - Anti-cheating Features:
    - Tab Switch Detection
    - Inactivity Detection
    - Window Minimization

- Post-Test Options:
  - Review (question-by-question feedback)
  - Summary (performance graph + areas of improvement)

### Admin Module
- View cheating logs with timestamps and student IDs
- Monitor exam sessions and track student-wise progress

---

## 📌Code Flow Summary

1. Login → Role selection (Student/Admin)
2. Student Dashboard → View leaderboard, choose `Revise` or `Start Test`
3. Revise → Filter & review questions using DSA-based smart generator
4. Test → Adaptive questions, timer, power-ups, and cheat detection
5. Post-Test → Review answers and get analytics-based summary
6. Admin Panel → Access session logs and cheating reports

---

## 📌Future Enhancements

- AI-driven Smart Question Recommendation System
- PDF/Excel Export for Reports
- Cloud Deployment & Real-Time Exam Hosting
- Mobile-Responsive Design for All Devices

---
## 📌Demo Video

**https://drive.google.com/file/d/1UL6ib4eupeaU-vLXLByQivv_NIT7Go0Z/view?usp=drivesdk**

---

## 📌Setup Instructions

1. Clone this repository.
2. Create the required tables in MySQL
3. Configure database connection in the codebase.
4. Compile and run using your preferred IDE (IntelliJ / Eclipse / NetBeans).

---
