# EX01 Developing a Simple Webserver

# Date:3.12.2024
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            background-color: black;
        }
        table {
            width: 70%; 
            border-collapse: collapse;
            margin: 0 auto; 
        }
        table, th, td {
            border: 1px solid white;
        }
         td {
            padding: 8px; 
            text-align: left;
            font-size: 20px;
            color: beige;
        }
        th {
            background-color: #a59d9d;
            color: black;
            padding: 8px;
            text-align: left;
            font-size: 20px;
            text-align: center;
        }
        h2 {
            text-align: center;
            font-size: 24px; 
            color: azure;
        }
    </style>
</head>
<body>

    <h2>LAPTOP CONFIGURATION DETAILS</h2>

    <table>
        <thead>
            <tr>
                <th>INFORMATION</th>
                <th>DETAILS</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Operating System</td>
                <td>Windows</td>
            </tr>
            <tr>
                <td>Architecture</td>
                <td>AMD64</td>
            </tr>
            <tr>
                <td>Processor</td>
                <td>Intel64 Family 6 Model 142 Stepping 10</td>
            </tr>
            <tr>
                <td>CPU Cores</td>
                <td>4</td>
            </tr>
            <tr>
                <td>Logical CPUs</td>
                <td>8</td>
            </tr>
            <tr>
                <td>Total Memory (GB)</td>
                <td>7</td>
            </tr>
            <tr>
                <td>Used Memory (GB)</td>
                <td>6</td>
            </tr>
            <tr>
                <td>Free Memory (GB)</td>
                <td>1</td>
            </tr>
            <tr>
                <td>Disk Usage(%)</td>
                <td>36.0</td>
            </tr>
        </tbody>
    </table>

</body>
</html>
```
```
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

# OUTPUT:
![WhatsApp Image 2024-12-07 at 14 19 44_c27a1a6f](https://github.com/user-attachments/assets/88471acb-de2e-496d-b437-9fbb4b47ae4c)
![WhatsApp Image 2024-12-16 at 20 46 31_37a29b68](https://github.com/user-attachments/assets/db17b847-5aa2-4c45-98f9-4582fcec7cec)



# RESULT:
The program for implementing simple webserver is executed successfully.
