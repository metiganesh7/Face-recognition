# Face-recognition



**📄 Abstract**

In today's fast-paced world, manual attendance systems are time-consuming, prone to errors, and vulnerable to proxy attendance. This project presents a Face Recognition-Based Attendance System that automates the process using computer vision techniques. The system captures real-time video from a webcam, detects and recognizes faces using deep learning-based encodings, and automatically marks attendance by storing the user's name, date, and time in a SQL database. Developed using Python, OpenCV, and face_recognition libraries, along with MySQL/SQLite for database management, this system enhances accuracy, security, and efficiency. It minimizes human intervention, ensures authentic attendance records, and can be deployed across educational institutions, workplaces, or events. Future enhancements could include cloud-based storage, mobile app integration, and additional security features



** System Architecture Diagram:**
     A simple flowchart:         
     Camera → Face Detection → Face Encoding → Compare with DB → Mark Attendance → Store in SQL DB
                 ![image](https://github.com/user-attachments/assets/655f35c5-7473-4810-96ac-6bf1db3038a4)



 
**Tools:**

**1 . Python**
Python is the main programming language used because of its simplicity, wide library support, and strong community for machine learning and computer vision projects.

**2 . OpenCV (Open Source Computer Vision Library):**
OpenCV is used for real-time computer vision tasks such as face detection, image processing, and handling video frames from the webcam.

**3 . face_recognition Library**
Built on top of dlib, this library simplifies face recognition by providing pre-trained models. It can detect faces, generate facial feature encodings, and compare faces with high accuracy.

**4 . NumPy**
NumPy supports mathematical operations on large arrays and matrices, which is useful when processing image data and face encodings efficiently.


![image](https://github.com/user-attachments/assets/6f7fdb6b-1c7e-4e0b-8a40-a917013c37bd)

**5 . MySQL / SQLite (Database Management System)**
The SQL database stores attendance records securely, including name, date, and time.
MySQL is used for more robust setups, while SQLite is preferred for lightweight, portable solutions.

**6 . MySQL Connector / sqlite3 (Python Libraries**)
These libraries help Python connect with SQL databases to insert, update, and retrieve attendance data.

**7 . Tkinter (Optional - GUI Framework)**
Tkinter is used if a basic graphical user interface (GUI) is required to make the system user-friendly, such as buttons to "Start Attendance" or "View Records."

**9 . Datetime Module (Python Standard Library)**
Used to capture the current date and time during attendance marking automatically.








**Key Features of Face Recognition Attendance System:**
"Our system provides an efficient, real-time, and secure method for marking attendance using facial recognition technology, with automatic database recording, multi-user support, and offline functionality."





1 . Real-Time Face Detection and Recognition
The system captures live video from a webcam and instantly detects and recognizes faces within the frame.
Recognition is fast, ensuring minimal delay during attendance marking.

2 . Automatic Attendance Marking
Once a face is recognized, the system automatically records the person's name along with the current date and time in the SQL database.
No manual input required, reducing chances of errors.

3 . Database Integration
Attendance data is securely stored in a structured SQL database (MySQL or SQLite).
Each record includes the Name, Date, and Time for future tracking and analysis.

4 . Multiple User Handling
The system can recognize and manage attendance for multiple individuals simultaneously.
Ideal for classrooms, offices, or group events.

5 . Duplicate Attendance Prevention
The system can be extended to check if a user has already marked attendance for the day, preventing multiple entries.

6 . Offline Functionality
Since face recognition and database operations are local, the system can work without an internet connection.

7 . Simple and User-Friendly Interface
Easy to operate even for non-technical users.
Optionally, a GUI using Tkinter can provide buttons and status displays.

8 . Secure and Proxy-Free
Reduces the chances of proxy attendance (someone else marking attendance).
Ensures that only the registered person's face is accepted.

9 . Highly Scalable
More user faces can be added to the system at any time without retraining from scratch.

10 . Cost-Effective
Uses a standard webcam and open-source libraries, making it a low-cost solution compared to biometric devices.







**🛠 Implementation Steps**

1 . Environment Setup:
Install required libraries such as opencv-python, face_recognition, numpy, and a database connector like mysql-connector-python or use built-in sqlite3.
Set up a database (MySQL or SQLite) with a table to store attendance records (name, date, time).

2 . Face Data Collection:
Capture multiple face images of each user through the webcam.
Store these images in a dataset/ folder, using a consistent naming convention (like Name_0.jpg, Name_1.jpg).

3 . Face Encoding Generation
Load the saved face images.
Use the face_recognition library to generate unique face encodings (numerical representations of the faces).
Save these encodings into memory (lists) for future comparisons.

4 . Real-Time Face Recognition
Access the webcam feed live.
For each frame:
    Detect faces in the video.
    Generate encodings for the detected faces.
    Compare the encodings against the known face encodings using face_recognition.compare_faces().

5 . Attendance Marking
If a match is found, extract the recognized person’s name.
Record the attendance by inserting the name, current date, and current time into the SQL database.
Optionally, avoid multiple entries by checking if the person has already been marked present for the day.

6 . User Interface 
 Create simple buttons like "Start Attendance" and "View Records" using Tkinter.

7 . Testing and Validation
Test with different users, lighting conditions, and angles.
Validate if the correct name is being detected and logged without duplication.

8 . Reporting and Data Handling
Retrieve attendance records from the database when needed.
Finally, export records to Excel or CSV using libraries like pandas.





