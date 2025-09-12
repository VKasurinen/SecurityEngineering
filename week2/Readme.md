# Task 1A: Browsers and Banking Security

## Questions & Answers

### 1. What does the "Not Secure" warning mean in the first picture and what risks does visiting sites with the warning pose?
- The **"Not Secure"** warning indicates that the website is not using HTTPS (HyperText Transfer Protocol Secure).  
- Risks include:
  - Data sent (like usernames, passwords, or financial info) can be intercepted (man-in-the-middle attack).
  - Attackers may modify content between the site and the user.
  - Lack of encryption makes it easier to impersonate or spoof the site.

---

  ### 2. Why does the second site show up as "trusted" to the browser?
- The second site has a **valid TLS/SSL certificate** issued by a recognized Certificate Authority (CA).  
- This means:
  - Communication is encrypted end-to-end.
  - The domain ownership has been verified at least at a basic level.
  - Browsers mark the connection as secure and display a lock icon.

---

### 3. What other ways are there to detect a phishing/scam site?
- Check for domain spelling and possible variations (e.g., typosquatting).
- Inspect the SSL certificate details for suspicious or recently registered certificates.
- Look at website design inconsistencies (branding, grammar, unusual requests).
- Check the URL structure (extra subdomains, strange paths).

---

### 4. Are there any tools available online?
- [Google Safe Browsing Transparency Report](https://transparencyreport.google.com/safe-browsing/search)  
- [VirusTotal](https://www.virustotal.com) – scans URLs for phishing/malware.  
- [PhishTank](https://phishtank.org) – community-driven database of phishing websites.  
- [SSL Labs](https://www.ssllabs.com/ssltest/) – analyzes SSL/TLS configuration.  

---

### 5. What is typosquatting and how does it relate to the pictures?
- Typosquatting is registering domains that are similar to legitimate ones (e.g., `danskebankk.fi` instead of `danskebank.fi`) to trick users.  
- In the context of the pictures:
  - Attackers may exploit minor differences in spelling to make fake banking sites appear authentic.
  - Users might not notice the small change, especially if the site has HTTPS and a padlock.

---

### 6. What is UDRP and how does it help with combatting typosquatting?
- UDRP (Uniform Domain-Name Dispute-Resolution Policy) is a process established by ICANN for resolving disputes over domain names.  
- It allows legitimate domain owners to:
  - File complaints against typosquatted domains.
  - Reclaim or disable maliciously registered domains.
  - Reduce the number of scam domains targeting users.

---

### 7. If you were to own the domain `ouspg.org` and would be running your crypto banking application at `bank.ouspg.org`, what domains could you monitor for warning signs of possible phishing attempts against your customers?
You could monitor domains that:
- Contain **misspellings or variations**:  
  - `ousg.org`, `ouspg.com`, `ouspg.net`,
- Use **common substitutions**:  
  - `0uspg.org` (zero instead of "o"), `ouspq.org` (q instead of g)


# Task 2: Cards and Payments

## Questions: Payments

### 1. Why do modern payment cards use a chip and not a magnetic stripe?
- Magnetic stripe cards store static data, which can easily be copied or cloned (skimming).  
- Chip cards (EMV) generate a unique cryptographic code for each transaction, making replay or cloning significantly harder.  
- Chips also support stronger authentication methods and comply with international security standards.

---

### 2. What are EMV Certificates and why are they relevant for payment protection?
- EMV certificates are digital certificates used in EMV Mastercard and Visa transactions.  
- They authenticate the card and the terminal, ensuring both are trusted entities.  
- Prevents the use of counterfeit cards.
- Protects against man-in-the-middle attacks by verifying cryptographic keys.

---

### 3. What attacks exist against payment cards?

#### a) Card-not-present (CNP):
- Used in online or phone transactions where the physical card isn’t required.  
- Common attacks:
  - Stolen card numbers used in e-commerce.
  - Phishing or malware to harvest credentials.
  - Credential stuffing attacks on online stores.

#### b) Contactless payment:
- Uses NFC (Near-Field Communication).  
- Possible attacks:
  - Relay attacks: extending the NFC range to trick terminals.  
  - Eavesdropping: capturing signals (though range is limited).  
  - Lost/stolen cards: small-value purchases without PIN.  
- Protections include transaction limits and cryptographic randomization.

---

## Questions: MFA

### 4. How is multi-factor authentication (MFA) used in banking?
- MFA requires combining at least two factors:
  - PIN, password.
  - payment card, phone, token.
  - fingerprint, facial recognition.
- In banking:
  - Used for login, high-value transfers, and confirming new payees.
  - Often implemented as SMS codes, authenticator apps, or biometric verification.

---

### 5. How does multi-factor authentication increase payment security?
- Even if one factor is compromised (e.g., password), an attacker cannot complete a transaction without the second factor.  
- Reduces fraud in online and mobile banking.  
- Provides layered security against phishing, credential theft, and device compromise.

---

### 6. What MFA methods are you using in your daily life?
Examples:
- Email/Cloud accounts: authenticator app with biometric login.  
- Work systems: authenticator app with biometric login.  

---

### 7. What attacks exist against different forms of 2FA?

#### a) Time-based-one-time-password (TOTP):
- Attacks:
  - Phishing: tricking users into entering the one-time code on a fake site.
  - Real-time relay attacks: attackers immediately reuse entered codes.

#### b) Text Message (SMS):
- Attacks:
  - SIM swapping: attackers hijack the victim’s phone number.
  - Phishing: convincing victims to reveal SMS codes.
- Considered weaker than authenticator apps or hardware keys.


# Task 3: Card Fraud

### What kinds of card fraud exist?

    There is Card-Not-Present fraud: Transactions where the physical card is not present (e.g., online stores, phone orders, or mail orders).

    Counterfeit cards: Information from the card’s magnetic stripe or chip is copied and transferred to a fake card.

    Lost or stolen cards: A legitimate card is used without authorization after it has been lost or stolen.

  - How does card fraud type prevalence differ geographically?
    Cross-border payments have a much higher fraud rate than domestic payments.


### How has the fraud landscape changed between 2008-2019? Why?
  The fraud landscape has changed significantly between 2008 and 2019. Instead of physical cards, it has shifted to CNP fraud. The number of physical card frauds decreased significantly with the gradual introduction of EMV chip technology and PIN codes, which made it more difficult to clone a card. At the same time, mobile applications and the internet and mobile devices in general have also developed, which created new platforms for fraud.

  - What type of fraud has seen a notable increase during the last decade?
    Card Not Present fraud emerged as the dominant type of fraud, increasing its share of total fraud from approximately 48% in 2010 to over 80% in 2019.

  - What technologies or regulations have had an impact on card fraud?
    Chip and PIN technology, which plummeted the number of counterfeit and lost/stolen card frauds at physical points.

### How has the transaction landscape changed in the same period?
The number and volume of payments grew exponentially, especially online, and also
physical cash withdrawals decreased, while card payments in stores, and especially online, increased.

  - What kind of transactions have become increasingly popular?

    Online payments have become very popular.
    Contactless payments in physical stores have become more common.

  - What kind of transactions have had a high risk of being fraudulent?
    - Has this changed at all during 2008-2019?

    Cross-border payments and all online payments and
    prior to 2010, the greatest risk was at ATMs and in stores, especially with counterfeit cards. In 2019, the overwhelming risk has shifted to online payments.


### What effect has internet and e-commerce had on card fraud?
  The internet and online shopping have enabled the huge growth of CNP scams, which offer fraudsters the ability to make payments worldwide without a physical card, using only stolen card information.

### why is preventing data breaches important in preventing card fraud?
 - How does payment card tokenisation help in this? -Anything interesting you found?

  Most CNP scams are committed using stolen card information. Data breaches are the primary way this information ends up in the hands of criminals. Preventing data breaches directly prevents access to the raw data that the scams require.

  ALso the tokenization is a very effective way to combat the damage caused by data breaches. If a merchant's system is compromised, the stolen tokens are useless to fraudsters because they cannot be used in any context other than that store or service. The original card number is not stored.





