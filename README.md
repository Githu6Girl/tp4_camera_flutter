# 📸 Flutter Camera App - TP4

**USTHB - Faculté Informatique | Dept. ID&SD**  
**Module:** Développement Mobile  
**Étudiante:** Meriem Saiki | **Matricule:** 232331454607

---

## 📱 Description

A Flutter mobile application that allows users to take pictures using the device camera and display the captured photo on a new screen.

---

## ✨ Features

- 🎥 Live camera preview on launch
- 📷 Take a photo with one button tap
- 🖼️ Display the captured image on a new screen
- 🔙 Navigate back to the camera

---

## 🗂️ Project Structure

```
lib/
└── main.dart           # Main app + TakePictureScreen + DisplayPictureScreen
pubspec.yaml            # Dependencies
```

---

## 📦 Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  camera: latest
  path_provider: latest
  path: latest
```

Install with:
```bash
flutter pub add camera
flutter pub add path_provider
flutter pub add path
flutter pub get
```

---

## 🏗️ App Structure

### `main()`
- Initializes Flutter bindings
- Fetches available cameras with `availableCameras()`
- Passes the first camera to `TakePictureScreen`

### `TakePictureScreen` (StatefulWidget)
- Initializes `CameraController` with `ResolutionPreset.medium`
- Displays live feed using `CameraPreview`
- Uses `FutureBuilder` to show a loading spinner until camera is ready
- `FloatingActionButton` triggers photo capture

### `DisplayPictureScreen` (StatelessWidget)
- Receives the image file path
- Displays the photo using `Image.file(File(imagePath))`

---

## 📸 Screenshots

👉 [View Screenshots on Google Drive](https://drive.google.com/drive/folders/1Aa2ukE49yZh_uMrja2ACzvuyLrq6YDzL?usp=sharing)

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/Githu6Girl/tp4_camera_flutter.git
cd tp4_camera_flutter

# Install dependencies
flutter pub get

# Run on Android device or emulator
flutter run
```

> ⚠️ Camera does **not** work on Flutter Web. Use an Android emulator or a real device.

---

## 🛠️ Built With

- [Flutter](https://flutter.dev/)
- [camera](https://pub.dev/packages/camera)
- [path_provider](https://pub.dev/packages/path_provider)
- [path](https://pub.dev/packages/path)
