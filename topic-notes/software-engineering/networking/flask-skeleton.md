Flask Docs: https://flask.palletsprojects.com/en/stable/

```

from flask import Flask, request, jsonify

# Initialize the Flask app
app = Flask(__name__)

# 2. Simple Endpoint (GET request)
@app.route('/')
def home():
    # Delivering simple HTML content upon a GET request
    return "Welcome to the Flask app!"

# 3. Simple endpoint that returns JSON
@app.route('/api/data', methods=['GET'])
def get_data():
    # Returning a simple JSON response
    data = {
        "message": "This is a simple JSON response.",
        "status": "success"
    }
    return jsonify(data)  # Returning a JSON response

# 4. Parsing a GET request
@app.route('/api/parse', methods=['GET'])
def parse_get_request():
    # Retrieving query parameters from the GET request
    name = request.args.get('name', 'Guest')  # Default value is 'Guest'
    age = request.args.get('age', 'unknown')  # Default value is 'unknown'
    return f"Hello, {name}. You are {age} years old."

# 5. Path Parameters to change response
@app.route('/api/greet/<name>', methods=['GET'])
def greet_user(name):
    # Using a path parameter in the URL
    return f"Hello, {name}! Welcome to the Flask app."

# 6. List of HTTP methods and when to use them:
@app.route('/api/post', methods=['POST'])
def post_data():
    # Handling a POST request (used for creating or submitting data)
    data = request.json  # Retrieving JSON data from the request body
    return jsonify({"message": "Data received", "data": data}), 201

@app.route('/api/put/<item_id>', methods=['PUT'])
def put_data(item_id):
    # Handling a PUT request (used for updating existing data)
    data = request.json  # Retrieving updated data from the request body
    return jsonify({"message": f"Item {item_id} updated", "data": data})

@app.route('/api/delete/<item_id>', methods=['DELETE'])
def delete_item(item_id):
    # Handling a DELETE request (used for deleting data)
    return jsonify({"message": f"Item {item_id} deleted"})

# 7. Error handling for graceful error responses
@app.errorhandler(404)
def page_not_found(e):
    # Custom error message for 404 (Page not found)
    return jsonify({"error": "Page not found"}), 404

@app.errorhandler(500)
def internal_error(e):
    # Custom error message for 500 (Internal server error)
    return jsonify({"error": "Internal server error"}), 500

----------- Other stuff I found -----------

def load_companies() -> list[dict]:
    with open("./companies.json") as file:
        data = json.load(file)
        return data


# Query Param
@app.route("/companies")
def companies() -> list:
    companies = load_companies()

    search = request.args.get("search")

    if search:
        found_companies = []
        for company in companies:
            if search in company["name"].lower():
                found_companies.append(company)

        if not found_companies:
            return {
                "error": f"No companies with search term '{search}' were found"
            }, 404

        return found_companies, 200

    return companies, 200


# Path Parameter
@app.route("/companies/<int:id>")
def companies_by_id(id: int) -> dict:
    companies = load_companies()
    
    for company in companies:
        if company["id"] == id:
            return company, 200

    return {
        "error": "Company not found"
    }, 404
		

--------------------------------------------

# 8. Properties of a RESTful API (this is a description in the code)
# A RESTful API has the following properties:
# - Stateless: Every request from the client to the server must contain all the information necessary to understand and complete the request.
# - Uniform interface: Resources are identified by URLs and interactions use standard HTTP methods (GET, POST, PUT, DELETE).
# - Cacheable: Responses are explicitly marked as cacheable or non-cacheable.
# - Client-Server architecture: The client and server are separate entities that interact over a network.

# 9. API testing using Postman or other tools
# You can test the following endpoints in Postman:
# - GET request: http://127.0.0.1:5000/api/data
# - POST request: http://127.0.0.1:5000/api/post with a JSON body
# - PUT request: http://127.0.0.1:5000/api/put/1 with a JSON body
# - DELETE request: http://127.0.0.1:5000/api/delete/1

# 10. Backend vs Client (explanation in the code)
# - The Backend (server-side) handles processing requests, managing data, and business logic.
# - The Client (front-end) is responsible for making requests to the backend and displaying the data.

# To run the Flask server
if __name__ == '__main__':
    app.run(debug=True)  # This runs the Flask app on http://127.0.0.1:500

```



**Breakdown of Features and Explanations:**

Simple Endpoint: The / route simply returns a text response ("Welcome to the Flask app!").

Returning JSON: The /api/data route sends a JSON response. This showcases how to use the jsonify function to return JSON data in Flask.

Parsing GET request: The /api/parse route demonstrates how to retrieve query parameters using request.args.get(). It provides default values if no parameters are provided.

Path Parameters: The /api/greet/<name> route illustrates how to use path parameters to alter the response dynamically based on the URL input.

HTTP Methods: The /api/post, /api/put/<item_id>, and /api/delete/<item_id> endpoints showcase how to handle POST, PUT, and DELETE HTTP methods. POST is used to submit data, PUT to update existing data, and DELETE to remove resources.

Error Handling: The app uses Flask’s error handler for 404 (Page Not Found) and 500 (Internal Server Error), sending back a JSON response with an appropriate error message.

RESTful API Properties: Describes key properties of a RESTful API, including statelessness, uniform interface, cacheability, and client-server architecture.

Backend vs Client: Provides a comment explaining the difference between backend (server-side) and client (front-end), emphasizing that the backend handles data and logic while the client interacts with the user.

Testing with Postman: The app’s API endpoints can be tested with tools like Postman by sending various HTTP requests (GET, POST, PUT, DELETE) to the provided routes.

