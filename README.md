# Setting Up a React Native Environment for Mobile Development

---

## 1. Installation Instructions

To build a React Native application, set up these core dependencies on your local machine. Using a framework like **Expo** is recommended to streamline the process.

### Node.js

Node.js is the runtime that executes your JavaScript code.

- **Download**: [Node.js LTS version](https://nodejs.org/)
- **Verify Installation**: Open your terminal and run:
  ```bash
  node -v
  npm -v
  ```

(Successful installation will display version numbers for both.)

### Expo CLI

Expo tools are managed via `npx`, so a global install is usually unnecessary.

- **Check Availability**:
  ```bash
  npx expo-cli --version
  ```

### Android Studio & Emulator

To test your app on an Android device:

- **Download**: [Android Studio](https://developer.android.com/studio)
- **SDK Setup**: During installation, ensure the following are selected:
  - Android SDK
  - Android SDK Platform
  - Android Virtual Device
- **Virtual Device (Emulator)**:
  1. Open Android Studio → **More Actions** → **Virtual Device Manager**.
  2. Click **Create Device**, select a phone (e.g., Pixel 7).
  3. Download a system image (e.g., API 34) and finish setup.

---

## 2. Configuration Steps

Proper configuration ensures your terminal can access the Android SDK.

### Environment Variables (Windows)

1. Search for **"Edit the system environment variables"**.
2. Click **Environment Variables**.
3. Under **User variables**, click **New**:
   - **Variable name**: `ANDROID_HOME`
   - **Variable value**: `C:\Users\[YourUsername]\AppData\Local\Android\Sdk`
4. Edit the **Path** variable and add:
   - `%ANDROID_HOME%\platform-tools`
   - `%ANDROID_HOME%\emulator`

### VS Code Setup

Use **Visual Studio Code** with the **"ES7+ React/Redux/React-Native snippets"** extension for a better workflow.

---

## 3. Project Creation

1. Navigate to your desired folder in the terminal.
2. Run:
   ```bash
   npx create-expo-app@latest {appName}
   ```
3. Move into the project directory:
   ```bash
   cd {appName}
   ```

---

## 4. Running the Project

1. **Start the Expo server**:
   ```bash
   npx expo start
   ```
2. **Launch the app**:
   - **Android Emulator**: Press `a` (ensure the emulator is open).
   - **Web**: Press `w`.
   - **Physical Device**: Download **Expo Go** on your phone, scan the QR code in the terminal, and ensure your PC and phone are on the same Wi-Fi network.

---

## 5. Troubleshooting

| Issue             | Solution                                                              |
| ----------------- | --------------------------------------------------------------------- |
| Command Not Found | Ensure Node.js is installed and restart your terminal.                |
| Wrong Directory   | Use `cd` to navigate to the project folder containing `package.json`. |
| Port Busy         | Use: `npx expo start --port 8082`                                     |
| Permissions Error | On Windows, run PowerShell as Admin and use:                          |
|                   | `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned`                   |
| App Doesn’t Run   | Run `npm install` to ensure all dependencies are installed.           |

---

## 6. Reset the Project

- **Command**:
  ```bash
  npm run reset-project
  ```
- **What it does**: Clears the default "boilerplate" code (pre-made tabs and example screens) from the Expo template. Files are moved to an `app-example` folder, or you can delete them.

---

## 7. Resources

- [React Native Docs](https://reactnative.dev/docs/getting-started)
- [Expo Docs](https://docs.expo.dev/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Stack Overflow: React Native](https://stackoverflow.com/questions/tagged/react-native)

