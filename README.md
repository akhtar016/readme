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
      userId: "USER_ID_OF_YOUR_USER"
    });
  
  
/* Track Custom Events */
    window.analytics.track({
      userId: "userId-abc",
      event: "Registration Button Clicked"
    });
    
 /* Identify a visitor */
    window.analytics.identify({
      userId: "USER_ID_OF_YOUR_USER",
      traits: {
        name: "NAME_OF_YOUR_USER",
        email: "EMAIL_OF_YOUR_USER",
        plan: "Enterprise",
        friends: 42
      },
    });

```

## Use in React Web App
After installing the analytics, to use this analytics in your react web app, you first have to initialize it into your index.js file

```
import React from "react";
import ReactDOM from "react-dom";
import App from "./App";
import Analytics from "analytics-mirobytes";


window.analytics = new Analytics("YOUR_PROJECT_API_KEY");

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById("root")
);
```
Now the initialization is done. 

To track pages, you have to use the follwing code -
```
  useEffect(() => {
    window.analytics.page({
      userId: "USER_ID_OF_YOUR_USER"
    });
  }, []);
```

To track event (e.g button click), you have to use the following code - 

```
    window.analytics.track({
      userId: "USER_ID_OF_YOUR_USER",
      event: "Registration Button Clicked"
    });
```

For identifying user, you have to use the following code - 

    window.analytics.identify({
      userId: "USER_ID_OF_YOUR_USER",
      traits: {
        name: "NAME_OF_YOUR_USER",
        email: "EMAIL_OF_YOUR_USER",
        plan: "Enterprise",
        friends: 42
      },
    });

NOTE: Don't forget to add the property userId in the object.
