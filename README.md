# ITM3
IoT Meter 3 promises give insight on quality of cybersecurity in network-connected consumer devices.

Measured factors are based on evaluating the practical risks of the device in common household-environment.

[Test process documentation](Test_process.md)

# Factors:
ITM3 is based in three measurement factors:
* Privacy (What level of access attacker needs to gain personal information of the user?)
* Communication (What is the strength of technical security and size of attack surface?)
* Device (How easy it is to gain direct access to the device?)

## Protection of privacy:
**What level of access attacker needs to gain personal information of the user?**
* Level 0: 
	* Accessing private information requires access to public network (e.g. port scanning, fingerprinting)
	* Device sends private information unencrypted in the network
* Level 1:
	* Accessing private information requires access to 3rd party database (e.g. shares usage data to marketing companies)
	* Device sends private information to 3rd party database (e.g. Facebook or Google Tag Manager)
* Level 2:
	* Accessing private information requires access to manufacturer-managed systems (e.g. dedicated/self-hosted data processing services)
	* Data sent only to self-hosted backend (e.g. dedicated / cloud-hosted platform operated by the manufacturer; Google Firebase, AWS, etc...)
* Level 3:
	* Accessing private information requires local access to the device (e.g. device does not send any data to Internet)
	* Device has no logging to backend
	* Device requires no registration or login to manufacturer platform
## Protection of communication:
**What is the strength of technical security and size of attack surface?**
* Level 0:
	* Communicates without encryption
	* HTTP
* Level 1:
	* Communicates using known-vulnerable encryption schemes
	* HTTPS with SSL or TLS1.0
	* CBC-mode used with AES
* Level 2:
	* Communicates using good encryption schemes
	* TLS1.2 or TLS1.3
* Level 3:
	* Communicates using PQC encryption schemes
	* AES256 and SHA-2 with TLS1.3
## Protection of device:
**How easy it is to gain direct access to the device?**
* Level 0:
	* Vulnerable to mass-scanning via Internet
	* Has open ports
	* Nessus scan reveals high-risk issues
* Level 1:
	* Vulnerable to customized attacks via Internet
	* Has open ports
	* Nessus scan reveals medium-risk issues
* Level 2:
	* Vulnerable to customized attacks via local network
	* Communicates only to local network devices (e.g. smartphone)
	* Nessus scan reveals low-risk issues
* Level 3:
	* Vulnerable to physical attack via physical access to device
	* No network communication
