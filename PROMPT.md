You are a highly skilled software engineer with expertise in building robust and scalable web services. Your task is to create a dockerized NodeJS-based web service using Express JS and PostgreSQL for database.

**Web Service Requirements:**
1. Docker
2. Node JS
3. Express JS
4. Open Telemetry
5. Idempotency
6. Prometheus
7. PostgreSQL
8. Kafka
9. Jaeger tracing
**Functionality:**
    **






1.  **Container:** Docker
2.  **WebService** NodeJS
2.  **Endpoint:** `/payment/confirm`
3.  **Method:** POST
4.  **Functionality:**
    *   The `/greet` endpoint should accept an optional query parameter named `name`.
    *   If `name` is provided, the service should return a JSON response in the format: `{"message": "Hello, [name]!"}`.
    *   If `name` is not provided, the service should return a JSON response in the format: `{"message": "Hello, World!"}`.
5.  **Error Handling:** Implement basic error handling for invalid requests or missing parameters, returning appropriate HTTP status codes and JSON error messages.
6.  **Code Structure:** Organize the code into a single `app.py` file.
7.  **Dependencies:** Ensure all necessary dependencies are listed for a `requirements.txt` file.

**Steps to Complete:**

1.  **Flask Application Setup:** Create a basic Flask application instance.
2.  **Define the `/greet` Endpoint:** Implement the `/greet` endpoint with the specified functionality.
3.  **Parameter Handling:** Extract and validate the `name` query parameter.
4.  **JSON Response:** Construct and return JSON responses as per the requirements.
5.  **Error Handling Implementation:** Add error handling for cases like invalid requests.
6.  **Dependency List:** Generate a `requirements.txt` file listing Flask.

**Example Usage:**

*   `GET /greet` should return `{"message": "Hello, World!"}`
*   `GET /greet?name=Alice` should return `{"message": "Hello, Alice!"}`

Provide the complete `app.py` and `requirements.txt` files.








Please generate a Node.js web service using Express.js.

**Requirements:**

1.  **Endpoints:**
    *   `GET /api/items`: Returns a list of all items.
    *   `GET /api/items/:id`: Returns a single item by its ID.
    *   `POST /api/items`: Creates a new item. The request body will contain the item data.
    *   `PUT /api/items/:id`: Updates an existing item by its ID. The request body will contain the updated item data.
    *   `DELETE /api/items/:id`: Deletes an item by its ID.

2.  **Data Storage:** Use a simple in-memory array to store items. Each item should have at least an `id` (unique, generated automatically) and a `name` property.

3.  **Error Handling:** Implement basic error handling for cases like item not found.

4.  **Server Setup:** The server should listen on port 3000.

**Please provide:**

*   The complete `app.js` file with all the necessary code.
*   Instructions on how to run the application (e.g., `npm install express`, `node app.js`).