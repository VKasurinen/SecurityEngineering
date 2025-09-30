## Task 1: Bring your own devices

## Intrusive application practices  

Apps that are aggressive and want access to your device's data. For example, contacts, location, or microphone without any specific reason. They can steal personal or business information. So that is, a flashlight app that demands access to your contacts and photos is being intrusive. 

## Account credential theft through phishing 

Attackers trick you into entering your username and password on a fake website or through a deceptive message. So you get a text message that looks like it came from IT and asks you to verify your account, but it's a scam and it steals your login information. 

 ## outdated phones  

Using a mobile operating system (OS) that is no longer supported with security updates. This leaves known weaknesses unpatched, making the device easy to hack. 

## Sensitive data transmissions  

Sending work data over unencrypted networks, for example a public wifi, where anyone can eavesdrop and see the information. 

## Brute-force attacks to unlock a phone  

An Attacker repeatedly guesses your passcode to gain access to your device, often using automated tools. 

## Application credential storage vulnerability  

An app stores your login information (passwords, tokens) in an insecure way on the device, allowing other apps or malware to find and steal them. 

## Unmanaged device protection  

A personal device that is not enrolled in the company's management system. The company cannot enforce security policies (like requiring a passcode) or protect its data on that device. 

## Lost or stolen data protection  

The risk of corporate data being exposed if an employee loses their phone or it is stolen. 

## Protecting enterprise data from being inadvertently backed up to a cloud service 

Work documents or emails being automatically saved to a employee's personal cloud account (like iCloud or Google Drive), outside the company's control and security. 

---

## Task 2: Attacks on CPU execution 


Zombieload exploits the internal buffers of processors. When the processor encounters an error, it launches a "microcode assistant" to fix it. During this process, a malicious process can temporarily load data left in these buffers, which can leak information from other applications or even kernel memory. The target was mainly Intel processors (from 2011-2019, including Coffee Lake, Skylake). Protection then required microcode updates and operating system patches. 

The Downfall attack exploits the VGAther instruction, which is designed to efficiently load data from scattered memory addresses. An attacker can manipulate this instruction to temporarily load data from the processor's internal vector registers, which contain data from a previous process running on the same core. This targeted a wide range of Intel processors including Skylake, Tiger Lake and Ice Lake. This was protected by a microcode update that introduces a new control bit GDS_CTRL 

The Inception attack manipulated the processor's return stack buffer, which predicts the destinations of ret instructions (function return values). This targeted all AMD Zen family processors. This was protected by operating system-level fixes. lfence instructions were added to the Linux kernel at critical points to slow down execution and prevent exploitation of the misprediction. 

---

## Task 3: Securing OS 

## Malware and Viruses  

They can take over your files, spy on you, use your system as a botnet, or steal passwords and money. Linux can help with this by restricting process permissions, using package repositories, SELinux sandboxing, and keeping packages up to date. It uses both OS-internal features and external ones. The basic restrictions, package management, and sandboxes are Linux-specific, but in addition to this, you can use malware scanners as external tools for this. 

## Exploiting Software Vulnerabilities  

Here, the attacker executes remote code that can, for example, crash a service or gain access to the system and obtain information. Linux prevents this with regular updates, package management, minimizing permissions, and clear permissions policies. These are mainly Linux-specific features. 

## Phishing and Social Engineering  

The downside to this is identity/account information theft, unauthorized money transfers, or access to internal systems via the user. Linux can prevent this by using browser protections and separate user modes, as well as by preventing automatic execution of non-executable attachments. These are mostly external tools you can use to protect yourself. 

## Drive-by Downloads  

The disadvantage here is that the malware is downloaded and run through just the browser or a vulnerable extension, which can lead to harm without the user downloading any files separately. Linux can prevent this by using up-to-date browsers, browser process isolation, limiting browser add-ons, minimizing permissions. This is partly due to the OS's own protections and also external ones can be used such as adblocks and other web security services. 

## Zero-Day Exploits  

Here, attackers exploit an unknown vulnerability, so there is no immediate fix, so there is a possibility of a large-scale compromise or data leak. Linux prevents this with a multi-layered defense and has a rapid update policy, anti-exploit technologies, and exploit prevention. There are both external and internal protections here. Linux has good internal protection mechanisms, but this type of vulnerability requires external tools to detect or repair it. 

## USB/Removable Media Attacks  

The disadvantages of this include firmware-level attacks, data theft, or malware distribution via a networked machine. Linux prevents this by preventing autorun, using mount options, restricting mount permissions, using isolated permissions, and disabling USB ports when necessary. Most of these are Linux-specific features. 

## Password Cracking 

The downside to this is account hijacking, service abuse, and broader access to internal resources. Using strong passwords, using strong hashing algorithms, using two-factor authentication (MFA), and enforcing strong password policies. In addition, user education and password management. MFA solutions and password managers are often external. 

---

## Task 4: Logging 

## Application logs  

This is where application errors, user actions, configuration errors, and performance information are stored. The location is usually Windows: C:\Program Files\<application>\logs Linux: /var/log/<appname>.log and MACOS: /Library/Logs. Threats from these logs are unauthorized login attempts to applications, repeated errors (DoS attempts), suspicious input data. 

## Event logs  

This is where operating system events are stored, such as logins, program installations, security events. Location in Windows: C:\Windows\System32\winevt\Logs\ Linux: /var/log/auth.log MACOS: /var/log/. Detected threats here are failed logins, suspicious installations, system crashes that could be a potential attack. 

## Service logs  

This is where status information and errors of web services, databases, web servers, e.g. Apache, MySQL, are stored. Location in Windows C:\inetpub\logs\LogFiles\ e.g. apache Linux: /var/log/apache2/ MACOS: /var/log/apache2/. These can be used to detect brute force attacks on the web service, service crashes, and suspicious traffic volume. 

## System logs 

This is where the operating system kernel, drivers, boot processes, and device errors are stored. Location MACOS: /var/log/system.log Linux: /var/log/syslog. Threats that can be detected from these include: kernel panic errors, suspicious drivers, and unauthorized device attempts. 

On Windows, you can monitor logs from PowerShell: "Get-EventLog" or with third-party monitoring programs. On MacOS, you can monitor them with the "log show" command and on Linux, you can monitor them with the "journalctl" command, and of course, all operating systems have external graphical tools that can be used for this. 

https://en.wikipedia.org/wiki/Logging_(computing) 

https://sematext.com/glossary/log-file/ 

https://www.sumologic.com/glossary/log-file  


