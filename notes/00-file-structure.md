# File structure

## `tsconfig.json`
Contains the rules that TypeScript will use to enforce type safety throughout the project.

---

## `package.json`
The **package.json** file contains the project's dependencies, scripts, and metadata. Anytime a new dependency is added to your project, it will be added to this file.

---

## `app.json`
Contains configuration options for the project and is called the app config. These options change the behavior of your project while developing, building, submitting, and updating your app.
```json
{
  "expo": {
    // display name users see under the app icon on their phone
    "name": "expo-react-native-starter",
    // project identifier used by Expo internally
    "slug": "expo-react-native-starter",
    "version": "1.0.0",
    // Locks the app to portrait mode.
    // If you set "default", it can rotate.
    "orientation": "portrait",
    // main app icon image file used by iOS/Android builds
    "icon": "./assets/images/icon.png",
    // This is for deep linking (opening your app via a link like):
    // exporeactnativestarter://topics/a-components
    // Expo Router uses this for routing and linking.
    "scheme": "exporeactnativestarter",
    // Light mode / Dark mode
    "userInterfaceStyle": "automatic",
    "newArchEnabled": true,
    "ios": {
      "supportsTablet": true
    },
    "android": {
      "adaptiveIcon": {
        "backgroundColor": "#E6F4FE",
        "foregroundImage": "./assets/images/android-icon-foreground.png",
        "backgroundImage": "./assets/images/android-icon-background.png",
        "monochromeImage": "./assets/images/android-icon-monochrome.png"
      },
      "edgeToEdgeEnabled": true,
      "predictiveBackGestureEnabled": false
    },
    "web": {
      "output": "static",
      "favicon": "./assets/images/favicon.png"
    },
    "plugins": [
      "expo-router",
      [
        "expo-splash-screen",
        {
          "image": "./assets/images/splash-icon.png",
          "imageWidth": 200,
          "resizeMode": "contain",
          "backgroundColor": "#ffffff",
          "dark": {
            "backgroundColor": "#000000"
          }
        }
      ]
    ],
    "experiments": {
      "typedRoutes": true,
      "reactCompiler": true
    }
  }
}
```
---
## `scripts`
Contains **reset-project.js**, which can be run with `npm run reset-project`. This script will move the app directory to app-example, and create a new app directory with an index.tsx file.

---

## `hooks`
Contains React Hooks, which allows sharing common behavior between components. For example, `useThemeColor()` is a hook that returns a color based on the current theme.

---

## `constants`
Contains **Colors.ts**, which contains a list of color values throughout the app.

---

## `components`
Contains React Native components, like **ThemedText.tsx**, which creates text elements that use the app's color scheme in light and dark modes.

---

## `app`
Contains the app's navigation, which is file-based. The file structure of the **app** directory determines the app's navigation.

The app has two routes defined by two files: **app/(tabs)/index.tsx** and **app/(tabs)/explore.tsx**. The layout file in **app/(tabs)/_layout.tsx** sets up the tab navigator.

---