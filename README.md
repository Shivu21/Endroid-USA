# **Endroid Streaming App**

## **Overview**
The **Endroid Streaming App** is a robust Flutter application designed for real-time streaming, device management, and user authentication. It adheres to **Clean Architecture**, utilizes **Firebase** for backend services, **Provider** for state management, and **GetIt** for Dependency Injection. The app integrates **RTSP Streaming** with **VLC Player**, providing an efficient and seamless video streaming experience.

---

## **Table of Contents**
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Architecture](#project-architecture)
- [File Structure](#file-structure)
- [Setup and Installation](#setup-and-installation)
- [App Modules](#app-modules)
- [Screenshots and Previews](#screenshots-and-previews)
- [Contributing](#contributing)
- [License](#license)

---

## **Features**
- **Authentication**:
  - Secure login, signup, and logout using Firebase Authentication.
- **Real-Time Streaming**:
  - RTSP streaming with dynamic grid layout.
  - Support for adding and managing multiple streams.
- **Device Management**:
  - Discover network cameras via ONVIF.
  - Manual camera addition or through QR code scanning.
- **State Management**:
  - Provider for efficient state handling.
  - Dependency injection using GetIt.
- **Clean Architecture**:
  - Layered and modularized structure for scalability and maintainability.
- **Responsive UI**:
  - Adaptive design for different devices.
- **Custom UI Components**:
  - Smooth loading animations using **Flutter Spinkit**.
  - Alerts and notifications with **Awesome Snackbar Content**.

---

## **Technologies Used**
- **Flutter**: For building cross-platform UI.
- **Firebase**: For backend services like Authentication and Firestore.
- **Provider**: For state management.
- **GetIt**: For Dependency Injection.
- **VLC Player**: For RTSP streaming.
- **ONVIF**: For camera discovery.

---

## **Project Architecture**
The application is based on **Clean Architecture** principles, providing clear separation between the following layers:

1. **Presentation**:
   - Contains UI widgets, state management (Provider), and navigation logic.
2. **Domain**:
   - Business logic, use cases, and domain entities.
3. **Data**:
   - Repositories, models, and data sources (Firebase and other integrations).

---

## **File Structure**
```plaintext
lib/
├── core/                     # Core utilities and services
│   ├── di/                   # Dependency injection setup
│   ├── errors/               # Error handling utilities
│   ├── utils/                # Common utility functions
├── features/                 # Feature-based modules
│   ├── auth/                 # Authentication module
│   │   ├── data/             # Data sources and models
│   │   ├── domain/           # Entities, repositories, and use cases
│   │   ├── presentation/     # UI and providers
│   ├── stream/               # Streaming module
│   ├── profile/              # User profile management module
├── widgets/                  # Shared widgets
├── main.dart                 # Entry point of the application
```

---

## **Setup and Installation**

### **Step 1: Clone the Repository**
```bash
git clone https://github.com/your-repo/endroid-streaming.git
cd endroid-streaming
```

### **Step 2: Install Dependencies**
```bash
flutter pub get
```

### **Step 3: Configure Firebase**
1. Go to the Firebase Console.
2. Create a project and enable Authentication and Firestore.
3. Download the configuration files:
   - `google-services.json` (for Android)
   - `GoogleService-Info.plist` (for iOS)
4. Place these files in their respective directories:
   - `android/app/google-services.json`
   - `ios/Runner/GoogleService-Info.plist`

### **Step 4: Run the Application**
```bash
flutter run
```

---

## **App Modules**

### **Authentication Module**
- **Data Layer**: Firebase for backend services.
- **Domain Layer**: User entity and authentication use cases.
- **Presentation Layer**: Login and Signup screens.

### **Stream Module**
- **Data Layer**: Firestore for storing streams.
- **Domain Layer**: Business logic for managing streams.
- **Presentation Layer**: Grid layout for streams and dynamic controls.

### **Profile Module**
- **Data Layer**: Firestore integration.
- **Domain Layer**: Profile use cases and entity.
- **Presentation Layer**: Profile screen UI.

---
## Demo
![Demo](assets/screenshots/demo.gif)


## **Screenshots and Previews**

### **Login Screen**
- Secure login with Firebase Authentication.
![LogIn](assets/screenshots/idle_screen.png)

### **Stream Management**
- Dynamic grid layout for managing multiple RTSP streams.
![Stream Management](assets/screenshots/incoming_call_screen.png)

### **Device Discovery**
- ONVIF-based camera discovery for seamless integration.
![Device Discovery](assets/screenshots/in_call_screen.png)

---

## **Contributing**
We welcome contributions! Please follow these steps:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature-name"
   ```
4. Push your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

---

## **License**
This project is licensed under the MIT License. See the LICENSE file for details.

---

## **Contact**
For queries or contributions:
- **Email**: shivamshakya2111@gmail.com
- **GitHub**: https://github.com/Shivu21/Endroid-USA

