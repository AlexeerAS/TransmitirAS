# Transmitir AS

This project implements a Windows service that automatically backs up SQL Server databases and uploads them to an SFTP server. 

## Project Structure

```
transmitiras
├── src
│   ├── main.py          # Implementation of the BackupService class
│   └── config.ini       # Configuration file for database and SFTP settings
├── requirements.txt     # List of dependencies required for the project
└── README.md            # Documentation for the project
```

## Installation

1. **Clone the repository:**
   ```
   git clone https://github.com/AlexeerAS/TransmitirAS.git
   cd transmitiras
   ```

2. **Install dependencies:**
   Ensure you have Python installed, then run:
   ```
   pip install -r requirements.txt
   ```

3. **Compile:**
   ```
   py -m  PyInstaller .\TransmitirAS.spec
   py -m  PyInstaller .\reload.spec   
   ```

4. **Create the installer:**
   Use inno setup and execute TransmitirAS.iss

5. **Install the service:**
   Run TransmitirAS_Installer.exe

6. **Configure the service:**
During the installation, you will be prompted to enter the database configuration, backup settings, and SFTP settings. Follow the instructions on each page to complete the configuration.

7. **Uninstall the service:**
To uninstall the service, run the uninstaller from the Start Menu or from the installation directory. This will also remove the `service_logs.log` file from the application directory.

