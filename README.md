# Lab Activity 1: Discussion

### 1. Activity Lifecycle During Screen Rotation

When the screen is rotated, Android usually destroys and recreates the current Activity to adjust the layout to the new screen orientation. Lifecycle methods such as `onPause()`, `onStop()`, `onDestroy()`, and `onCreate()` may be triggered. The application can preserve temporary information using `onSaveInstanceState()` and restore it when the Activity is recreated.

### 2. Activity Lifecycle When Pressing the Home Button

When the Home button is pressed, the application moves into the background. The Activity usually calls `onPause()` followed by `onStop()`. When the user returns to the application, `onRestart()`, `onStart()`, and `onResume()` may be called if the Activity was stopped but not destroyed.

### 3. How Logcat Helped Verify Lifecycle Events

Logcat helped monitor the sequence of Activity lifecycle callbacks. By filtering the logs using the application tag, it was easier to identify which methods were executed during application startup, screen rotation, and background transitions.

### 4. Setup and Gradle Sync Issues

During the setup, Android Studio required Gradle synchronization to download and configure the necessary project dependencies. Git was also used to manage the project files and upload the completed laboratory activity to GitHub.

### 5. Enhancements Implemented

The application was enhanced to display the current application ID and the active laboratory room, CompLab 1, in the header. A Clear Log button was also added to remove the displayed lifecycle trace while maintaining proper state handling during screen rotation.