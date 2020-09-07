# Analytics Microbytes
A analytics library for tracking page views, custom events, & identify visitors.

## Installation
Use the package manager [npm](https://www.npmjs.com/) to install Analytics Microbytes.

```
npm install analytics-mirobytes
```

## Usage
```
import Analytics from "analytics-mirobytes";


/* Initialize Analytics */

const analytics = new Analytics("API_KEY_OF_YOUR_PROJECT");

/* Track Page View */
 
    window.analytics.page({
      userId: "userId-abc"
    });
  
  
/* Track Custom Events */
    window.analytics.track({
      userId: "userId-abc",
      event: "Registration Button Clicked"
    });
    
 /* Identify a visitor */
    window.analytics.identify({
      userId: "userId-abc",
      traits: {
        name: "username",
        email: "useremail",
        plan: "Enterprise",
        friends: 42
      },
    });

```

## Use in React Web App
To use this analytics in your react web app, you first have to initialize it into your index.js file

```
import React from "react";
import ReactDOM from "react-dom";
import App from "./App";
import Analytics from "analytics-mirobytes";


window.analytics = new Analytics("8041d345-dbec-4a36-bf6d-a75d497970ab");

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById("root")
);
```
