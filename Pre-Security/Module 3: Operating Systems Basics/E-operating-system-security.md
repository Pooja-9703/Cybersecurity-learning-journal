# E. Operating System Security

## Operating System Security

A computer has hardware interfaces for all the computer parts and peripherals that you can interact with using your hands. Hardware includes the screen, keyboard, printer, USB flash memory, and the desktop board.

The desktop board is the main part of a computer, and all the other pieces of hardware, from the keyboard and mouse to the screen and printer, connect to it. However, hardware components by themselves are useless if you want to run programs and applications. We need an **Operating System (OS)** to control and manage them.

### Hardware and Software

- **Hardware** → Physical components such as CPU, memory, storage, screen, keyboard, etc.
- **Software** → Programs and operating systems.

Examples of programs:
- Firefox
- Chrome
- Microsoft Office
- WhatsApp

Examples of operating systems:
- Android
- Microsoft Windows
- iOS
- macOS
- Linux

The **OS is the layer between the hardware and applications/programs**. Programs and applications cannot directly interact with the computer hardware. Instead, they run on top of the OS, which allows them to access hardware according to specific rules.

> **Note:** Mozilla Thunderbird is an email program.

## Common Examples of OS Security

There are three main weaknesses targeted by malicious users:

### 1. Authentication & Weak Passwords

**Authentication** is the act of verifying your identity, whether it is a local or remote system.

Authentication can be achieved in three main ways:

- **Something you know** → PIN or password
- **Something you are** → Fingerprint
- **Something you have** → A phone number through which you can receive an SMS message

Since passwords are the most common form of authentication, they are also one of the most commonly attacked.

Many users choose easy-to-guess passwords or reuse the same password on multiple websites. Some users also rely on personal details because they are easy to remember and may seem unknown to attackers.

Attackers are aware of these tendencies. If an attacker guesses the password of one of your online accounts, they may gain access to your private data.

Therefore:

- Choose complex passwords.
- Use different passwords for different accounts.
- Avoid using easily guessable personal information.

### 2. Weak File Permissions

Proper security follows the principle of **least privilege**.

Weak file permissions can make it easier for an adversary to attack **confidentiality** and **integrity**.

- Weak permissions may allow attackers to access files they should not be able to access.
- They may attack **confidentiality** by accessing information that should remain private.
- They may attack **integrity** by modifying files that they should not be able to edit.

### 3. Access to Malicious Programs

Depending on the type of malicious program, it can attack:

- Confidentiality
- Integrity
- Availability

Some types of malicious programs, such as **Trojan horses**, can give an attacker access to your system. Consequently, the attacker may be able to read your files or even modify them.

Some malicious programs, such as **ransomware**, attack availability.

Ransomware is a malicious program that encrypts the user's files. Encryption makes the file(s) unreadable. The attacker then offers the user the ability to restore availability if the ransom is paid.

## Note: Command History

The `history` command displays the commands you previously typed in the terminal.

Different operating systems and shells provide different commands for viewing command history:

- **Linux** → `history`
- **Windows CMD** → `doskey /history`
- **Windows PowerShell** → `Get-History` or `history`
