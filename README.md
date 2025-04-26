# Face-recognition

📄 Abstract
In today's fast-paced world, manual attendance systems are time-consuming, prone to errors, and vulnerable to proxy attendance. This project presents a Face Recognition-Based Attendance System that automates the process using computer vision techniques. The system captures real-time video from a webcam, detects and recognizes faces using deep learning-based encodings, and automatically marks attendance by storing the user's name, date, and time in a SQL database. Developed using Python, OpenCV, and face_recognition libraries, along with MySQL/SQLite for database management, this system enhances accuracy, security, and efficiency. It minimizes human intervention, ensures authentic attendance records, and can be deployed across educational institutions, workplaces, or events. Future enhancements could include cloud-based storage, mobile app integration, and additional security features


 System Architecture Diagram:
     A simple flowchart:
            Camera → Face Detection → Face Encoding → Compare with DB → Mark Attendance → Store in SQL DB

 
Tools:

Python

OpenCV, face_recognition

MySQL / SQLite

Tkinter (optional GUI)

NumPy, datetime
