## Guess Login

This Python script performs a brute-force password guessing attack against a login page, attempting to guess the correct password for a specified username by iterating through a list of common passwords.

### Features

- **Login Brute Force**: Uses a dictionary attack method to submit a series of password guesses.
- **Real-Time Feedback**: Reports the correct password when found, then exits.
- **Customizable Target URL and Username**: Easily modify the `target_url` and `username` fields to target different login pages.

### How It Works

The script sends a POST request with a username and a password guess to the target login page. It iterates through each password in a specified wordlist file and monitors the response content for indicators of a successful login attempt.

### Usage

1. **Set Target URL and Username**
   - Update `target_url` and `username` with the appropriate values for your testing environment:
     ```python
     target_url = "http://192.168.**.**/dvwa/login.php"
     data_dict = {"username": "admin", "password": "", "Login": "submit"}
     ```

2. **Run the Script**
   - Use the following command:
     ```bash
     python guess_login.py
     ```

### Requirements

- **Python 3.x**
- **Requests Library**: Install using:
  ```bash
  pip install requests
  ```

### Wordlist

Ensure you have a wordlist file (`common.txt`) containing passwords you want to test, and place it in the specified path:
```plaintext
/home/kali/Downloads/common.txt
```

### Example

Running the script might produce:
```bash
[+] Got the password --> password123
```
If no password is found, it will display:
```bash
[+] Reached end of line!
```

### Important Note

This script is intended for **use only on systems you have permission to test**. Unauthorized access attempts are illegal and unethical.

### Authors

- [Zaid Sabih](https://ie.linkedin.com/in/zaid-sabih-al-quraishi-5444a6127)
- [Uzoeshi Daniel](https://www.linkedin.com/in/daniel-ikenna-33b709235)
