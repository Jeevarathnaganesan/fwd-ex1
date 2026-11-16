# EX01 Developing a Simple Webserver
## Date:16-11-2026
## Reg no:26018066
~~~
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """

<!DOCTYPE html>
<html>
<head>
    <title>TCP/IP Protocol Suite</title>
</head>

<body>

    <h1 align="center">TCP/IP PROTOCOL SUITE</h1>
    <hr>

    <h2>Introduction</h2>
    <p>
        TCP/IP is a set of communication protocols
        used to connect devices and transfer data
        over the Internet.
    </p>

    <h2>Four Layers of TCP/IP</h2>

    <h3>1. Application Layer</h3>
    <p>Provides network services to users and applications.</p>
    <ul>
        <li>HTTP</li>
        <li>HTTPS</li>
        <li>FTP</li>
        <li>SMTP</li>
        <li>DNS</li>
        <li>SSH</li>
    </ul>

    <h3>2. Transport Layer</h3>
    <p>Responsible for data transmission between devices.</p>
    <ul>
        <li>TCP</li>
        <li>UDP</li>
    </ul>

    <h3>3. Internet Layer</h3>
    <p>Responsible for addressing and routing data packets.</p>
    <ul>
        <li>IP</li>
        <li>IPv4</li>
        <li>IPv6</li>
        <li>ICMP</li>
    </ul>

    <h3>4. Network Access Layer</h3>
    <p>Transfers data through the network.</p>
    <ul>
        <li>Ethernet</li>
        <li>Wi-Fi</li>
        <li>ARP</li>
    </ul>

    <hr>

    <h2 align="center">Protocol Summary</h2>

    <table border="1" align="center" cellpadding="10">
        <tr>
            <th>Layer</th>
            <th>Protocols</th>
        </tr>

        <tr>
            <td>Application Layer</td>
            <td>HTTP, HTTPS, FTP, SMTP, DNS, SSH</td>
        </tr>

        <tr>
            <td>Transport Layer</td>
            <td>TCP, UDP</td>
        </tr>

        <tr>
            <td>Internet Layer</td>
            <td>IP, IPv4, IPv6, ICMP</td>
        </tr>

        <tr>
            <td>Network Access Layer</td>
            <td>Ethernet, Wi-Fi, ARP</td>
        </tr>
    </table>

    <br>
    <hr>

    <h3 align="center">Thank You</h3>

</body>
</html>




"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',880)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
~~~

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
![alt text](<Screenshot 2026-11-14 161119.png>)
## OUTPUT:
![alt text](<Screenshot 2026-11-14 161238.png>)
## RESULT:
The program for implementing simple webserver is executed successfully.

