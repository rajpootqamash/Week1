SCREENSHOTS OF THIS TASK:
## 1. Install Node.js and npm
sudo apt update
sudo apt install nodejs npm -y

## 2. Clone the Mock Web Application (e.g., Juice Shop)
git clone https://github.com/juice-shop/juice-shop.git
cd juice-shop

## 3. Install Dependencies
npm install

## 4. Start the Application
npm start

# Access the app in browser:
http://localhost:3000


# ---------------------------
# OWASP ZAP Usage
# ---------------------------

# Start ZAP (or launch it manually)
zap.sh

# Steps in ZAP:
# 1. Start a new session.
# 2. Configure browser to use ZAP as a proxy:
#    HTTP Proxy: 127.0.0.1
#    Port: 8080
# 3. Open the app (http://localhost:3000) in browser.
# 4. Right-click target in ZAP > Attack > Active Scan

# ---------------------------
# Manual Testing Inputs
# ---------------------------

## Reflected XSS Payload:
<script>alert('XSS');</script>

## SQL Injection Payload for Login Form:
Username: admin' OR '1'='1
Password: anything

![1](https://github.com/user-attachments/assets/9b46481f-7862-4a26-83b5-84277fde3f5a)

![2](https://github.com/user-attachments/assets/ef705c6f-b060-4390-b17b-35957c2f251f)
![3](https://github.com/user-attachments/assets/710af281-51dc-44d5-9e5c-9ce001394561)
![4](https://github.com/user-attachments/assets/0cc56ad9-47cc-4e70-85d2-f85db24ebfd6)
![5](https://github.com/user-attachments/assets/a823c46b-b976-4294-a2b4-498a23bbf70d)
![6](https://github.com/user-attachments/assets/630b604c-bc85-4e10-8bf1-217a33cd525d)
![7](https://github.com/user-attachments/assets/5ab91452-0e3b-42f7-a47a-2680f1da7d4f)
![8](https://github.com/user-attachments/assets/51367735-c41e-4567-9976-dac2744acc9f)
![9](https://github.com/user-attachments/assets/fd201e79-c327-4db4-8778-64e6ad225294)
![10](https://github.com/user-attachments/assets/d2ab3cf2-3caf-40f2-90d7-d4e28e9dfd07)
![11](https://github.com/user-attachments/assets/2135fc38-a08f-47a7-86b7-bfe0c99505cb)
![12](https://github.com/user-attachments/assets/831edb75-fb63-43d9-947f-298af4308679)
![13](https://github.com/user-attachments/assets/7fdc997a-fb3c-46cb-bb4a-af6acfb6b64e)
![14](https://github.com/user-attachments/assets/e1665717-e065-4adb-b95c-46f9eaedc06d)
![15](https://github.com/user-attachments/assets/31f2fd60-3bd4-407f-b430-532feec989b2)
![16](https://github.com/user-attachments/assets/f3b20fe7-b45d-4461-86c7-722c5be9cabe)
![17](https://github.com/user-attachments/assets/7be2bd93-5ce9-4270-9d40-9511849e8474)
