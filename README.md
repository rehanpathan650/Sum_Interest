## **Backend Logic for Sum and Simple Interest Calculation**

### **Project Description**
This is a simple backend application built using **Node.js** and **Express.js**. The application provides two endpoints:  
1. **Sum of Two Numbers**  
2. **Simple Interest Calculation**  

It takes input values via API requests and returns the results in JSON format.

---

### **Features**
1. Calculate the **sum** of two numbers.
2. Calculate the **simple interest** based on the principal amount, rate of interest, and time.

---

### **Technologies Used**
- **Node.js**  
- **Express.js**

---

### **Setup Instructions**

Follow these steps to set up and run the project locally:

1. **Clone the repository**  
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install dependencies**  
   Make sure you have Node.js installed, then run:
   ```bash
   npm install
   ```

3. **Start the server**  
   Run the following command to start the server:
   ```bash
   node index.js
   ```
   The server will start on `http://localhost:4000` (default port).

---

### **API Endpoints**

#### 1. **Calculate Sum**  
- **Endpoint**: `/sum`  
- **Method**: `POST`  
- **Request Body** (JSON format):
   ```json
   {
     "num1": 5,
     "num2": 10
   }
   ```
- **Response**:
   ```json
   {
     "result": 15
   }
   ```

---

#### 2. **Calculate Simple Interest**  
- **Endpoint**: `/simple-interest`  
- **Method**: `POST`  
- **Request Body** (JSON format):
   ```json
   {
     "principal": 1000,
     "rate": 5,
     "time": 2
   }
   ```
- **Response**:
   ```json
   {
     "result": 100
   }
   ```

   **Explanation**:  
   Simple Interest Formula:  
   \[
   \text{Simple Interest} = \frac{\text{Principal} \times \text{Rate} \times \text{Time}}{100}
   \]

---

### **Folder Structure**
```
project-folder/
│
├── index.js           # Main application file
├── package.json       # Project configuration and dependencies
└── README.md          # Project documentation
```

---

### **Sample Code for `index.js`**
If needed, here’s an example of your Express code:

```javascript
const express = require('express');
const app = express();
const port = 3000;

app.use(express.json());

// Route for sum of two numbers
app.post('/sum', (req, res) => {
  const { num1, num2 } = req.body;
  const result = num1 + num2;
  res.json({ result });
});

// Route for simple interest calculation
app.post('/simple-interest', (req, res) => {
  const { principal, rate, time } = req.body;
  const result = (principal * rate * time) / 100;
  res.json({ result });
});

app.listen(port, () => {
  console.log(`Server is running on http://localhost:${port}`);
});
```

---

### **Testing the APIs**
You can use **Postman** or any API testing tool to test the endpoints:
1. **POST `/sum`**: Send `num1` and `num2` in the request body.
2. **POST `/simple-interest`**: Send `principal`, `rate`, and `time` in the request body.

---

### **Contributing**
Feel free to fork this repository, create a new branch, and make contributions. Pull requests are welcome!

---

### **License**
This project is licensed under the **MIT License**.

---

### **Author**
- **Rehan Parhan**  
- GitHub: [Your GitHub Profile](https://github.com/rehanpathan650)

---
