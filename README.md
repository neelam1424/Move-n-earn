# 🎓 Move-n-Earn 

A full-stack application that allows users to track their movement and earn rewards based on activity. Built with:

- 🌐 **Frontend**: React.js  
- 🔧 **Middleware/API Layer**: Golang  
- 🗃️ **Backend**: MongoDB  

---

## 🚀 Features

- User authentication and activity tracking
- RESTful API built in Go for fast and scalable backend services
- Responsive UI built with React
- MongoDB database for storing user data and movement history
- Seamless communication between frontend and backend

---

## To start FrontEnd (React)
```
cd move-n-earn/client
npm install
npm start
```

## To start GOlang Server
```
cd go-server
go run main.go
```
## MongoDB Setup
```
Make sure MongoDB is installed and running.
Update the MongoDB connection string in your Go code (typically in main.go):

clientOptions := options.Client().ApplyURI("mongodb://localhost:27017")
```


## 🔧 Features

### 🔐 1. User Authentication & Role-based Signup

Secure login and signup system.

Two separate signup flows:

Client: Users who request transport services.
Transporter: Users who offer transport services.
Role-based access to features and dashboard data.
Password hashing for secure credential storage.

### 🧭 2. Manual Distance Calculation

Users manually enter pickup and drop locations.
System calculates the distance between those locations internally.
Used as a base for pricing and billing logic.

### 🚚 3. Vehicle Type & Size-Based Pricing

Users choose vehicle size/type (e.g., small, medium, large).
Pricing is dynamically adjusted based on:
Vehicle size
Entered distance

### 💸 4. Dynamic Rate Calculation

Total transportation rate is calculated using:
Rate per km
Vehicle size multiplier
Distance entered manually

Formula used:
Total Rate = Distance × Base Rate × Vehicle Size Multiplier

### 🧾 5. Billing & Confirmation

Once rate is calculated, a final bill is generated.

Billing details include:
Distance
Chosen vehicle
Total cost
Client and transporter information
Data is stored in MongoDB for record-keeping.

### 📊 6. Interactive Dashboard

Separate dashboards for:

Clients: View past bookings, billing, and status.
Transporters: View incoming orders, earnings, and availability.

Displays:

Booking details
Distance and rate breakdown
Time stamps and user metadata

### 📁 7. MongoDB Integration

MongoDB is used to store:

User data (clients and transporters)
Booking details
Billing records
Structured collections for scalable data handling.

###💡 8. Clean, Responsive Frontend (React)

Built using React.js for fast and dynamic UI.
Responsive design supports both desktop and mobile use.
Form validation and error handling for smooth UX.

### 🌐 9. Golang Middleware API

Acts as a secure bridge between frontend and backend.

Handles:
Authentication logic
Distance & rate computation
Billing generation
MongoDB communication

Homepage
![homepage](https://github.com/user-attachments/assets/3caa8f59-0c0d-4b0b-a4e0-a4202b8849e5)
Popup
![popup](https://github.com/user-attachments/assets/5cdd1789-3dac-4036-907b-090cac20d9e9)
Sign-Up for Client
![Sign-up](https://github.com/user-attachments/assets/4ad83139-826b-4136-a1db-e9f4b1c5ffc0)
Sign-Up for Transporter 
![SignupT](https://github.com/user-attachments/assets/61a8e773-5b06-4373-a743-eed9fe58a0e2)
Login Page
![Login](https://github.com/user-attachments/assets/ffc827a4-c518-443f-a1c9-08a3089a475e)
Maps
![maps](https://github.com/user-attachments/assets/4d26d189-93e0-4ba0-b1ab-f2fc9c5ecdc4)
Dashboard
![dashboard](https://github.com/user-attachments/assets/660958a3-ad53-4d60-8d28-c62f10b4fe51)
Bill
![bill](https://github.com/user-attachments/assets/963625a8-d21e-428c-b46e-94bed7311cda)


