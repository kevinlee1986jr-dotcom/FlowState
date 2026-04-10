# FlowState

## Description

FlowState is a productivity application designed to help users achieve a state of deep focus and concentration by blocking distracting websites and applications for a predetermined amount of time. It aims to eliminate procrastination and enhance workflow, enabling users to complete tasks more efficiently. FlowState is ideal for students, writers, programmers, and anyone who needs to focus intensely on their work.

## Features

*   **Website Blocking:** Create custom lists of websites to block during focus sessions.
*   **Application Blocking:** Block access to distracting applications on your computer.
*   **Timer-Based Sessions:** Set specific durations for your focus sessions, ranging from minutes to hours.
*   **Strict Mode (Optional):** Once a session starts in strict mode, it cannot be interrupted, enforcing unwavering focus.
*   **Customizable Blocklists:** Easily add, remove, or edit websites and applications within your blocklists.
*   **Session History:** Track your focus session history, including start and end times, duration, and websites blocked.
*   **Notification System:** Receive notifications when a focus session begins, ends, or when you attempt to access a blocked resource.
*   **Break Reminders:** Schedule short break reminders to prevent burnout and maintain optimal focus.
*   **Cross-Platform Compatibility:** Available on macOS, Windows, and Linux (details in Installation).
*   **Light & Dark Mode:** User-selectable light and dark themes for comfortable use in any environment.
*   **Statistics:** Track your total focused time, longest streak, and other productivity metrics.

## Technologies Used

*   **Frontend:**
    *   React (JavaScript library for building user interfaces)
    *   Redux (State management library for React)
    *   Material UI (React UI framework)
    *   HTML5
    *   CSS3
*   **Backend:**
    *   Node.js (JavaScript runtime environment)
    *   Express.js (Web application framework for Node.js)
    *   MongoDB (NoSQL database for storing user data and session history)
*   **Desktop Application Framework (if applicable):**
    *   Electron (For cross-platform desktop application development - macOS, Windows, Linux) *OR*
    *   Tauri (For cross-platform desktop application development with Rust backend - macOS, Windows, Linux) *OR*
    *   Qt (C++ framework with Python bindings available)
*   **Operating System Specific APIs:**
    *   macOS: `NetworkExtension`, `Screen Recording` (for application blocking, if applicable), `UserNotifications`
    *   Windows: `Windows Filtering Platform (WFP)`, `AppLocker` (for application blocking if applicable), `Toast Notifications`
    *   Linux: `iptables`, `X11` (for application blocking, if applicable), `libnotify`
*   **Other Dependencies:**
    *   Axios (HTTP client for making API requests)
    *   bcrypt (Password hashing library)
    *   jsonwebtoken (JSON Web Token for authentication)
    *   moment.js (JavaScript library for parsing, validating, manipulating, and formatting dates)

## Installation

**Prerequisites:**

*   Node.js and npm (Node Package Manager) installed (recommended version: >= 16.0.0)
*   MongoDB installed and running (local or cloud-based)
*   (If using Electron/Tauri/Qt) Ensure the necessary build tools for your platform are installed (e.g., Xcode for macOS, Visual Studio Build Tools for Windows, build-essential for Linux). Specific instructions are provided for each platform below.

**Steps:**

1.  **Clone the repository:**

    ```bash
    git clone [repository URL]
    cd FlowState
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Configure the environment:**

    *   Create a `.env` file in the root directory.
    *   Add the following environment variables (replace with your actual values):

        ```
        MONGODB_URI=[your MongoDB connection string]
        JWT_SECRET=[your secret key for JWT]
        NODE_ENV=development  # or production
        PORT=3000 # or any other available port
        ```

4.  **Run the application:**

    *   **Development Mode:**

        ```bash
        npm run dev
        ```

        This command typically starts the application with hot-reloading and debugging support.

    *   **Production Mode:**

        ```bash
        npm run build  # Build the application
        npm start      # Start the application
        ```

    **Platform-Specific Instructions (if applicable):**

    *   **macOS:**
        *   Ensure Xcode and Command Line Tools are installed.
        *   If using Electron/Tauri, follow the specific instructions in their respective documentation for macOS builds.

    *   **Windows:**
        *   Install Visual Studio Build Tools with the necessary C++ workload.
        *   If using Electron/Tauri, follow the specific instructions in their respective documentation for Windows builds. You may need to run the installer with administrator privileges.

    *   **Linux:**
        *   Install `build-essential` and other necessary dependencies using your distribution's package manager (e.g., `sudo apt-get install build-essential` on Debian/Ubuntu-based systems).
        *   If using Electron/Tauri, ensure you have the required dependencies for building native modules.

5.  **Executable Creation (if applicable):**

    If using Electron/Tauri, use the provided scripts in `package.json` (e.g., `npm run package-mac`, `npm run package-win`, `npm run package-linux`) to create platform-specific executables. Refer to the Electron/Tauri documentation for advanced packaging options.

**Troubleshooting:**

*   **Dependency Installation Errors:** Double-check that Node.js and npm are installed correctly and that you have the required build tools for your platform. Try clearing the npm cache (`npm cache clean --force`) and reinstalling the dependencies.
*   **MongoDB Connection Errors:** Verify that MongoDB is running and accessible from your machine. Ensure that the `MONGODB_URI` in your `.env` file is correct.
*   **Application Blocking Issues:** Ensure that FlowState has the necessary permissions to block applications and websites on your operating system. This may involve granting accessibility permissions or administrator privileges. Consult the documentation for your operating system and the chosen technology.
*   **Build Errors:** If you encounter build errors during the `npm run build` or `npm run package-*` commands, consult the documentation for Electron/Tauri/Qt for troubleshooting specific build issues on your platform.

## Usage

1.  Launch the FlowState application.
2.  Create an account or log in.
3.  Create or edit blocklists by adding websites and/or applications.
4.  Set the duration for your focus session.
5.  Choose whether to enable "Strict Mode".
6.  Start the focus session.
7.  During the session, FlowState will block access to the specified websites and applications.
8.  You will receive notifications when the session begins, ends, or if you attempt to access a blocked resource.
9.  Review your session history and statistics to track your progress.

## Contributing

We welcome contributions to FlowState! Please follow these guidelines:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Implement your changes and write thorough tests.
4.  Submit a pull request with a clear description of your changes.

## License

[Choose a License - e.g., MIT License]

Copyright (c) [Year] [Your Name/Organization]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.