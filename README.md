# Tesla Website Replica

This repository contains a Tesla-inspired website built with React.
It includes core pages, customization logic, and a simple authentication system.

---

## Features

* **Home Page** with hero sections for Model S and Model 3.
* **Cars Page** listing available models with images, price, and specs.
* **Customize Page** where the user can:

  * Select battery, paint, wheels, and interior.
  * See live price calculation.
  * View live preview with readable text on both light and dark paint colors.
* **Authentication** (Signup / Login) using in-memory state.
* **Responsive Layout** suitable for desktop and mobile screens.
* **Fixed Header** with navigation and user session handling.

---

## Notes

* Authentication is temporary and stored in memory using `btoa`. This is **not secure** and only for demonstration.
* Car images are linked from Tesla’s public assets for demo purposes.
* This project is purely educational and not affiliated with Tesla.

---

## Requirements

* Node.js (v16 or later recommended)
* npm (v8 or later) or yarn

---

## How to Run

1. Create a new React project (if not already done):

```bash
npx create-react-app tesla-website
cd tesla-website
```

2. Replace the contents of `src/App.js` (or `src/App.jsx`) with the code from this repository. This repo has App.js

3. Update `src/index.js` if using `App.jsx`:

```js
import React from 'react';
import ReactDOM from 'react-dom/client';
import TeslaApp from './App'; // or App.jsx
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<TeslaApp />);
```

4. Run the project:

```bash
npm install
npm start
```

5. Open `http://localhost:3000` in your browser.

---

## Repository Structure (suggested)

```
/src
  App.js            # main React component (single-file)
  index.js
  index.css
  /assets            # (optional) local images
  /components        # (optional) split Header, HomePage, CarsPage etc.
  /data              # (optional) car data
```

---

## Testing

* Open the app and navigate to **Home**.
* Click **Custom Order** to open the customization page.
* Switch between paint, battery, wheels, and interior options to see price and preview updates.
* Try white and black paint to confirm text contrast works properly.
* Use the signup/login page to test authentication flow.

---

## Improvements (future work)

* Replace in-memory authentication with backend + database.
* Use `react-router` for proper page navigation.
* Store car data in a separate file.
* Add unit tests.
* Replace Tesla hotlink images with local images.

---

