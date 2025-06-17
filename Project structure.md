🔍 Week 1: Security Assessment
🎯 Objectives
Understand how the application works.

Perform basic vulnerability testing (manual + tools).

Identify critical weaknesses such as:

XSS (Cross-Site Scripting)

SQL Injection (SQLi)

Weak password storage or plaintext credentials

🧪 Tools Used
OWASP ZAP: Automated vulnerability scanner.

Browser DevTools: Manual testing for form inputs, payload injection.

Manual Payloads:

"<script>alert('XSS')</script>" for XSS

' OR '1'='1 for SQL Injection

📝 Tests Performed
XSS: Input script tags into user profile and search fields.

SQL Injection: Test login form with:

Username: admin' OR '1'='1
Password: anything

📌 Findings
❌ XSS vulnerability found on profile update.
❌ Login could be bypassed using SQL injection.
❌ Passwords were stored in plaintext in the database.

🛠️ Week 2: Implementing Security Fixes
🎯 Goals
Fix vulnerabilities discovered in Week 1.

Harden the backend against common attack vectors.

🔐 Packages Installed
npm install validator bcrypt jsonwebtoken helmet

✅ Fixes Applied
Input Validation:

Used validator to ensure correct data format (e.g., emails, text fields).
Example:
if (!validator.isEmail(email)) {
  return res.status(400).send('Invalid Email');
}

Password Hashing:
   Used bcrypt to hash and salt user passwords before storing.
const hashedPassword = await bcrypt.hash(password, 10);

JWT-based Authentication:
   Added login tokens using jsonwebtoken.
const token = jwt.sign({ id: user._id }, 'your-secret-key');
res.send({ token });

HTTP Header Protection:
  Enabled helmet to secure HTTP headers.
const helmet = require('helmet');
app.use(helmet());

📈 Week 3: Logging & Final Reporting
🎯 Objectives
Add basic security logging.
Simulate attacks and document mitigation.
Summarize project in a final security checklist.

🧪 Penetration Testing Tools
Nmap: Used for port scanning and basic recon.
nmap -sV -p 3000 localhost
📝 Logging (Winston Setup)
Installed Winston:
npm install winston

Created logs/logger.js:
const winston = require('winston');
const logger = winston.createLogger({
  transports: [
    new winston.transports.Console(),
    new winston.transports.File({ filename: 'logs/security.log' })
  ]
});
module.exports = logger;
Used in routes:
logger.info(`Login attempt from ${email}`);
