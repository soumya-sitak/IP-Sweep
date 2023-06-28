# IP-Sweep
The IP Sweep script is a bash script that allows you to scan a range of IP addresses to check for active hosts within that range. This can be useful for network administrators or security professionals who want to quickly identify live hosts on a network.

# Prerequisites
To use the script, ensure that you have the following requirements:

- Linux or macOS operating system
- Bash shell (version 4 or higher)
- Ping utility

# Usage
Follow the syntax below to run the script:

```bash
./ipsweep.sh <IP_ADDRESS_PREFIX>
```

Replace <IP_ADDRESS_PREFIX> with the first three octets of the IP address range you want to scan. For example, if you want to scan the range 192.168.1.1 to 192.168.1.254, you would run the script as follows:

```bash
./ipsweep.sh 192.168.1
```
**Note**: Make sure you have the necessary permissions to execute the script.

# Description
The IP Sweep script uses a for loop to iterate through each IP address in the specified range. It sends a single ICMP echo request (ping) to each IP address and checks for a successful response. The script captures the IP addresses of the live hosts and displays them on the terminal.

If you forget to provide an IP address prefix as a command-line argument, the script will display an error message:

```bash
You forgot an IP address!
Syntax: ./ipsweep.sh <IP_ADDRESS_PREFIX>
```
## Example
Let's assume you want to scan the IP range 192.168.1.1 to 192.168.1.254. Run the script as follows:

```bash
./ipsweep.sh 192.168.1
```
The script will ping each IP address in the range and display the live hosts:

```python
192.168.1.1
192.168.1.10
192.168.1.25
...
```

# Contribution
Contributions to the IP Sweep script are welcome! If you have any suggestions, bug fixes, or additional features, feel free to submit a pull request or open an issue on the GitHub repository.

# License
This script is licensed under the MIT License. Feel free to modify and distribute it as per the license terms.

# Disclaimer
Please note that the IP Sweep script is provided as-is and the author takes no responsibility for its usage or any damages that may occur as a result. Use it responsibly and with proper authorization on networks you have permission to scan.
