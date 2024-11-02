# IP Address Monitoring with Toast Notifications

This PowerShell script monitors the status of specified IP addresses and sends a toast notification if any go down. It uses the `BurntToast` module to generate notifications on Windows, making it easy to stay informed about network connectivity issues in real time.

## Features
- Monitors multiple IP addresses continuously.
- Sends a toast notification when an IP address goes down.
- Logs each status change to a local log file.
- Allows customization of check intervals.

## Prerequisites
1. **BurntToast Module**: This script requires the [BurntToast](https://github.com/Windos/BurntToast) module to send notifications.
   - Install BurntToast by running:
     ```powershell
     Install-Module -Name BurntToast -Force -Scope CurrentUser
     ```
2. **PowerShell**: Ensure you’re running PowerShell on Windows with admin privileges for best results.

## Usage

1. **Import the BurntToast Module**:
   ```powershell
   Import-Module BurntToast
2. Define IP Addresses to Monitor: Update the $ipAddresses variable with the IP addresses you want to monitor:
   $ipAddresses = "8.8.8.8", "192.168.1.1", "10.0.0.2"

3. Run the Script: Execute the script. It will continuously check each IP address and display a toast notification if any go offline. 
   A log file (IPStatusLog.txt) will be created in the script's directory, recording each status change.
4. Adjust Check Frequency: Modify the delay between checks by adjusting the Start-Sleep -Seconds 30 line.

# Code Overview
  Check-IPStatus Function: Checks the status of an IP address by pinging it. If the IP address is down and its status has changed, a toast notification is triggered, and the status is logged.
  Infinite Loop: The script continuously monitors each IP address in the $ipAddresses array with a 30-second delay between checks.
# Example Notification
  The notification displays the IP address status and timestamp. Customize notification settings (like sound) within the New-BurntToastNotification call in the Check-IPStatus function.

Here’s a README.md for your GitHub project:

markdown
Copy code
# IP Address Monitoring with Toast Notifications

This PowerShell script monitors the status of specified IP addresses and sends a toast notification if any go down. It uses the `BurntToast` module to generate notifications on Windows, making it easy to stay informed about network connectivity issues in real time.

## Features
- Monitors multiple IP addresses continuously.
- Sends a toast notification when an IP address goes down.
- Logs each status change to a local log file.
- Allows customization of check intervals.

## Prerequisites
1. **BurntToast Module**: This script requires the [BurntToast](https://github.com/Windos/BurntToast) module to send notifications.
   - Install BurntToast by running:
     ```powershell
     Install-Module -Name BurntToast -Force -Scope CurrentUser
     ```
2. **PowerShell**: Ensure you’re running PowerShell on Windows with admin privileges for best results.

## Usage

1. **Import the BurntToast Module**:
   ```powershell
   Import-Module BurntToast
Define IP Addresses to Monitor: Update the $ipAddresses variable with the IP addresses you want to monitor:

powershell
Copy code
$ipAddresses = "8.8.8.8", "192.168.1.1", "10.0.0.2"
Run the Script: Execute the script. It will continuously check each IP address and display a toast notification if any go offline. A log file (IPStatusLog.txt) will be created in the script's directory, recording each status change.

Adjust Check Frequency: Modify the delay between checks by adjusting the Start-Sleep -Seconds 30 line.

Code Overview
Check-IPStatus Function: Checks the status of an IP address by pinging it. If the IP address is down and its status has changed, a toast notification is triggered, and the status is logged.
Infinite Loop: The script continuously monitors each IP address in the $ipAddresses array with a 30-second delay between checks.
Example Notification
The notification displays the IP address status and timestamp. Customize notification settings (like sound) within the New-BurntToastNotification call in the Check-IPStatus function.

Enjoy effortless network monitoring with real-time notifications! 🎉
