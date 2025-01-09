# **Endroid Streaming App**

## **Overview**
The **Endroid Streaming App** is a cutting-edge Flutter application built for real-time streaming, device management, and user authentication. It follows **Clean Architecture** principles, incorporates **Firebase** for backend services, uses **Provider** for state management, and **GetIt** for dependency injection. The app allows users to manage multiple RTSP streams efficiently and includes features like dynamic grid layouts, ONVIF device discovery, and custom UI components.

---

## **Table of Contents**
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Architecture](#project-architecture)
- [File Structure](#file-structure)
- [Setup and Installation](#setup-and-installation)
- [App Modules](#app-modules)
- [State Management](#state-management)
- [Pagination](#pagination)
- [Screenshots and Previews](#screenshots-and-previews)
- [Contributing](#contributing)
- [License](#license)

---

## **Features**
- **Authentication**:
  - Firebase Authentication for secure login, signup, and logout.
- **Real-Time Streaming**:
  - RTSP streaming with VLC Player integration.
  - Support for managing multiple streams.
- **Device Management**:
  - Discover ONVIF cameras.
  - Add devices manually or through QR code scanning.
- **State Management**:
  - Reactive state updates using Provider.
  - Dependency injection with GetIt.
- **Clean Architecture**:
  - Layered design for scalability and maintainability.
- **Pagination for Streams**:
  - Lazy loading of stream data for better performance.
- **Custom UI Components**:
  - Loading animations with **Flutter Spinkit**.
  - Snackbars with **Awesome Snackbar Content**.
- **Responsive Design**:
  - Adaptive layouts for different screen sizes and resolutions.

---

## **Technologies Used**
- **Flutter**: For building cross-platform UI.
- **Firebase**: Backend services for authentication and Firestore.
- **Provider**: State management library.
- **GetIt**: Dependency injection for decoupled modules.
- **VLC Player**: RTSP streaming library.
- **ONVIF**: Camera discovery protocol.

---

## **Project Architecture**

### **Clean Architecture**
The project adheres to **Clean Architecture** to ensure scalability, maintainability, and testability:

1. **Presentation Layer**:
   - Contains UI components, state management (via Provider), and navigation logic.
2. **Domain Layer**:
   - Includes business logic, use cases, and domain entities.
3. **Data Layer**:
   - Comprises repositories, models, and data sources for interacting with Firebase and other APIs.

---

## **File Structure**
```plaintext
lib/
├── core/                     # Core utilities and services
│   ├── di/                   # Dependency injection setup
│   ├── utils/                # Utility functions and helpers
├── features/                 # Feature-based modules
│   ├── auth/                 # Authentication module
│   │   ├── data/             
│   │   │   ├── datasources/  # Remote and local data sources
│   │   │   ├── models/       # Firebase models
│   │   ├── domain/           
│   │   │   ├── entities/     # Core business objects
│   │   │   ├── usecases/     # Business logic
│   │   ├── presentation/     
│   │       ├── screens/      # Login and signup screens
│   │       ├── providers/    # Auth state management
│   ├── stream/               
│   │   ├── data/             
│   │   ├── domain/           
│   │   ├── presentation/     
│   ├── profile/              
│       ├── data/             
│       ├── domain/           
│       ├── presentation/     
├── widgets/                  
│   ├── custom_snackbar.dart  # Reusable snackbar widgets
│   ├── stream_grid_view.dart # Stream grid rendering
│   ├── action_buttons.dart   # Common action buttons
├── main.dart                 # App entry point
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
2. Set up a project and enable Authentication and Firestore.
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
- **Data Layer**: Firebase integration for authentication.
- **Domain Layer**: Use cases for login, signup, and logout.
- **Presentation Layer**: Login and signup screens with Provider for state management.

### **Stream Module**
- **Data Layer**: Firestore integration for managing streams.
- **Domain Layer**: Use cases for handling stream CRUD operations.
- **Presentation Layer**: Dynamic grid layout for streams with VLC Player integration.

### **Profile Module**
- **Data Layer**: Firestore integration for user profiles.
- **Domain Layer**: Business logic for profile updates.
- **Presentation Layer**: Profile management screens.

---

## **State Management**
The app uses Provider for reactive state updates:

- **AuthProvider**: Manages user authentication.
- **StreamProvider**: Handles stream data and CRUD operations.
- **ProfileProvider**: Manages user profile information.

---

## **Pagination**
Lazy loading is implemented for efficient loading of stream data:

```dart
LazyLoadScrollView(
  onEndOfPage: _loadMoreStreams,
  child: GridView.builder(
    itemCount: streams.length,
    gridDelegate: const SliverGridDelegateWithFixedCrossAxisCount(
      crossAxisCount: 2,
      crossAxisSpacing: 8,
      mainAxisSpacing: 8,
    ),
    itemBuilder: (context, index) {
      return StreamCard(stream: streams[index]);
    },
  ),
);
```

---

## **Screenshots and Previews**

### **Login Screen**
- A secure and intuitive interface for user authentication.

### **Stream Management**
- Manage multiple streams with a dynamic grid layout.

### **Device Discovery**
- Discover ONVIF cameras seamlessly.

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
- **GitHub**: Shivu21

