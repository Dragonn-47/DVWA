# besic linux cmd

- Demonstrate basic Linux commands useful for penetration testing.
    
    ## 1. File and Directory Navigation
    
    These help you move around the system to find configuration files, logs, or install tools.
    
    | Command | Use in Penetration Testing | Example |
    | --- | --- | --- |
    | **`ls -la`** | Lists all files (`-a`) in long format (`-l`), showing permissions, owners, and sizes. Crucial for checking file permissions and ownership. | `ls -la /var/www/html` |
    | **`cd`** | Change directory. Use this to access log directories or web roots. | `cd /var/log/apache2` |
    | **`pwd`** | Prints the current working directory. Essential for knowing your current location on a compromised system. | `pwd` |
    | **`cat`** | Outputs the content of a file. Used to quickly view small configuration or password files. | `cat /etc/passwd` |
    
    Export to Sheets
    
    ---
    
    ## 2. System and Network Information
    
    These are vital for initial reconnaissance and post-exploitation information gathering.
    
    | Command | Use in Penetration Testing | Example |
    | --- | --- | --- |
    | **`ip a`** or **`ifconfig`** | Shows network interfaces and IP addresses. Used to confirm your machine's IP for listener setup or to check a target's local IPs. | `ip a` |
    | **`ping`** | Tests network connectivity to a target host. | `ping 192.168.1.1` |
    | **`netstat -antp`** | Displays active network connections, listening ports (`-l`), and associated programs (`-p`). Great for finding services running on a target. | `netstat -antp` |
    | **`whoami`** | Shows the current user ID. Essential after gaining initial access to confirm your privileges. | `whoami` |
    | **`uname -a`** | Shows detailed information about the kernel. Used to identify the target's operating system version to search for specific exploits. | `uname -a` |
    | **`history`** | Shows a list of recently executed commands. Useful for an attacker to see what the previous user was doing, or for a blue teamer to find attacker activity. | `history` |