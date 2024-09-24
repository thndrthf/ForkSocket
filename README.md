
ForkSocket2

ForkSocket2 is a versatile Python-based network utility tool designed for port scanning, phone number lookups, and IP geolocation. It integrates with external APIs like NumVerify and IPSTACK to provide detailed information while ensuring secure and efficient usage through API key management.

Table of Contents

- Features
- Installation
  - Prerequisites
  - Clone the Repository
  - Install Dependencies
  - Setting Up API Keys
- Usage
  - Running the Executable
  - Application Menu
  - Port Scan
  - Phone Number Scan (NumVerify)
  - IP Geolocation Scan (IPSTACK)
- Logging
- Contributing
- License
- Acknowledgements

Features

- Port Scanning: Identify open ports on a target IP address or URL, providing insights into active services.
- Phone Number Lookup: Validate and retrieve information about phone numbers using the NumVerify API.
- IP Geolocation: Obtain detailed geolocation data for IP addresses via the IPSTACK API.
- Progress Indicators: Real-time progress bars during port scans to monitor scan status.
- Loading Screen: Engaging loading screen with ASCII art and thunderbolts to enhance user experience.
- Logging: Comprehensive logging of scan results and geolocation data for future reference.
- API Key Management: Secure handling of API keys through environment variables and manual entry prompts.

Installation

Prerequisites

- Python 3.7 or higher
- pip (Python package installer)
- Git (for cloning the repository)

Clone the Repository

```bash
git clone https://github.com/yourusername/ForkSocket2.git
cd ForkSocket2
```

Install Dependencies

It's recommended to use a virtual environment to manage dependencies:

```bash
# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# On Windows:
venv\Scriptsctivate
# On macOS/Linux:
source venv/bin/activate

# Install required packages
pip install -r requirements.txt
```

Setting Up API Keys

ForkSocket2 requires API keys for the NumVerify and IPSTACK services. You can set these as environment variables or enter them manually when prompted.

Option 1: Environment Variables

Set the following environment variables in your system:

- NUMVERIFY_API_KEY
- IPSTACK_API_KEY

Windows:

1. Open Command Prompt and run:
   ```cmd
   set NUMVERIFY_API_KEY=your_numverify_api_key
   set IPSTACK_API_KEY=your_ipstack_api_key
   ```

2. To set them permanently, go to System Properties > Advanced > Environment Variables and add them under User variables or System variables.

macOS/Linux:

1. Open Terminal and run:
   ```bash
   export NUMVERIFY_API_KEY=your_numverify_api_key
   export IPSTACK_API_KEY=your_ipstack_api_key
   ```

2. To set them permanently, add the above lines to your shell configuration file (`~/.bashrc`, `~/.zshrc`, etc.) and run `source ~/.bashrc` or `source ~/.zshrc`.

Option 2: Manual Entry

If you prefer not to set environment variables, the application will prompt you to enter your API keys upon running.

Usage

Running the Executable

After installing dependencies and setting up API keys, you can run ForkSocket2 using Python:

```bash
python ForkSocket2.py
```

Alternatively, if you've packaged it as an executable using PyInstaller, run the executable file directly.

Application Menu

Upon launching, you'll see a loading screen with ASCII art, followed by a menu with the following options:

1. Port Scan
2. Phone Number Scan (NumVerify)
3. IP Geolocation Scan (IPSTACK)
4. Exit

Port Scan

1. Select Option 1: Port Scan
2. Enter Target: Input the IP address or URL you wish to scan.
3. Progress Bar: A real-time progress bar will display the scanning status.
4. Results: Open ports will be listed and logged in the `portscans` directory with a timestamped log file.

Phone Number Scan (NumVerify)

1. Select Option 2: Phone Number Scan
2. Enter Phone Number: Input the phone number in E.164 format (e.g., +14155552671).
3. Results: Validity, country, carrier, and line type information will be displayed and logged in the `phone_scans` directory.

IP Geolocation Scan (IPSTACK)

1. Select Option 3: IP Geolocation Scan
2. Enter IP/URL: Input the IP address or URL you wish to geolocate.
3. Results: Geolocation details including country, region, city, latitude, and longitude will be displayed and logged in the `ip_geolocations` directory.

Exit

Select Option 4 to gracefully exit the application.

Logging

ForkSocket2 maintains comprehensive logs for each type of scan:

- Port Scans: Stored in the `portscans` directory with files named as `portlist_<timestamp>.txt`.
- Phone Number Scans: Logged in `phone_scans/phone_scans.txt`.
- IP Geolocation Scans: Logged in `ip_geolocations/ip_geolocations_log.txt`.

Ensure these directories exist or allow the application to create them automatically upon first run.

Contributing

Contributions are welcome! To contribute:

1. Fork the Repository
2. Create a Feature Branch
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Commit Your Changes
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to the Branch
   ```bash
   git push origin feature/YourFeature
   ```
5. Open a Pull Request

Please ensure your code follows the project's coding standards and includes necessary documentation.

License

This project is licensed under the MIT License.

Acknowledgements

- Rich Library: For enhancing terminal UI with progress bars and styled text.
- NumVerify API: For providing robust phone number validation and information.
- IPSTACK API: For comprehensive IP geolocation data.
- Phonenumbers Library: For parsing and validating phone numbers.
- Python Community: For continuous support and resources.
