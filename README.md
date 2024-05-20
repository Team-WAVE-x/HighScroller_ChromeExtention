## Overview

Overview
The HighScroller Chrome Extension is designed to enhance your browsing experience by offering a unique and interactive interface when using the Google Chrome browser. The project sets up a window with specific dimensions as part of its functionality.

##
## Features

Features
- **Launch Listener**: Listens for when the app is launched and creates a dedicated window.
- **Customizable Window**: Sets up a window with specified dimensions (`800x600`).

##
## Installation Instructions

Installation Instructions
To install and set up the HighScroller Chrome Extension, follow these steps:

1. **Clone the Repository**
   - Open your terminal or command prompt.
   - Execute the following command to clone the repository:
     ```sh
     git clone https://github.com/Team-WAVE-x/HighScroller_ChromeExtension.git
     ```
   - Navigate to the cloned directory:
     ```sh
     cd HighScroller_ChromeExtension
     ```

2. **Load the Extension in Chrome**
   - Open Google Chrome browser.
   - Navigate to `chrome://extensions/`.
   - Enable "Developer mode" on the top right corner of the page.
   - Click on "Load unpacked" and select the cloned directory (`HighScroller_ChromeExtension`).

##
## Usage Examples

Usage Examples
Once the extension is loaded in your browser, it will automatically react to launch events as configured in the code.

Example usage:
- Launching the extension will create a new window with the specified dimensions.

##
## Code Summary

Code Summary
The project consists primarily of a single JavaScript file:

### File: `background.js`
**Content:**
```javascript
/**
 * Listens for the app launching, then creates the window.
 *
 * @see http://developer.chrome.com/apps/app.runtime.html
 * @see http://developer.chrome.com/apps/app.window.html
 */
chrome.app.runtime.onLaunched.addListener(function(launchData) {
  chrome.app.window.create(
    'index.html',
    {
      id: 'mainWindow',
      innerBounds: {
        'width': 800,
        'height': 600
      }
    }
  );
});
```
- This file sets up an event listener to detect when the app is launched. Upon launch, it creates an app window that loads `index.html` with dimensions 800x600 pixels.

##
## License

License
This project is licensed under the MIT License.
```

This Markdown file provides a comprehensive readme for the HighScroller Chrome Extension project, outlining all the necessary information for users or developers who wish to understand, install, and use the project.