# capstone-project
🚌 Where Is My Bus – Real-Time Bus Tracking System

📌 Project Overview

Where Is My Bus is a real-time bus tracking web application designed to help passengers track buses, view their current locations, and estimate arrival times at different bus stops.

The system uses GPS tracking, WebSocket communication, and Machine Learning-based ETA prediction to provide updated bus information. It provides separate interfaces for passengers and bus drivers.

The main objective is to make public transportation more convenient, reliable, and efficient by providing real-time bus location information.

🎯 Objectives

- Track buses in real time using GPS.
- Display bus locations and routes on an interactive map.
- Provide estimated arrival times (ETA) for upcoming bus stops.
- Allow drivers to share their live location.
- Support offline data buffering and automatic reconnection.
- Use Machine Learning to improve arrival-time predictions.
- Collect anonymous passenger location updates when official GPS data is unavailable.

✨ Key Features

1. User and Driver Authentication

- Separate login and registration for passengers and drivers.
- Password hashing for secure authentication.
- Driver registration protected by an access code.

2. Real-Time Bus Tracking

- Track bus locations using GPS.
- Display live bus movement on an interactive map.
- Show bus speed and tracking status.
- Automatically update bus positions.

3. Interactive Map

- Displays bus routes and stops.
- Shows the current bus location.
- Provides automatic camera-follow functionality.
- Allows passengers to unlock the map camera.

4. Estimated Time of Arrival (ETA)

- Calculates estimated arrival times for upcoming stops.
- Uses distance, speed, time, and day information.
- Provides both baseline and Machine Learning-based predictions.

5. Machine Learning Integration

- Uses an online-trained Linear Regression model.
- Learns from actual bus arrival observations.
- Improves ETA predictions using collected training samples.
- Compares ML prediction errors with baseline prediction errors.

6. Offline Support

- Stores unsent GPS updates locally.
- Automatically reconnects when the network becomes available.
- Uploads buffered location updates after reconnection.
- Supports dead reckoning when GPS signals are temporarily unavailable.

7. Crowd-Sourced Location Sharing

- Allows passengers to share their location anonymously.
- Uses rounded coordinates to reduce location precision.
- Provides alternative location information when official GPS updates are unavailable.

8. System Performance Monitoring

- Messages per second.
- Average communication latency.
- Dead-reckoning updates.
- Crowd-sourced updates.
- ETA prediction error (MAE).
- Machine Learning training samples.

🛠️ Technologies Used

Technology| Purpose
HTML| Web page structure
CSS| User interface styling
JavaScript| Frontend functionality
Node.js| Backend runtime
Express.js| Server and REST API
WebSocket| Real-time communication
MapLibre GL JS| Interactive maps
GPS / Geolocation API| Location tracking
Machine Learning| ETA prediction
Linear Regression| Arrival-time estimation
Local Storage| Client-side data storage
JSON| Data persistence

🏗️ System Architecture

The application follows a client-server architecture.

1. Passenger Interface: Passengers log in and view bus locations, routes, and estimated arrival times.
2. Driver Interface: Drivers log in and share their real-time GPS coordinates.
3. Backend Server: Node.js and Express.js handle authentication, location updates, and application logic.
4. WebSocket Communication: Transfers real-time location information between the server and connected users.
5. Machine Learning Module: Uses collected bus arrival data to improve ETA predictions.
6. Database Storage: Stores user accounts, sessions, bus information, training samples, and model parameters in a JSON file.

🗺️ Sample Bus Routes

The project currently includes two sample routes around Warangal.

Route 1: Hanamkonda → Warangal Station

- Hanamkonda Bus Stand
- Nakkalagutta
- Subedari
- Warangal Station

Route 2: Warangal Station → Fort Warangal

- Warangal Station
- Mulugu Road
- Mattewada
- Fort Warangal

Note: These are sample routes and coordinates. They can be modified according to actual transportation requirements.

⚙️ Installation and Setup

Prerequisites

- Node.js
- npm (Node Package Manager)
- Modern web browser
- Internet connection

Step 1: Clone the Repository

git clone YOUR_GITHUB_REPOSITORY_URL

Step 2: Open the Project Folder

cd where-is-my-bus

Step 3: Install Dependencies

npm install

Step 4: Start the Server

npm start

Step 5: Open the Application

Open the following address in your browser:

http://localhost:3000

Register as a passenger or driver to explore the application.

Note: Driver registration requires the configured driver access code. For production deployment, configure a secure "DRIVER_CODE" environment variable instead of using the default development code.

📂 Project Structure

where-is-my-bus/
│
├── public/
│   └── index.html
│
├── server.js
├── package.json
├── package-lock.json
├── data.json          (Generated automatically)
└── README.md

🔄 Working Process

1. The driver registers and logs into the application.
2. The driver selects a bus route and starts the trip.
3. The application collects GPS coordinates from the driver's device.
4. The backend receives location updates through WebSocket communication.
5. The server processes the location and updates the bus position.
6. Passengers receive real-time bus location updates.
7. The application calculates estimated arrival times for upcoming stops.
8. The Machine Learning model improves ETA predictions using actual arrival data.

🚀 Future Enhancements

- Integration with actual public transportation GPS systems.
- Addition of more bus routes and stops.
- Mobile application development.
- Improved ETA prediction using advanced Machine Learning algorithms.
- Push notifications for bus arrivals.
- Admin dashboard for managing buses, routes, and drivers.
- Integration with a dedicated database such as MongoDB.
- Deployment on a cloud platform.

🌟 Advantages

- Reduces passenger waiting time.
- Provides real-time bus location information.
- Improves transportation convenience.
- Supports temporary network interruptions.
- Provides intelligent arrival-time predictions.
- Encourages efficient public transportation usage.

👩‍💻 Conclusion

The Where Is My Bus – Real-Time Bus Tracking System provides an intelligent solution for public transportation tracking. By combining GPS, WebSocket communication, interactive maps, and Machine Learning, the application helps passengers access updated bus information and estimated arrival times.

The project demonstrates how modern web technologies can be used to develop a smart, reliable, and efficient transportation tracking system.

---

Project Name: Where Is My Bus – Real-Time Bus Tracking System

Category: Web Development | Real-Time Tracking | Machine Learning

Developed using: HTML, CSS, JavaScript, Node.js, Express.js, WebSocket and MapLibre GL JS
