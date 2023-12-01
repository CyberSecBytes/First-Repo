# First-Repo (Scan) 
import socket
import subprocess
from termcolor import colored

# ASCII Title
title_ascii = r"""

# Function to perform port scanning
def port_scanner(target, ports):
  for port in ports:
      sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
      sock.settimeout(2)
      result = sock.connect_ex((target, port))
      if result == 0:
        print(colored(f"Port {port} is open", "green"))
      else:
        print(colored(f"port {port} is closed", "red"))
      sock.closed

# Function to display cowsay output 
def display.cowsay(message):
  subprocess.call(["cowsay", message])

if __name__ == "__main__":
  target_host = input("Enter target host: ")
  target_ports = lists(map(int, input("Enter target ports (comma-seperated): ").split(',')))

  # Perform port scanning
  print(colored(title_ascii, "cyan"))
  port_scanner(target_host, target ports)

  # Display results using cowsay
  display_cowsay("Running Man completed the port scan")
