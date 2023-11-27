# Developing a Simple Webserver
![image](https://github.com/prathyusharavi/webserver/assets/147474424/614813c2-de64-42a0-8787-5807eb42eb3f)


# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```py
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
<h2>4.MERN Stack</h2>
<h2>5.ASP.Net</h2>
</body>
</html>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',80)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
## OUTPUT:

![image](https://github.com/prathyusharavi/webserver/assets/147474424/2168af34-4de2-4ada-92a6-9bd041710e0b)

### Server output
/home/sec/Pictures/Screenshots/serveroutput.png
### Client output
/home/sec/Downloads/clientoutput.png

## RESULT:
The program is executed succesfully
