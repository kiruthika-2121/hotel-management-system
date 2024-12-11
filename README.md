****Hotel Management System****

The Hotel Management System is a web-based application designed to streamline hotel operations and provide a seamless experience for both hotel staff and customers. 
Built using HTML, CSS, Python (Flask), and MySQL, the system handles room availability checks, bookings, cancellations, payments, and feedback collection.

---

**Technologies Used**
Frontend: HTML, CSS for structure and styling.
Backend: Python with the Flask web framework.
Database: MySQL for storing and managing data.

---

**Features**
1. Room Availability: Customers can check available rooms for specific dates and room types.
2. Room Booking: Allows users to book a room by providing details such as name, contact information, and payment confirmation.
3. Room Cancellation: Enables customers to cancel their bookings with a valid booking reference.
4. Feedback System: Collects feedback from users to improve hotel services.
5. Payment Gateway: Simulates or integrates basic payment functionality to confirm room bookings.

---

**Database Schema**
The database schema will include tables such as:
//
CREATE DATABASE hotel_management;

USE hotel_management;

CREATE TABLE rooms (
    room_id INT AUTO_INCREMENT PRIMARY KEY,
    room_type VARCHAR(50),
    price DECIMAL(10, 2),
    available BOOLEAN DEFAULT TRUE
);

CREATE TABLE bookings (
    booking_id INT AUTO_INCREMENT PRIMARY KEY,
    customer_name VARCHAR(100),
    email VARCHAR(100),
    phone VARCHAR(15),
    room_id INT,
    check_in DATE,
    check_out DATE,
    FOREIGN KEY (room_id) REFERENCES rooms(room_id)
);

CREATE TABLE feedback (
    feedback_id INT AUTO_INCREMENT PRIMARY KEY,
    customer_name VARCHAR(100),
    message TEXT
);

INSERT INTO rooms (room_type, price, available) VALUES
('Single Room', 50.00, TRUE),
('Double Room', 80.00, TRUE),
('Suite', 150.00, TRUE);
//

---

**Screenshots**
![Screenshot 2024-12-11 180217](https://github.com/user-attachments/assets/b89ca0d2-b615-4da2-a94e-7a2c25b3a7c4)

![Screenshot 2024-12-11 180230](https://github.com/user-attachments/assets/cae5d2b6-e9e1-4f17-835c-c3d2cc424142)

![Screenshot 2024-12-11 180300](https://github.com/user-attachments/assets/9b2358db-66fb-4d83-b4ce-a43bda51cb32)

![Screenshot 2024-12-11 180316](https://github.com/user-attachments/assets/919d7157-20b8-4af3-b714-4bb3f40e50a6)

![Screenshot 2024-12-11 180331](https://github.com/user-attachments/assets/adbf3dfa-5153-46ed-9bee-3ae68a2f4096)

![Screenshot 2024-12-11 180431](https://github.com/user-attachments/assets/b7b05ae0-a8a1-4492-ad97-1832155e0094)

******THANK YOU!!!******








