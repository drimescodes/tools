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

#### Note: Be sure to take appropriate precautions and use ngrok responsibly, as sharing your laptop's content with others over the internet may pose security risks. But if you're only exposing your index.html you should be fine


#### Special Case

In my case after inputing ```ngrok http 8000```, it brought forth this error
```
bash: ngrok: command not found
```
I added ngrok to my environment variables path using the graphic interface but still didn't work so I had to do it this way before it finally worked

So
If you're seeing the error message ```"bash: ngrok: command not found"```, it means that the ngrok executable is not in your system's PATH. Here's how you can add it to your PATH:

First, make sure that you've downloaded and extracted the ngrok executable to a directory on your computer. For example, you might have extracted it to the ~/Downloads directory.

Open your .bashrc file in a text editor by typing the following command in your terminal:

```
nano ~/.bashrc

This will open the .bashrc file in the Nano text editor.
```

Add the following line to the end of the .bashrc file:
ruby
```
export PATH=$PATH:/path/to/ngrok/directory
```
Replace /path/to/ngrok/directory with the path to the directory where you extracted the ngrok executable. For example, if you extracted it to the``` ~/Downloads``` directory, you would use the following line:

```
export PATH=$PATH:~/Downloads
```
Save the .bashrc file by pressing Ctrl+O and then Ctrl+X to exit Nano.

Reload your .bashrc file by typing the following command in your terminal:

```
source ~/.bashrc
```
Try running the ngrok command again to make sure it's working using this
```ngrok http 8000```
This should start ngrok and expose your local web server to the internet.

I hope this helps you resolve the issue with ngrok not being found in your PATH. Let me know if you have any other questions or concerns!

One thing to note is that if you're using a different shell (e.g., zsh instead of bash), you may need to modify a different configuration file ```(e.g., ~/.zshrc instead of ~/.bashrc)```. So make sure to use the appropriate configuration file for your shell.

Also, if you want to add the ngrok executable to your PATH permanently (so that you don't have to add it every time you open a new terminal window), you can add the export line to your ```~/.bash_profile (or ~/.zprofile for zsh)``` file instead.

Written by drimes after careful research on the internet and chatGPT


My Twitter handle
##### [©drimescodes](https://twitter.com/drimesbot)
