# API Reference
To start Posting Server Count stats to your Bots Page follow the steps below.

# Step 1
Go to your bot edit page, and click the Authorization Token link at the bottom of the page. This will generate an auth token.

# Step 2
Edit and add one of the Templates below to your bots "Ready Event"

# NodeJS Reference
```jsx harmony
var myHeaders = new Headers();
myHeaders.append("authorization", "YOUR_AUTH_TOKEN");
myHeaders.append("Content-Type", "application/json");

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: JSON.stringify({"server_count": 1500}); // Replace this number with the server count
};

fetch("/api/auth/stats/:botid", requestOptions) // Make sure you include the domain
  .then(response => response.text())
  .then(console.log)
  .catch(console.error);
  ```
