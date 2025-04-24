Sensor Management API
Overview
This project is a RESTful API for managing sensors and their measurements, built using Spring Boot. It provides endpoints to register sensors, add measurements, retrieve measurement data, and count rainy days. The API is documented using OpenAPI (Swagger) for easy exploration and testing.
Features

Register new sensors with a unique name.
Add measurements for a sensor, including temperature value and raining status.
Retrieve all measurements.
Count the number of rainy days based on measurement data.

API Endpoints
Sensor Registration

POST /api/v1/sensors
Description: Register a new sensor.
Request Body:{
  "name": "TestName"
}


Success Response: Sensor registered successfully.
Error Response: Returns an error if the sensor name is invalid or already exists.



Add Measurement

POST /api/v1/measurements
Description: Add a measurement for a registered sensor.
Request Body:{
  "value": 24.5,
  "raining": true,
  "sensor": {
    "name": "TestName"
  }
}


Success Response: Measurement added successfully.
Error Response: Returns an error if the sensor does not exist or the data is invalid.



Get All Measurements

GET /api/v1/measurements
Description: Retrieve all measurements.
Response: List of all measurements in the system.



Get Rainy Days Count

GET /api/v1/measurements/rainy-days-count
Description: Count the number of days with rainy measurements.
Response: Number of rainy days.



Getting Started
Prerequisites

Java 17 or later
Maven
Spring Boot
Swagger UI (included for API documentation)

Installation

Clone the repository:git clone <repository-url>


Navigate to the project directory:cd sensor-management-api


Build the project:mvn clean install


Run the application:mvn spring-boot:run



Accessing the API

The API will be available at http://localhost:8080.
Access the Swagger UI for interactive documentation at http://localhost:8080/swagger-ui.html.

Usage

Register a sensor using the POST /api/v1/sensors endpoint.
Add measurements for the sensor using the POST /api/v1/measurements endpoint.
Retrieve all measurements with GET /api/v1/measurements.
Check the count of rainy days with GET /api/v1/measurements/rainy-days-count.

Documentation
The API is documented using OpenAPI (Swagger). You can explore and test the endpoints directly from the Swagger UI.
Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.
License
This project is licensed under the MIT License.
