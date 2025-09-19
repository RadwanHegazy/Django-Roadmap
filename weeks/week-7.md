# Week 7: Networks

This week explores computer networking fundamentals, which are essential for understanding how web applications work. You'll learn about network protocols, the OSI model, HTTP, and how to build basic network applications. This knowledge will help you understand Django's request/response cycle and web communication.

## Topics Covered

1. **Network Basics**
   - What is a network?
   - Types of networks (LAN, WAN, Internet)
   - IP addresses and domain names
   - Ports and sockets

2. **OSI Model**
   - 7 layers of the OSI model
   - Responsibilities of each layer
   - How data flows through the layers
   - TCP/IP model comparison

3. **HTTP Protocol**
   - HTTP vs HTTPS
   - Request methods (GET, POST, PUT, DELETE)
   - Status codes
   - Headers and cookies
   - RESTful principles

4. **Web Servers**
   - How web servers work
   - Building a simple web server in Python
   - Static vs dynamic content
   - Server-side vs client-side processing

5. **DNS and Domain Names**
   - How DNS works
   - Domain name resolution
   - DNS records (A, CNAME, MX)

6. **Network Security Basics**
   - HTTPS and SSL/TLS
   - Firewalls and security layers
   - Common security threats

## Resources

- [Network Basics](https://www.youtube.com/watch?v=q6tUCEUqxTQ&list=PL8s4OGp0649_e_Wbz5MlBgW5rBW-9hD0c)
- [OSI Model](https://www.youtube.com/watch?v=A31bxOyj5mk)
- [HTTP Protocol](https://www.youtube.com/watch?v=pi4gaFDBtMc)
- [Build Web Server in Python](https://www.youtube.com/watch?v=Hncp0mPfUvk&t=1s)

## Tasks

### Task 1: OSI Model Study
Create a visual representation or summary of the OSI model.

**Requirements:**
- List all 7 layers with their responsibilities
- Explain how data encapsulation works
- Create a diagram or chart showing data flow
- Give real-world examples for each layer

### Task 2: Simple HTTP Client
Build a basic HTTP client in Python to make requests.

**Requirements:**
- Use Python's `urllib` or `requests` library
- Make GET and POST requests to httpbin.org
- Handle response status codes
- Parse JSON responses
- Add custom headers

**Example Code:**
```python
import requests

# GET request
response = requests.get('https://httpbin.org/get')
print(f"Status Code: {response.status_code}")
print(f"Response: {response.json()}")

# POST request
data = {'key': 'value'}
response = requests.post('https://httpbin.org/post', json=data)
print(response.json())
```

### Task 3: Build a Simple Web Server
Create a basic web server using Python's built-in modules.

**Requirements:**
- Use `http.server` module
- Serve static HTML files
- Handle different HTTP methods
- Add basic routing
- Serve JSON data

**Example Server:**
```python
from http.server import BaseHTTPRequestHandler, HTTPServer
import json

class SimpleHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        if self.path == '/':
            self.send_response(200)
            self.send_header('Content-type', 'text/html')
            self.end_headers()
            self.wfile.write(b'<h1>Hello, World!</h1>')
        elif self.path == '/api':
            self.send_response(200)
            self.send_header('Content-type', 'application/json')
            self.end_headers()
            data = {'message': 'Hello from API'}
            self.wfile.write(json.dumps(data).encode())
        else:
            self.send_response(404)
            self.end_headers()
            self.wfile.write(b'Not Found')

def run():
    server_address = ('', 8000)
    httpd = HTTPServer(server_address, SimpleHandler)
    print('Server running on port 8000...')
    httpd.serve_forever()

if __name__ == '__main__':
    run()
```

### Task 4: Network Analysis
Analyze network traffic for a web application.

**Requirements:**
- Use browser developer tools to inspect HTTP requests
- Analyze headers, cookies, and request/response data
- Test different HTTP methods
- Understand CORS (Cross-Origin Resource Sharing)

### Task 5: DNS Investigation
Explore DNS and domain name resolution.

**Requirements:**
- Use command-line tools like `nslookup` or `dig`
- Check DNS records for different domains
- Understand DNS caching
- Explore DNS propagation

**Commands to try:**
```bash
nslookup google.com
dig google.com
ping google.com
```

## Tips for Success

- Networking can be abstract, so focus on practical examples
- Use tools like Wireshark (optional) to visualize network traffic
- Practice with real websites using browser dev tools
- Understand that HTTP is just one protocol among many
- Relate networking concepts back to web development

## Next Steps

Networking knowledge will help you understand web application architecture. In the Intermediate section (starting next week), we'll dive into Django REST Framework and APIs. Meanwhile, experiment with your simple web server and think about how Django abstracts away many of these low-level details.

Keep exploring the connected world! 🌐
