import os
import socket
import requests
import paramiko
from datetime import datetime

REMOTE_IP = "192.168.56.104"
USERNAME = "diablo" 
PASSWORD = "Hellblaze@354" 

def test_ssh_connection():
    try:
        ssh = paramiko.SSHClient()
        ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy())

        ssh.connect(REMOTE_IP, username=USERNAME, password=PASSWORD)
        print(f"Connected to {REMOTE_IP}")

        stdin, stdout, stderr = ssh.exec_command("echo Hello from Linux!")
        print(stdout.read().decode())

        ssh.close()
    except Exception as e:
        print(f"Error: {e}")

def show_date_time():
    """Display the local date and time."""
    print("\nLocal Date and Time:")
    print(datetime.now().strftime("%Y-%m-%d %H:%M:%S"))

def show_ip_address():
    """Display the local computer's IP address."""
    print("\nLocal Computer IP Address:")
    ip_address = socket.gethostbyname(socket.gethostname())
    print(ip_address)

def show_remote_home_directory():
    """Show the home directory listing of the remote Linux machine."""
    try:
        ssh = paramiko.SSHClient()
        ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy())
        ssh.connect(REMOTE_IP, username=USERNAME, password=PASSWORD)

        stdin, stdout, stderr = ssh.exec_command("ls ~")
        print("\nRemote Home Directory Listing:")
        for line in stdout.readlines():
            print(line.strip())

        ssh.close()
    except Exception as e:
        print(f"Error connecting to the remote server: {e}")

def backup_remote_file():
    """Back up a remote file by renaming it with a .old suffix."""
    file_path = input("\nEnter the full path of the file to back up: ")

    try:
        ssh = paramiko.SSHClient()
        ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy())
        ssh.connect(REMOTE_IP, username=USERNAME, password=PASSWORD)

        backup_path = file_path + ".old"
        ssh.exec_command(f"mv {file_path} {backup_path}")
        print(f"File backed up as: {backup_path}")

        ssh.close()
    except Exception as e:
        print(f"Error connecting to the remote server: {e}")

def save_web_page():
    """Save the HTML content of a web page to a local file."""
    url = input("\nEnter the URL of the web page: ")
    file_name = input("Enter the file name to save the web page (e.g., page.html): ")

    try:
        response = requests.get(url)
        response.raise_for_status()
        with open(file_name, "w", encoding="utf-8") as file:
            file.write(response.text)
        print(f"Web page saved as: {file_name}")
    except Exception as e:
        print(f"Error saving the web page: {e}")

def main():
    """Main menu for the program."""
    while True:
        print("\nMenu:")
        print("1 - Show date and time ")
        print("2 - Show IP address")
        print("3 - Show Remote home directory listing")
        print("4 - Backup remote file")
        print("5 - Save web page")
        print("Q - Quit")

        choice = input("Enter your choice: ").strip().upper()

        if choice == "1":
            show_date_time()
        elif choice == "2":
            show_ip_address()
        elif choice == "3":
            show_remote_home_directory()
        elif choice == "4":
            backup_remote_file()
        elif choice == "5":
            save_web_page()
        elif choice == "Q":
            print("Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")

if __name__ == "__main__":
    main()
