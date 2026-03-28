# React Native Expo → APK Build Guide (Revision Document)

This document explains **all commands and steps** used to convert your **React Native Expo app** into an **APK file**.

---

# 1. What is Expo

Expo is a framework used to build **React Native mobile applications** easily.

Benefits:

- No Android Studio required
- Easy setup
- Fast development
- Cloud builds

---

# 2. What is EAS

EAS = Expo Application Services

EAS allows you to:

- Build APK
- Build AAB
- Deploy app
- Manage credentials

---

# 3. Install Required Tools

Install Expo CLI

```
npm install -g expo-cli
```

Install EAS CLI

```
npm install -g eas-cli
```

---

# 4. Login to Expo

Login using terminal

```
eas login
```

OR

```
eas login --browser
```

This connects your local project with Expo cloud.

---

# 5. Configure EAS

Run:

```
eas build:configure
```

This creates:

```
eas.json
```

This file controls build settings.

---

# 6. Install Compatible Dependencies

IMPORTANT (Always use expo install)

```
npx expo install @react-native-async-storage/async-storage
```

This installs compatible version for Expo.

---

# 7. Clear Cache (Recommended)

```
npx expo start -c
```

This clears metro cache.

---

# 8. Build APK

Basic command

```
eas build -p android
```

APK build command

```
eas build -p android --profile preview
```

---

# 9. Build Process

When running build:

You will see prompts:

Generate Android keystore?

Select:

```
YES
```

Expo automatically:

- Creates keystore
- Signs app
- Builds APK

---

# 10. After Build

Expo gives download link:

Example:

```
https://expo.dev/....
```

Download APK

Install in mobile

---

# 11. Change API URL (Production)

Update:

```
src/services/api.ts
```

Example:

```
const BASE_URL = "https://your-api-url.com";
```

---

# 12. Common Errors

### Dependency error

Fix:

```
npx expo install package-name
```

### Gradle error

Fix:

```
npx expo start -c
```

---

# 13. Useful Commands Summary

Install Expo CLI

```
npm install -g expo-cli
```

Install EAS CLI

```
npm install -g eas-cli
```

Login

```
eas login
```

Configure build

```
eas build:configure
```

Install dependency

```
npx expo install package-name
```

Clear cache

```
npx expo start -c
```

Build APK

```
eas build -p android --profile preview
```

---

# 14. Folder Structure (Recommended)

```
app/
src/
components/
services/
```

---

# 15. Final Workflow

1. Build App
2. Upload to Expo
3. Build APK
4. Download APK
5. Install on mobile

---

# 16. Best Practices

- Always use expo install
- Always test before build
- Use hosted API
- Use environment variables

---

# 17. Production Checklist

Before building APK:

- API URL updated
- No localhost
- No console logs
- App name set
- Version updated

---

# 18. Next Steps

You can now:

- Publish to Play Store
- Generate AAB
- Add Splash screen
- Add App icon

---

# End of Document

This document is created for revision and future builds.

