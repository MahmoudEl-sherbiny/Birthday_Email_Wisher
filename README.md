
# 🎂 Birthday Email Wisher in Python

This Python project automatically sends personalized birthday emails using Gmail and a list of birthdays from a CSV file.

---

## ✨ Features

- Checks if today's date matches any birthdays from the list
- Sends a random pre-written birthday message as an email
- Uses Gmail SMTP with secure App Password login
- Fully customizable letter templates
- Uses environment variables for safer password management

---

## 📁 Project Structure

```
project_folder/
├── birthday_wisher.py
├── birthdays.csv
└── letter_templates/
    ├── letter_1.txt
    ├── letter_2.txt
    └── letter_3.txt
```

---

## 📋 Requirements

- Python 3.6 or higher
- `pandas` library

### Install dependencies:

```bash
pip install pandas
```

---

## 🔐 Gmail Setup (Important!)

To allow your script to send emails through Gmail, follow these steps:

### Step 1: Enable 2-Step Verification

- Go to [https://myaccount.google.com/security](https://myaccount.google.com/security)
- Enable **2-Step Verification** on your Google account

### Step 2: Generate an App Password

1. After enabling 2FA, return to the same security page
2. Click on **App Passwords**
3. Sign in again if prompted
4. Under **Select app**, choose `Mail`
5. Under **Select device**, choose your device or select `Other` and name it (e.g., `Python Script`)
6. Click **Generate**
7. Copy the 16-character password shown (e.g., `abcd efgh ijkl mnop`) and **use it in your Python program**

---

## 🔧 Setting Environment Variables

Instead of hardcoding your email and password, set them as environment variables:

### Linux / macOS:

```bash
export GMAIL_USER='your_email@gmail.com'
export GMAIL_APP_PASSWORD='your_app_password'
```

### Windows:

1. Search for "Edit environment variables"
2. Add new **User Variables**:
   - Variable Name: `GMAIL_USER`
   - Variable Value: your Gmail address
   - Variable Name: `GMAIL_APP_PASSWORD`
   - Variable Value: your Gmail App Password

---

## 📌 Usage

Run the script manually:

```bash
python birthday_wisher.py
```

You can also automate it to run daily using:

- **Linux/macOS**: `cron` job
- **Windows**: Task Scheduler

---

## 📁 Sample `birthdays.csv`

```csv
name,email,year,month,day
Ali,ali@example.com,1995,4,24
Sara,sara@example.com,1998,7,10
```

---

## 💌 Sample `letter_1.txt`

```
Dear [NAME],

Wishing you a fantastic birthday filled with joy and happiness!

Your friend,
Birthday Bot
```

You can add more templates like `letter_2.txt`, `letter_3.txt` with different messages.

---

## ✅ Output Behavior

- If there's a birthday today: sends a personalized email to the person
- If not: prints `"No birthdays today."`

---

## 🔒 Security Tip

Avoid hardcoding your password. Use environment variables or a `.env` file to protect sensitive information.

---

## 📬 License

This project is open-source under the **MIT License**. Feel free to use, modify, and share it!

---

## 🙋 Need Help?

If you run into issues with Gmail or want to use services like Mailtrap or SendGrid for testing, feel free to reach out or open an issue.

Happy coding! 🎉
