Basic Flask application:

```
from flask import Flask  
  
app = Flask(__name__)  
  
@app.route("/", methods=['GET'])  
def hello_world():  
return "Hello, World!"  
  
if __name__ == "__main__":  
app.run(debug=True, host="0.0.0.0", port=5000)
```

When we run this, a server starts and waits to receive requests at a certain address (URI). When we run locally, this is usually 127.0.0.1 and it runs on port 5000.

When we make a GET API call to this server: 127.0.0.1:5000/ Flask runs the function hello_world(). It knows that we are making a GET request, and so is expecting a response to return some data.

The [Flask Quick Start Guide](https://flask.palletsprojects.com/en/stable/quickstart/) gives an in-depth overview of what each line is doing in the code.