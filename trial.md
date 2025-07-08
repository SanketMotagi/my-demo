## Code Breakdown

### 1. `index.htm`

This is the main HTML file for the web interface.

* Displays the project title and logo
* Lets users:

  * Select their gender
  * Upload or capture three types of images: happy face, serious face, and body
* Includes buttons to capture images using the webcam
* Calls JavaScript functions to handle capture and submit data
* Displays results returned from the backend

---

### 2. `style.css`

This file styles the web page to look modern and visually appealing.

* Applies gradients, blur effects, and card-style sections
* Styles elements like buttons, input fields, captions, videos, and countdown overlays
* Uses Google Fonts for better typography
* Ensures consistent look and feel across all sections

---

### 3. `script.js`

Handles all the logic in the browser using JavaScript.

* Uses the webcam to capture images after a 5-second countdown
* Converts captured images to base64 format
* Sends the images and gender to the Flask backend via a POST request
* Displays the results (emotion, symmetry, and body scores) returned from the server
* Handles webcam errors and provides user feedback via alerts and messages

---

### 4. `server.py`

This is the backend server built with Flask.

* Accepts POST requests at `/analyze_images`
* Stores the incoming images and gender in `config.py` variables
* Runs external scripts (`emotion.py`, `symmetry.py`) to compute scores
* Returns the results as a JSON response
* Includes a test route `/get_variables` to return stored values

---

Let me know if you want a matching breakdown for `emotion.py`, `symmetry.py`, or `config.py`.
