📊 Periodic Process Logger 📜
Welcome to the Periodic Process Logger project! This Python-based script logs information about the processes running on your machine at regular intervals. It generates a log file, and if there's an internet connection, it sends the log via email as an attachment.

🚀 Features

📝 Log Running Processes: Captures PID, process name, username, and memory usage (VMS).

📂 Save Logs: Saves logs in a timestamped file within a specified directory.

📧 Email Logs: Automatically sends the log file as an email attachment when connected to the internet.

⏱️ Periodic Execution: Allows the script to run at user-defined intervals.

📋 Prerequisites
Python 3.x
Libraries: psutil, schedule, smtplib, ssl, urllib, time, os
Email account (for SMTP sending)

📚 Usage
To run the script periodically with a specific time interval (in minutes), use the following command:
python periodic_process_logger.py <time_interval_in_minutes>

Example:
python periodic_process_logger.py 10
This will run the process logger every 10 minutes.

To view help or usage information:
python periodic_process_logger.py -h

To get usage instructions:
python periodic_process_logger.py -u

🔧 How It Works
1.The script checks for running processes using the psutil library and logs relevant information such as process ID (PID), process name, username, and memory usage.

2.The log is saved in a directory (LogFiles by default). Each log file is named with a timestamp.

3.The script checks if there is an active internet connection. If so, it emails the log file to the specified email addresses.

4.The email contains the log file as an attachment and a message with the log generation timestamp.

⚙️ Configuration
Email Configuration: Set your email addresses in the script (fromaddr and toaddr). You will need an app password if you're using Gmail.
Log Directory: The logs are stored in a folder called LogFiles (it will be created automatically if it doesn’t exist).

🧑‍💻 Example Output
The generated log will look something like this:
--------------------------------------------------------------------------------
Process Logger : Mon Feb 18 14:20:30 2025
--------------------------------------------------------------------------------

{'pid': 1234, 'name': 'python', 'username': 'user1', 'vms': 128.34}
{'pid': 5678, 'name': 'chrome', 'username': 'user2', 'vms': 204.56}
...

Error Handling
❌ No Internet Connection: The script won’t send the email if there’s no internet connection.

⚠️ Invalid Input: If you provide an invalid time interval, the script will display an error message.

Author
Atharva Borawake
