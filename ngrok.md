# How to Use Ngrok to Expose a Local Web Server to the Internet

### Introduction
'ngrok' is a tool that allows you to expose your local web server to the internet and share it with others, even if your laptop is behind a firewall or NAT.

In this guide, we'll show you how to use ngrok to expose your local web server and share it with others.

#### Prerequisites
A local web server running on your computer. You can start a Python web server by running the following command in your terminal:
```
cd /path/to/your/website
python -m http.server 8000

Note: Replace /path/to/your/website with the path to the directory containing your website files.
```
##### ngrok must be installed on your computer. You can download it from the official website: https://ngrok.com/download



#### Steps
Download ngrok from the official website and extract it to a directory on your computer.

Start your local web server by running the following command in your terminal:

```
cd /path/to/your/website
python -m http.server 8000
The above will start the server on port 8000.
```
In a new terminal window, navigate to the directory where you extracted ngrok and run the following command:

```./ngrok http 8000```

This will start ngrok and provide you with a public URL that you can use to access your local web server from the internet.

Look for the Forwarding section in the ngrok output. You should see a line that looks something like this:
```
Forwarding         http://abcd1234.ngrok.io -> http://localhost:8000
```
The http://abcd1234.ngrok.io URL is the public URL that you can use to access your local web server from the internet.

Copy the http://abcd1234.ngrok.io URL and paste it into your web browser's address bar. You should see your local web server's content displayed in your browser.
That's it! You can now share the ngrok URL with others to allow them to access your local web server from the internet.

#### Note: Be sure to take appropriate precautions and use ngrok responsibly, as sharing your laptop's content with others over the internet may pose security risks.

Written by drimes after careful research on the internet and chatGPT


My Twitter handle
##### [©drimescodes](https://twitter.com/drimesbot)
