# NETWORKWALKS-B083-WK3-PM1-PM2-PROJECT
PDF PASSWORD CRACKING

---

🔐 PDF Password Cracking Lab — John the Ripper & NetworkWalks

📌 Overview

As part of my cybersecurity learning journey, I completed a hands-on password-cracking exercise focused on encrypted PDF files.

The objective of this lab was to understand how password-protected files can be assessed when the password hash is available, and how dictionary-based password attacks work in a controlled cybersecurity environment.

For this exercise, I used:

John the Ripper on Windows

NetworkWalks Password Cracker Lab

Hash Calculator

Dictionary attack

Encrypted PDF files

Windows environment


> ⚠️ Ethical Notice: This exercise was performed strictly in a controlled training environment using authorized files. Password-cracking techniques should only be used on files, systems, or accounts that you own or have explicit permission to test.




---

🛠️ Tools Used

1. John the Ripper

John the Ripper is a password-security auditing and password-recovery tool that can test password hashes against different password candidates.

For this lab, I downloaded the Windows version of John the Ripper and extracted the program before using it from the command line.

2. NetworkWalks Password Cracker

I also used the NetworkWalks private password-cracking application provided as part of the training environment.

The application provided two important components:

Hash Calculator

Password Cracker


This allowed me to extract/process the PDF password hash and perform a dictionary-based attack against the authorized training PDF.


---

🔎 Lab Workflow

The overall workflow was:

Encrypted PDF
     │
     ▼
Extract PDF Hash
     │
     ▼
Hash Calculator
     │
     ▼
Dictionary Attack
     │
     ├── John the Ripper
     │
     └── NetworkWalks Password Cracker
     │
     ▼
Recovered Password
     │
     ▼
Open Encrypted PDF


---

💻 Part 1 — Installing John the Ripper on Windows

I downloaded the Windows build of John the Ripper Jumbo and extracted it to my computer.

After extracting the files, I navigated to the run directory where the John executable and supporting tools are located.

I then opened Command Prompt/PowerShell in the directory and verified that John was working.

A basic verification command is:

john.exe --help

This displays the available John the Ripper options.


---

🔐 Part 2 — Preparing the PDF

The next step was to work with an encrypted PDF supplied for the training exercise.

The PDF itself was password protected, so instead of attempting to modify or bypass the PDF directly, I first needed to obtain the information required for password testing.

The general process is:

PDF → PDF hash → Password candidates → Hash comparison

For John the Ripper, a PDF hash extraction utility such as pdf2john can be used to prepare the hash for John.

For example:

pdf2john.pl encrypted.pdf > pdf_hash.txt

Depending on the John the Ripper version and Windows setup, the extraction utility may have a slightly different filename or require the appropriate scripting environment.


---

📖 Part 3 — Dictionary Attack with John the Ripper

Once the PDF hash had been prepared, I used a dictionary-based attack.

The basic workflow is:

john.exe --wordlist=passwords.txt pdf_hash.txt

John then tests passwords from the wordlist against the extracted hash.

To display a recovered password:

john.exe --show pdf_hash.txt

The important concept I learned here is that John isn't simply "decrypting" the PDF. It is testing password candidates and checking whether one produces the correct cryptographic result.


---

🌐 Part 4 — NetworkWalks Password Cracker

I also completed the exercise using the NetworkWalks training environment.

The platform provided a dedicated Hash Calculator and Password Cracker.

The process involved:

Step 1 — Obtain the PDF hash

I extracted the required PDF hash and supplied it to the training platform's hash calculator.

Step 2 — Submit the hash

The resulting hash was entered into the NetworkWalks password-cracking interface.

Step 3 — Run the dictionary attack

The password cracker tested entries from its wordlist against the supplied hash.

The interface displayed the progress of the attack, including attempted password candidates.

Step 4 — Password recovered

The correct password was eventually identified by the application.

I then used the recovered password to open the encrypted PDF and verify that the result was successful.


---

🧪 Results

I successfully completed the password-cracking exercise using two different approaches:

Tool	Technique	Result

John the Ripper	Dictionary attack	✅ Successful
NetworkWalks Password Cracker	Dictionary attack	✅ Successful
NetworkWalks Hash Calculator	PDF hash processing	✅ Successful
Encrypted PDF	Password verification	✅ Successfully opened


The NetworkWalks lab also provided confirmation that I had successfully captured the required flags.


---

🧠 What I Learned

This exercise helped me understand several important cybersecurity concepts:

🔹 Password Hashing

Passwords should not normally be stored as plaintext. Instead, systems use cryptographic mechanisms to protect password information.

🔹 Dictionary Attacks

A dictionary attack uses a predefined list of possible passwords rather than trying every possible combination.

This demonstrates why predictable passwords such as:

password
password1
123456
qwerty

are poor security choices.

🔹 Password Complexity

The exercise reinforced the importance of using passwords that are:

Long

Unique

Difficult to guess

Not based on common words

Not reused across different services


🔹 Password Cracking vs. Decryption

One important distinction I learned is that password cracking is generally about finding the password that produces the expected cryptographic result, whereas decryption refers to using the correct cryptographic key/password to recover protected content.


---

🚧 Challenges Encountered

One of the challenges was understanding the relationship between the encrypted PDF, its hash, the wordlist, and the password-cracking tool.

Initially, it can be easy to think:

PDF → John → Password

But the actual process is closer to:

Encrypted PDF
      ↓
Extract password-verification data
      ↓
Generate/obtain suitable hash representation
      ↓
Provide password candidates
      ↓
Compare candidates
      ↓
Recover matching password

Understanding this workflow made the exercise much clearer.


---

📸 Evidence

Screenshots from the lab are included in this repository showing:

1. John the Ripper running on Windows


2. Password-cracking progress


3. Successful password recovery


4. NetworkWalks Hash Calculator


5. NetworkWalks Password Cracker


6. Successfully unlocked PDF


7. NetworkWalks flag capture



Important: I have intentionally excluded sensitive credentials, personal information, and reusable passwords from the public documentation.


---

🎯 Key Takeaway

This lab gave me practical exposure to password auditing, hash-based password verification, dictionary attacks, and password security.

More importantly, it reinforced that cybersecurity isn't just about learning tools—it's about understanding how attacks work so that better defensive controls can be implemented.

Going forward, I want to continue building practical skills around:

Password security

Authentication security

Hashing algorithms

SIEM

Network security

Vulnerability assessment

Incident detection and response

Penetration testing



---

📚 Skills Demonstrated

John the Ripper Password Auditing Dictionary Attack Hash Analysis PDF Security Windows Cybersecurity Lab Vulnerability Assessment Ethical Hacking


---

Author

Olore Sulaimon Omobolaji 
