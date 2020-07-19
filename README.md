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
  /* 
   * Replace "1500" With your server count to update manually or
   * Add something along the lines of "client.guilds.size" for (Discord.JS v11)
   */
  body: JSON.stringify({"server_count": 1500}); 

fetch("https://paradisebots.net/api/auth/stats/:botid", requestOptions)
  .then(response => response.text())
  .then(console.log)
  .catch(console.error);
  ```
