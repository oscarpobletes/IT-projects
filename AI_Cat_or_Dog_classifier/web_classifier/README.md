# Web and mobile image classification

These files represent the website, once the AI ​​model is created and trained with Python and Tensorflow, which is exported to "js" and "bin" files.

This can be used on mobile, just point the camera at what you want to classify (it can be a computer image or a real one)

## How to use

### Start a server in the classifier folder.

Note: This project uses a Tensorflow.js model, which requires access via http/https to load.
You can use any server for that, but here's a way to do it:

- Download Python on your computer
- Open a command line or terminal
- Navigate to the folder where you downloaded the repository
- Run the command `python -m http.server 8000`
- Open a browser and go to http://localhost:8000

### Use it on a cell phone
If you want to open it on your cell phone, you can't just put the local IP of your computer and the port, since HTTPS is required to use the camera. You can make an HTTPS tunnel by following the steps below:
- Download ngrok on your computer, and unzip it
- Open a command line or terminal
- Navigate to the folder where you downloaded ngrok
- Run the command `ngrok http 8000`
- It is important to have both active: The python server, and the ngrok tunnel
- An HTTPS link will appear on the command line. You can enter there with your cell phone, it does not matter if you are not in the local network.
- The tunnel expires after 2 hours, in which case you just restart ngrok
- Open a browser on your cell phone and go to the indicated HTTPS link

### Use
You can click the "Change camera" button to use the front or rear camera of the cell phone. The prediction will appear below.

### Credits 
Code was inspired on: https://github.com/ringa-tech/clasificador-perros-gatos