# News Central

News Central is a web application inspired by BBC News that allows users to search and read news articles from various categories. Whether you're interested in current events, sports, travel, or culture, News Central provides a platform to stay informed and explore news topics of your choice.

## Features

• Search Functionality: Users can search for news articles using keywords, allowing them to find articles on specific topics or events.

• Category Navigation: Different categories such as general news, sports, travel, and culture are available for users to browse through.

• Interactive Interface: The application provides a user-friendly interface with tabs for each category and interactive elements for reading articles and watching videos.

## Setup Locally
To set up News Central locally on your machine, follow these steps:

```vscode terminal
npm install ws
```
## Opt-in for performance
bufferutil is an optional module that can be installed alongside the ws module:
```
npm install --save-optional bufferutil
```

## Navigate to the Directory:
Move into the directory containing the project files:
```vscode terminal
cd news-server
```
## Obtain API Keys: 
You will need API keys for the News API and YouTube Data API v3. You can obtain these keys from the respective websites:

•News API
•YouTube Data API v3

## Set Up API Keys: 
Replace the placeholder API keys in the script.js file with your own API keys: (javascript)
``` 
const apiKey = 'YOUR_NEWS_API_KEY';
const youtubeApiKey = 'YOUR_YOUTUBE_API_KEY'
``` 
## Set Up Webscokets: 
Adding WebSockets to your project can enhance real-time communication and interactivity. 
``` 
const WebSocket = require('ws');
const http = require('http');

const server = http.createServer();
const wss = new WebSocket.Server({ server });

socket.addEventListener('open', function (event) {
    console.log('Connected to WebSocket server');
    socket.send('Hello Server!');
});

socket.addEventListener('message', function (event) {
    console.log('Message from server ', event.data);
    // Handle incoming messages and update the UI accordingly
});

socket.addEventListener('close', function (event) {
    console.log('Disconnected from WebSocket server');
});

socket.addEventListener('error', function (event) {
    console.error('WebSocket error:', event);
});

``` 
## Usage Examples:
Send Message to server
``` 
function sendMessage(message) {
    if (socket.readyState === WebSocket.OPEN) {
        socket.send(message);
    } else {
        console.error('WebSocket is not open. ReadyState: ' + socket.readyState);
    }
}
``` 

## Open index.html: 
Open the index.html file in a web browser to launch the application.

## Explore and Enjoy: 
Start exploring the different categories, search for news articles, and stay informed about the latest happenings around the world!
