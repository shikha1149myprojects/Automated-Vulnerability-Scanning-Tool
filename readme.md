# Security Tools Automation

This project involves creating scripts to automate the installation of specific security tools and running scans on a target IP address. The main tasks are:

1. **Installation Script (install_main.sh)**
2. **Scan Script (script_scan.sh)**

## Installation Script (install_main.sh)

### Purpose
To install necessary security tools (like figlet, postfix, nikto, rustscan, and feroxbuster) if they are not already installed on the system.

### Process
- Checks if each tool is installed.
- If not, installs the tool.
- Sets the correct permissions for the tools.
- Prints confirmation messages to indicate the progress and completion of the installation.

## Scan Script (script_scan.sh)

### Purpose
To perform a security scan on a given IP address, detect open ports, and send an email with the scan results.

### Process
- Takes an IP address as input.
- Runs RustScan on the IP address to find open ports.
- If port 80 (HTTP) is open, runs Feroxbuster to discover directories.
- Saves the results in a file called `results.txt`.
- Prompts the user for an email address and sends the results to this email.

## Summary
We are automating the setup and use of security tools to scan a target IP address and report the findings. One script installs the tools, while the other runs the scans and sends the results via email. The scripts ensure that tools are installed if needed, perform scans, and alert the user with the results.

## Usage

1. Clone the repository:
    ```sh
    git clone https://github.com/aryan-nair69/Swiftsafe-assignment.git
    cd Swiftsafe-assignment
    ```

2. Make the scripts executable:
    ```sh
    chmod +x install_main.sh
    chmod +x script_scan.sh
    ```

3. Run the installation script:
    ```sh
    ./install_main.sh
    ```

4. Run the scan script:
    ```sh
    ./script_scan.sh
    ```
