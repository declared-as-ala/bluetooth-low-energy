# React Native BLE Heart Rate Monitor App (Expo + BLE)

A React Native project using **Expo** and **Bluetooth Low Energy (BLE)** to connect with heart rate monitor devices like the Elite HRV. This project demonstrates how to scan, connect, and read data (e.g., heart rate) from a BLE peripheral using modern Expo workflows.

---
![1](https://github.com/user-attachments/assets/37d229c1-7175-4ab0-9a2a-796ead0583e8)


## 🚀 Features

- 📱 Built with **Expo + TypeScript**
- 📡 Connects to BLE heart rate monitors (or other BLE devices)
- 🔒 Handles Android and iOS Bluetooth permission logic
- 🔄 Scans for devices and filters duplicates
- 📊 Streams real-time heart rate data
- 🧠 Clean modular code using hooks (`useBLE`)
- 🎨 Includes optional animation using `react-native-skia`

---

## 📦 Tech Stack

- [`react-native-ble-plx`](https://github.com/dotintent/react-native-ble-plx)
- Expo EAS (for custom dev client with BLE support)
- `expo-device`, `react-native-base64`
- `react-native-skia` (for UI animations)

---

## 🛠️ Setup Instructions

### 1. Create Project

```bash
npx create-expo-app ble-heart-rate --template expo-template-blank-typescript
cd ble-heart-rate
2. Install Dependencies
bash
Copy
Edit
npx expo install expo-device
npm install --save react-native-ble-plx react-native-base64
npm install --save-dev @config-plugins/react-native-ble-plx
npm install react-native-skia
3. Add eas.json for custom Expo build
json
Copy
Edit
{
  "cli": {
    "version": ">= 2.0.0"
  },
  "build": {
    "development": {
      "developmentClient": true,
      "distribution": "internal"
    },
    "preview": {},
    "production": {}
  }
}
4. Configure Plugins in app.json
json
Copy
Edit
{
  "expo": {
    "name": "BLEHeartRate",
    "slug": "ble-heart-rate",
    "plugins": ["@config-plugins/react-native-ble-plx"],
    "sdkVersion": "EXPO_SDK_VERSION"
  }
}
🔁 Replace EXPO_SDK_VERSION with the actual version you're using, e.g., 54.0.0.
