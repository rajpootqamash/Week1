Screenshots
1. Setup Project Directory
--------------------------
mkdir user-management-secure
cd user-management-secure

Explanation:
- mkdir: Creates a new folder for your project.
- cd: Enters the project folder.

2. Initialize Node.js Project
-----------------------------
npm init -y

Explanation:
- Initializes a new Node.js project and creates a package.json file.

3. Install Required Dependencies
-------------------------------
npm install express mongoose bcrypt jsonwebtoken validator helmet

Explanation:
- express: Web framework to build APIs.
- mongoose: MongoDB connection and management.
- bcrypt: Secure password hashing.
- jsonwebtoken: Token-based authentication.
- validator: Validate and sanitize input (e.g., email).
- helmet: Adds security HTTP headers.

4. Create Necessary Files
-------------------------
touch app.js routes/user.js models/User.js

Explanation:
- Creates main server file and folders for user routes and models.

5. Setup MongoDB
----------------
sudo systemctl start mongod
sudo systemctl enable mongod

Explanation:
- Starts and enables MongoDB to run in the background.

6. Start Your Backend Server
----------------------------
node app.js

Expected Output:
Server running at http://localhost:3000

7. Test API with curl
---------------------
curl -X POST http://localhost:3000/api/register \\
  -H "Content-Type: application/json" \\
  -d '{"email": "test@example.com", "password": "Secret123"}'

Explanation:
- Simulates a user registering to your backend securely.

8. View Data in MongoDB
-----------------------
mongo

> use userdb

> db.users.find().pretty()

Explanation:
- use userdb: Connects to the MongoDB database.
- db.users.find().pretty(): Displays all users in a readable format.

![1](https://github.com/user-attachments/assets/ed1e254c-8fa6-4ca3-8512-68ff4b074e3b)
![2](https://github.com/user-attachments/assets/47075306-5d13-47bd-badd-9b189da713e7)
![3](https://github.com/user-attachments/assets/51246adc-4f39-4d26-9c0c-b6187585fd49)
![4](https://github.com/user-attachments/assets/fa8e37ab-5795-44ce-909a-2f5ca3c1c5d0)
![5](https://github.com/user-attachments/assets/7d9f2548-1a7a-4d00-a5a9-2faf4e0bb443)
![6](https://github.com/user-attachments/assets/ec02a893-6829-46ea-8254-79b08366d84c)
![7](https://github.com/user-attachments/assets/4266ab23-02ed-4aee-9267-6b687da05086)
![8](https://github.com/user-attachments/assets/e87892f5-f86d-4387-999b-c471c70e2d9b)
![10](https://github.com/user-attachments/assets/bace84b6-36b4-4b64-91ca-07dd84aceba9)
![11](https://github.com/user-attachments/assets/9b9f1b0b-55fe-46d1-9619-b29e12148beb)
![12](https://github.com/user-attachments/assets/9db70364-348c-4dff-98fc-369b96a1c0c7)
![21](https://github.com/user-attachments/assets/4df1e030-355b-4732-b2c2-622a326776c6)
![22](https://github.com/user-attachments/assets/487ef861-48ed-4112-a83f-e8638b1c6af8)
![23](https://github.com/user-attachments/assets/e6409aa3-6b08-44fd-b3b8-7ddefab00de2)
