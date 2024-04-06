## Real Time Communication 
![image](https://github.com/thiagohrcosta/real-time-communication/assets/28869405/cf5c70a6-5935-4b37-b95d-7dd2998cd18c)

## Overview

The Real Time Communication project is a part of the Python Developer formation at Rocketseat. The primary goal is to create and practice Websockets in payment methods, enabling real-time updates on pages as soon as the payment gateway confirms transactions.

## Features

-   **QR Code Payment Creation**: The system allows users to create payments that generate a QR Code, facilitating seamless transactions.
    
-   **Real-time Communication with Websockets**: The system keeps track of user actions using Websockets. Once a payment is completed, real-time communication updates the payment status in the database to "paid." Users are then automatically redirected to the confirmation payment page, ensuring a smooth and efficient payment experience.


## API endpoint

### Insomnia

For this first version, Insomnia was used to make the requests, but you can use any other API client that you prefer.

### User

1.  **Create Payment**
    -   Endpoint: `POST http://127.0.0.1:5000/payments/pix`
    -   Request Body:     `{"value": 1100.98}`
    -   ![image](https://github.com/thiagohrcosta/real-time-communication/assets/28869405/07e7453e-bce1-48b7-aa99-e95661617e16)

### Payment

2.  **Payment confirmation**
    -   Endpoint: `POST http://127.0.0.1:5000/payments/pix/confirmation`
    - Requested body `{"bank_payment_id": "3cf60249-feb8-4b84-96b9-dd4a713f693c", "value": 1100.98}`
    - ![image](https://github.com/thiagohrcosta/real-time-communication/assets/28869405/cfcb4ec0-057e-4459-aed2-9a7fb973c680)

## How to Run

To run this application, ensure you Python installed on your machine. Follow these steps:

1.  **Navigate to Project Folder:**
    
    -   Open your terminal/command prompt and navigate to the project folder.
2.  **Install Dependencies:**
    
    -   Before starting the application, install the required dependencies by running the following command:
                
        `pip install -r requirements.txt` 
        
3.  **Configure Python Environment:**
    
    -   After installing the dependencies, open a Python shell by running the following command:`flask shell` 
        
    -   Once in the Python shell, run the following commands to configure the database: `
        db.drop_all()
        db.create_all()
        db.session.commit()` 

4.  **Start the Application:**
    
    -   After configuring the Python environment, run the following command to start the application:  `python app.py` 
                
5.  **Access the endpoint:**
    
    -   Once both the application and the database are running, you can access the project at `http://localhost:5000` in your web browser.

6. **Frontend Application:**
	-   Once both the application is running the `/payment` and `/confirmation_payment` can be acces at browser.









