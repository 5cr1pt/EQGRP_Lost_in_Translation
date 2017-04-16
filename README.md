# EQGRP Lost in Translation
Decrypted content of odd.tar.xz.gpg, swift.tar.xz.gpg and windows.tar.xz.gpg

Downloaded from https://yadi.sk/d/NJqzpqo_3GxZA4
Original post from the #ShadowBrokers https://steemit.com/shadowbrokers/@theshadowbrokers/lost-in-translation

- **windows**: contains Windows exploits, implants and payloads
- **swift**: contains operational notes from banking attacks
- **oddjob**: docs related to the ODDJOB backdoor

## sha256 hashes
### Original archives
- `7c19a67d728bc700d18d2ed389a80de495681b7097222d9b8f1d696f0986f9a2` odd.tar.xz.gpg
- `78b89b2c4b129400150c7b60a426ff469aaea31da1588d2abc4180feaa9c41d3` swift.tar.xz.gpg
- `c28d5c10ec78bc66d3868e4862c7f801ffd561e2116b529e0782bf78f3ef3255` windows.tar.xz.gpg


### Decrypted archives
- `85e03866ae7eaaedd9462054b62a10f2180983bdfd086b29631173ae4422f524` odd.tar.xz
- `df468f01e65f3f1bc18f844d7f7bac8f8eec3664a131e2fb67ae3a55f8523004` swift.tar.xz
- `5bb9ddfbcefb75d017a9e745b83729390617b16f4079356579ef00e5e6b5fbd0` windows.tar.xz

# Exploits

- **EARLYSHOVEL** RedHat 7.0 - 7.1 Sendmail 8.11.x exploit
- **EBBISLAND (EBBSHAVE)** root RCE via RPC XDR overflow in Solaris 6, 7, 8, 9 & 10 (possibly newer) both SPARC and x86.
- **ECHOWRECKER** remote Samba 3.0.x Linux exploit.
- **EASYBEE** appears to be an MDaemon email server vulnerability
- **EASYPI** is an IBM Lotus Notes exploit  that gets detected as Stuxnet
- **EWOKFRENZY** is an exploit for IBM Lotus Domino 6.5.4 & 7.0.2
- **EXPLODINGCAN** is an IIS 6.0 exploit that creates a remote backdoor
- **ETERNALROMANCE** is a SMB1 exploit over TCP port 445 which targets XP, 2003, Vista, 7, Windows 8, 2008, 2008 R2, and gives SYSTEM privileges (MS17-010)
- **EDUCATEDSCHOLAR** is a SMB exploit (MS09-050)
- **EMERALDTHREAD** is a SMB exploit for Windows XP and Server 2003 (MS10-061)
- **EMPHASISMINE** is a remote IMAP exploit for IBM Lotus Domino 6.6.4 to 8.5.2
- **ENGLISHMANSDENTIST** sets Outlook Exchange WebAccess rules to trigger executable code on the client's side to send an email to other users
- **EPICHERO** 0-day exploit (RCE) for Avaya Call Server
- **ERRATICGOPHER** is a SMBv1 exploit targeting Windows XP and Server 2003
- **ETERNALSYNERGY** is a SMBv3 remote code execution flaw  for Windows 8 and Server 2012 SP0 (MS17-010)
- **ETERNALBLUE is** a SMBv2 exploit for Windows 7 SP1 (MS17-010)
- **ETERNALCHAMPION** is a SMBv1 exploit
- **ESKIMOROLL** is a Kerberos exploit targeting 2000, 2003, 2008 and 2008 R2 domain controllers
- **ESTEEMAUDIT** is an RDP exploit and backdoor for Windows Server 2003
- **ECLIPSEDWING** is an RCE exploit for the Server service in Windows Server 2008 and later (MS08-067)
- **ETRE** is an exploit for IMail 8.10 to 8.22
- **FUZZBUNCH** is an exploit framework, similar to MetaSploit
- **ODDJOB** is an implant builder and C&C server that can deliver exploits for Windows 2000 and later, also not detected by any AV vendors


# Utilities

- **PASSFREELY** utility which "Bypasses authentication for Oracle servers"
- **SMBTOUCH** check if the target is vulnerable to samba exploits like ETERNALSYNERGY, ETERNALBLUE, ETERNALROMANCE
- **ERRATICGOPHERTOUCH**  Check if the target is running some RPC
- **IISTOUCH** check if the running IIS version is vulnerable
- **RPCOUTCH** get info about windows via RPC
- **DOPU** used to connect to machines exploited by ETERNALCHAMPIONS
