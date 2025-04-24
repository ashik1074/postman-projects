Here's a professional and clean `README.md` for your GitHub project, following the standard GitHub README format:

---

# 🌦️ Sensor & Measurement REST API

This project provides a RESTful API for managing sensors and their measurements. Built with **Spring Boot**, it allows users to register sensors, log environmental measurements, retrieve data, and count the number of rainy days. The project also features API documentation via **OpenAPI (Swagger)** for easy exploration and testing.

## 🔗 API Documentation

Explore the API via Swagger UI:  
**[OpenAPI Swagger Documentation](https://)**

---

## 🚀 Features

- Register new sensors
- Submit new measurements (e.g., temperature, rain status)
- Retrieve all measurements
- Count total rainy days

---

## 📦 Endpoints

### Sensor

#### ✅ Register Sensor (Successful)
- **Method:** `POST`
- **URL:** `/api/v1/sensors`
- **Request Body:**
```json
{
  "name": "TestName"
}
```

#### ❌ Register Sensor (Unsuccessful)
- **Method:** `POST`
- **URL:** `/api/v1/sensors`
- **Request Body:**
```json
{
  "name": "TestName"
}
```
> ⚠️ This fails when the sensor with the same name already exists.

---

### Measurement

#### 📥 Add Measurement
- **Method:** `POST`
- **URL:** `/api/v1/measurements`
- **Request Body:**
```json
{
  "value": 24.5,
  "raining": true,
  "sensor": {
    "name": "TestName"
  }
}
```

#### 📊 Get All Measurements
- **Method:** `GET`
- **URL:** `/api/v1/measurements`

#### 🌧️ Get Rainy Days Count
- **Method:** `GET`
- **URL:** `/api/v1/measurements/rainy-days-count`

---

## 🛠️ Tech Stack

- Java
- Spring Boot
- OpenAPI / Swagger
- REST API

---

## 🧪 Testing

You can use Postman or Swagger UI to test all endpoints. Make sure the backend server is running before sending requests.

---

## 📂 Project Structure

```
src
├── main
│   ├── java
│   └── resources
└── test
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

Let me know if you'd like to add sections like "How to Run", "Contributing", or a sample `.env` setup!
