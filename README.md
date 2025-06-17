# Cybersecurity Intern Project: Strengthening Security Measures for a Web Application

## Overview

This project is a learning and hands-on implementation task designed for cybersecurity interns. It focuses on identifying and mitigating security vulnerabilities in a web application. The project is divided into 3 weeks, covering security assessments, patching vulnerabilities, implementing best practices, and documenting the entire process.

## Technologies Used

- Node.js & Express.js
- MongoDB
- bcrypt (password hashing)
- jsonwebtoken (JWT-based authentication)
- validator (input validation)
- helmet (HTTP header security)
- winston (logging)
- OWASP ZAP (vulnerability scanning)
- Nmap (port scanning)
- Browser DevTools (manual XSS/SQLi testing)

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/cybersecurity-webapp-project.git
   cd cybersecurity-webapp-project/app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   npm start
   ```

4. Open the app in your browser at: `http://localhost:3000`

## Project Structure

### Week 1: Security Assessment
- Performed basic scanning using OWASP ZAP and browser tools.
- Discovered issues: XSS, SQLi, and weak password handling.

### Week 2: Fixing Vulnerabilities
- Added input validation (validator)
- Hashed passwords with bcrypt
- Applied JWT-based authentication
- Secured headers with helmet

### Week 3: Logging & Final Report
- Simulated basic attacks with Nmap
- Implemented Winston for logging


## Security Best Practices Checklist

- [x] Input validation and sanitization
- [x] Secure password hashing (bcrypt)
- [x] Token-based authentication (JWT)
- [x] HTTP header protection (helmet)
- [x] Basic logging with Winston
- [x] Manual and automated vulnerability testing


## Contributors

- 👩‍💻 Qamash Bashir - Cybersecurity Intern
- 🧠 Faizan Khan   - Mentor

## License

This project is licensed under the MIT License - see the LICENSE file for details.
