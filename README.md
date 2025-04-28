# Mobile Application Automated Testing with Appium on Linux

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Last Commit](https://img.shields.io/github/last-commit/jonasgil/appium-linux-automation.svg)](https://github.com/jonasgil/appium-linux-automation/commits/main)
[![GitHub Stars](https://img.shields.io/github/stars/jonasgil/appium-linux-automation.svg?style=social)](https://github.com/jonasgil/appium-linux-automation/stargazers)

This project provides a framework for automated testing of mobile applications (both Android and iOS) using Appium on a Linux environment. It aims to streamline the process of writing, executing, and maintaining UI tests for mobile apps, ensuring quality and faster feedback cycles.

## Table of Contents

- [Description](#description)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Test Examples](#test-examples)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## Description

This project leverages Appium, a powerful open-source test automation framework, to interact with mobile application elements in a way that mimics user behavior. By running these tests on a Linux system, we can integrate them into continuous integration and continuous delivery (CI/CD) pipelines efficiently. This framework is designed to be modular and extensible, allowing for easy addition of new test cases and functionalities.

## Prerequisites

Before you can run and contribute to this project, ensure you have the following installed and configured on your Linux computer:

* **Operating System:** Linux Mint 22 Wilma or later (other Debian-based distributions should also work).
* **Java Development Kit (JDK):** Version 21.0.6 or higher.
    ```bash
    sudo su
         apt-get update && apt-get upgrade
         apt-get install default-jdk
    java --version
    ```
* **Android SDK:** Required for testing Android applications. Ensure you have the necessary platform tools and emulator images (if needed).
    * Download and [install](android_installation.md) from [Android Studio](https://developer.android.com/studio).
    * Set up the `ANDROID_HOME` environment variable.
    * Ensure `adb` is in your system's PATH.
* **Node.js and npm:** Required for installing and running the Appium server.
    ```bash
    apt-get update
    apt-get install nodejs && apt-get npm
    node -v
    npm -v
    ```
* **Appium Server:** Install the Appium server globally using npm.
    ```bash
    npm install -g appium
    appium --version
    ```
* **Appium GUI (Appium inspector):** Install the Appium server globally using npm.
    ```bash
    npm install -g appium
    appium --version
    ```
* **Appium GUI (Appium Desktop):** Install the Appium server globally using npm.
    ```bash
    npm install -g appium
    appium --version
    ```
* **Python:** Version 3.6 or higher (example client language).
    ```bash
    sudo apt update
    sudo apt install python3 python3-pip
    python3 --version
    pip3 --version
    ```
* **Python Dependencies:** Install the necessary Python packages.
    ```bash
    pip3 install Appium-Python-Client
    pip3 install pytest  # Example testing framework
    # Add other necessary Python packages here
    ```
* **Physical Device or Emulator:**
    * For Android: A physical Android device with USB debugging enabled or an Android emulator configured via the Android SDK.
    * For iOS (Note: Testing iOS on Linux has limitations and typically requires a connected macOS machine for the WebDriverAgent): While direct iOS testing on Linux is challenging, this framework might include configurations for remote execution or specific workarounds if applicable. Clarify the extent of iOS support in your specific project.

## Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/jonasgil/appium-linux-automation.git](https://github.com/jonasgil/appium-linux-automation.git)
    cd appium-linux-automation
    ```

2.  **Install Python dependencies (if applicable):**
    ```bash
    pip3 install -r requirements.txt
    ```
    *(Note: Create a `requirements.txt` file listing your Python dependencies if you are using Python as your client.)*

## Configuration

1.  **Set up Environment Variables (if needed):**
    You might need to set environment variables like `ANDROID_HOME` or paths to your application files. Refer to the specific configuration files in the project.

2.  **Configure Desired Capabilities:**
    The desired capabilities for interacting with your mobile applications are typically defined in your test scripts or a configuration file. Ensure these are correctly set for your target device or emulator (e.g., `platformName`, `deviceName`, `appPackage`, `appActivity` for Android). Example in Python:
    ```python
    desired_caps = {
        'platformName': 'Android',
        'deviceName': 'emulator-5554',  # Replace with your device or emulator name
        'appPackage': 'com.example.myapp',
        'appActivity': '.MainActivity'
    }
    ```

3.  **Application Paths:**
    Ensure the paths to your `.apk` (Android) or `.ipa` (iOS, if supported) files are correctly specified in your configuration or test scripts.

## Usage

1.  **Start the Appium Server:**
    Open a new terminal and start the Appium server.
    ```bash
    appium
    ```

2.  **Run the Tests:**
    Navigate to the project directory in another terminal and execute your test scripts. For example, if you are using pytest with Python:
    ```bash
    pytest tests/
    ```
    *(Adjust the command based on your chosen testing framework and the location of your test files.)*

3.  **View Test Results:**
    The test results will be displayed in the terminal. You might also have reports generated depending on your testing framework configuration.

## Project Structure
