# <p align="center"> Expo React Native Starter </p>

<p align="center"> 
A beginner-friendly starter repository for learning <b>React Native</b> using <b>Expo</b>. </p>
  
---

## What is React Native?

**React Native** is a JavaScript framework used to build **mobile applications for Android and iOS** using a single codebase.  
It is based on **React**, allowing developers to use components and reusable logic to create native mobile apps.

### Why React Native is used
- One codebase for Android and iOS
- Faster development cycle
- Strong community and ecosystem
- Uses JavaScript and React concepts

---

## What is Expo?

**Expo** is a development platform that simplifies `React Native` development, especially for beginners.  
It removes complex native setup and provides tools to run apps quickly on real devices.

### Why Expo is recommended
- Easy and fast setup
- No need for Android Studio at the beginning
- Run apps instantly using Expo Go
- Built-in APIs (camera, media, storage, etc.)

---

## Prerequisites

Before starting, make sure you have:

- **Node.js (LTS version recommended)**
- A code editor (recommended: **VS Code**)
- An **Android device** with the **Expo Go** app installed

---

## Recommended Setup and Run (Beginner Friendly)

This is the **recommended and simplest method** to create and run a React Native app using Expo.

---

### Step 1: Create an Expo app

Open your terminal and run:

```bash
npx create-expo-app@latest
# Or, if you want to create the app inside the current folder:
npx create-expo-app@latest ./
```

Then move into the project directory:

```bash
cd your-project-name
```
### Step 2: Install Expo Go on your mobile
1. Open Google Play Store
2. Search for Expo Go
3. Install the app
4. Open Expo Go and log in (optional but recommended)

### Step 3: Start the development server
Run the following command in your project folder:
```bash
npx expo start
```
This will start the Expo development server and display a `QR code` in the terminal or browser.

### Step 4: Run the app on your Android device
1. Open Expo Go on your mobile phone
2. Scan the QR code shown in the terminal or browser
3. The app will automatically run on your device

--- 
## Other Ways to Run the App

### Option 1: Run on Android Emulator
You can also run the app using an Android Emulator: 
`Install Android Studio`
Create and start an Android Virtual Device (AVD)
Run:
```bash
npx expo start
```
Press a in the terminal to open the app in the emulator

### Option 2: Expo Dev Client (Advanced)
`Expo Dev` Client is used when your app needs custom native modules.<br>
This approach is more advanced and not required for beginners.

### Option 3: React Native CLI (Not recommended for beginners)
React Native can also be set up without Expo, but it requires:
- Manual Android Studio setup
- More configuration
- Native build knowledge

This approach is recommended only for advanced users.

---
## Common Commands

Start Expo development server:
```bash
npx expo start
```
Install dependencies:
```bash
npm install
```
Clear Expo cache (if errors occur):
```bash
npx expo start -c
```
---
## Troubleshooting
PowerShell script execution error (Windows)

If you see an error like:
```lua
npx.ps1 cannot be loaded because running scripts is disabled
```
Open PowerShell as Administrator and run:
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
Then retry the command.
