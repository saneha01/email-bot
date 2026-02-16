# email-bot
# 📧 Email Bot – Bulk Email sender

A simple Python automation script that sends personalized internship offer emails in bulk using Gmail SMTP. The bot reads recipient details from a CSV file and attaches a PDF offer letter automatically.

--------------------------------------------------

🚀 FEATURES
• Send personalized emails in bulk  
• Automatically attach offer letters (PDF)  
• Retry mechanism for failed emails  
• Email status logging  
• Secure password handling using environment variables  

--------------------------------------------------

📁 PROJECT STRUCTURE

email_bot/
│── email_bot.py        → Main script  
│── recipients.csv      → Recipient list  
│── resume.pdf          → Attachment file  
│── email_log.txt       → Email sending logs  

--------------------------------------------------

⚙️ REQUIREMENTS

• Python 3.7+  
• Gmail account  
• Gmail App Password  

(Uses mostly built-in Python libraries)

--------------------------------------------------

🔐 SETUP GMAIL APP PASSWORD

1. Enable 2-Step Verification in your Google Account.  
2. Go to Google Account → Security → App Passwords  
3. Generate password for **Mail**  
4. Copy the generated password  

Set it as an environment variable:

Windows (PowerShell)
setx EMAIL_APP_PASSWORD "your_app_password"

Mac/Linux
export EMAIL_APP_PASSWORD="your_app_password"

--------------------------------------------------

📝 CONFIGURE RECIPIENTS

Edit recipients.csv:

email,name,company  
john@email.com,John,ABC Corp  
jane@email.com,Jane,XYZ Ltd  

--------------------------------------------------

📎 ADD ATTACHMENT

Place your offer letter PDF in the project folder and update:

ATTACHMENT_PATH = "resume.pdf"

--------------------------------------------------

▶️ RUN THE BOT

python email_bot.py

--------------------------------------------------

📄 EMAIL PERSONALIZATION

The script automatically personalizes:
• Recipient Name  
• Company Name  
• Subject Line  

To customize the message, edit the template inside:
create_email()

--------------------------------------------------

🛠 CONFIGURATION OPTIONS

Inside email_bot.py:

MAX_RETRIES = 3  
RETRY_DELAY = 5  

--------------------------------------------------

📊 LOGGING

Results are saved in:

email_log.txt

SUCCESS → Email sent  
ERROR → Failed attempt details  

--------------------------------------------------

⚠️ IMPORTANT NOTES

• Gmail limits bulk sending — avoid sending too many emails quickly  
• Always test with your own email first  
• Never share your App Password  
• Ensure the attachment file exists before running  

--------------------------------------------------

👨‍💻 AUTHOR
Saneha

--------------------------------------------------

📜 LICENSE
Free to use for learning and personal automation.
