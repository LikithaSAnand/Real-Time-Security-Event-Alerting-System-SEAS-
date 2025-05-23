##Features
-Real-Time Monitoring: Uses Python's win32evtlog module to read and parse Windows Security Event Logs in real-time.
-Email Notifications: Automatically sends alert emails to a specified receiver using smtplib and Gmail's App Password authentication.
-Alert Logging: All detected security events are logged into a .txt file for future review and incident response.

###Email Alert Configuration
-Sender Email: Uses a Gmail account to send emails. Authentication is secured using a Gmail App Password.
-Receiver Email: Alerts are delivered to another designated email address.

###Important:
-Replace the sender and receiver email addresses in the script.
-Never share your app password or credentials publicly.
-Enable 2FA on your Gmail account and use App Passwords for authentication.

###Tools & Technologies
-Python 3
-pywin32 (win32evtlog)
-smtplib
-email
-Windows OS (Tested on Windows 10/11)
-Task Scheduler (Optional: For periodic or boot-time script execution)

###Use Cases
-Detecting failed logon attempts
-Monitoring for privilege escalation
-Observing unexpected user account activities
-Tracking other critical security log events

###Security Best Practices
-Store credentials in environment variables or a .env file.
-Use python-dotenv or similar tools to load environment variables securely.
-Add .env to .gitignore to prevent accidental commits of sensitive data.

###How to Use
-Clone this repository.
-Install dependencies:
-pip install pywin32
-Configure the script with your sender and receiver email addresses.
-Generate and use a Gmail App Password.
-Run the script on a Windows machine:
-python seas_monitor.py

Optionally, set up Windows Task Scheduler for continuous monitoring.

