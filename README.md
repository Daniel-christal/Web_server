# Developing a Simple Webserver
Name: DANIEL.C
ID: 23008937 
emailid: danielsubitha05@gmail.com

# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
```from http.server import HTTPServer , BaseHTTPRequestHandler

content="""
<html>
<head>
</head>
<body>
<h1>welcome</h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request recieved")
        self.send_response(200)
        self.send_header('Content-type','text/html;charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver")
server_address = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.serve.forever()
```
# OUTPUT:
![WhatsApp Image 2023-10-18 at 22 26 55_d802a364](https://github.com/Daniel-christal/Web_server/assets/145742847/ae9ce258-b903-4116-a20d-5003b47650e1)

# RESULT:

The program is executed succesfully
