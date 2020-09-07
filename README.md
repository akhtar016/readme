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
