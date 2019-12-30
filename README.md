# web-server-with-flask ✊
Build a python web server with flask

##Introduction

We’ll set up a web server and create a simple website using Flask, Python, and HTML/CSS.  

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/ab998c3t8xd4kf2ed91g.png)

The web server will be able to react to the user inputting dynamic content, turning your website into a web application capable of doing more than just showing static information.

##Build a Flask website

We need to make sure we have python3 installed. https://www.python.org/downloads/

We also need to install Flask with pip. 
```pip3 install flask```

Open a terminal or command prompt window, and make a new directory called `webapp` for your project.
```mkdir webapp```

Use the change directory command `cd` to open the new directory.
```cd webapp```

Open up Python3 IDLE.

Create a new file by clicking File and then New file, and save it as `app.py` inside the `webapp` folder you just created.

Now enter the following lines of code into the blank `app.py` window:
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/smjls8rn3qpm6yqnxscw.png)

Save your changes in IDLE (or your preferred text editor). Now we need to run your web app from the terminal/command prompt we opened up earlier. 

###On Raspberry Pi/Linux/macOS

Enter the command python3 app.py into the terminal window.

###On Windows

Enter the command python app.py into the command prompt window.

If everything is correct, we should see something similar to this! 
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/sxoit98ea78riyjo5gxg.png)

If you see this, go ahead and open up your web browser. Enter the URL `http://127.0.0.1:5000/`. You should see a white screen and your "Hello World" text!
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/0kke6vkkh2jq9xxx7zo2.png)
Note: `127.0.0.1` refers to your local network aka this computer. `:5000` means port 5000 which is the port your web server is running on. 

Congrats, the web server is up and running!

##Add some HTML
Now we can add some HTML to your web app, rather than just using simple text in our `app.py`.

First, create a `templates` directory in your `webapp` directory by entering this into the terminal or command prompt window:
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/rgi1wan96e8po116vxkc.png)

Create a new file in IDLE by clicking File and New file. Save this as `index.html` in your `templates` folder.

Enter the following in your `index.html`
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/ztuuiitvwabg1f7m2k0r.png)

Save your changes by clicking File and Save, or by pressing Ctrl and s.

Return to your `app.py` file in IDLE, and modify the first line of your code to import the `render_template` function from the `flask` module as well:
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/u43vztagylrt0lkjy1gp.png)

Last step, we need to modify our `index()` function to return your `index.html` template. Change the code inside the definition so that your code looks like this!

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/9au56wqr9i4dukpfysbn.png)

Flask is now going to look for our `index.html` and show this on our local host server. (Test this by changing up the `h1` text and making it your own! 
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/lzljvrd56rtzuresj5fp.png)

##Add some CSS

Now since we've got our `index.html` showing on our web server, let's add some style to it with CSS. 

We first need to go back into our terminal/command prompt and navigate to the `webapp` directory. 

Create a new directory called `static`
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/wd7ffj1fgu5x93mt4tkn.png)

Create a new file in IDLE by clicking File and New File and save this file as `style.css`. Let's add the following CSS: (feel free to add your own colors) 
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/mwz1dzpnzsj7idcxep0a.png)

Make sure to save these changes. 

We now need to make sure we add our CSS link to our `index.html`. Go into your HTML file and let's add a `<head>` tag with a `<link>` tag with a reference to our CSS file. 
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/xplkmd3b07gabr6s7yj9.png)

Save your changes and then let's refresh our localhost server. You should now see your colorful changes! 
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/emx0le99m3oyxz89scjs.png)

Congrats! You now have a web server directly on your computer! Feel free to mess around with the HTML and CSS and make it your own!
