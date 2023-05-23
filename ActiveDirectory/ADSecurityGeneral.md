# General AD Security References
This is primarily an exercise for me to organize links and info, but doing it publically as it may be of use to others.  This is a continual work in progress (hopefully).

## Microsoft Official Guidance:
- Best Practices for Securing Active Directory:  https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory
- Securing Domain Controllers Against Attack: https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/securing-domain-controllers-against-attack
- Monitoring Active Directory for Signs of Compromise: https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/monitoring-active-directory-for-signs-of-compromise
- Implementing Least-Privilege Administrative Models: https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/implementing-least-privilege-administrative-models
- Stopping Active Directory Attacks & Other Post-Exploition Behavior with AMSI & Machine Learning: https://www.microsoft.com/security/blog/2020/08/27/stopping-active-directory-attacks-and-other-post-exploitation-behavior-with-amsi-and-machine-learning/
- Backing Up and Restoring an Active Directory Server: https://docs.microsoft.com/en-us/windows/win32/ad/backing-up-and-restoring-an-active-directory-server
- Active Directory Domain Services Docs: https://docs.microsoft.com/en-us/windows/win32/ad/active-directory-domain-services


## ADSecurity.org 
- Securing Domain Controllers to Improve Active Directory Security: https://adsecurity.org/?p=3377
- Beyond Domain Admins - Domain Controller & AD Administration: https://adsecurity.org/?p=3700
- Mimikatz DCsync Usage, Exploitation, and Detection: https://adsecurity.org/?p=1729
- NTDS.dit: https://adsecurity.org/?p=451
- Attack Methods for Gaining Domain Admin Rights in AD: https://adsecurity.org/?p=2362
- Beyond Domain Admins - Domain Controller & AD Administration: https://adsecurity.org/?p=3700
- Detecting Forged Kerberos Ticket (Golden & Silver) use in AD: https://adsecurity.org/?p=1515
- Service Accounts: https://adsecurity.org/?p=4115

## Trimarc Security
- Ten Ways to Improve AD Security Quickly (Plus my Whitepaper): https://www.hub.trimarcsecurity.com/post/ten-ways-to-improve-ad-security-quickly
- Implementing Controls in Active Directory: Protecting Against Privileged Credential Sprawl : https://www.hub.trimarcsecurity.com/post/implementing-controls-in-active-directory-protecting-against-privileged-credential-sprawl
- Honeypot Accounts: https://www.hub.trimarcsecurity.com/post/the-art-of-the-honeypot-account-making-the-unusual-look-normal

## Pwndefend
- Rapid AD Hardening Checklist: https://www.pwndefend.com/2022/02/26/rapid-active-directory-hardening-checklist/
- Post Compromise AD Checklist: https://www.pwndefend.com/2021/09/15/post-compromise-active-directory-checklist/

## SpecterOps
- Manual AD Querying with dsquery and LDAPsearch: https://posts.specterops.io/an-introduction-to-manual-active-directory-querying-with-dsquery-and-ldapsearch-84943c13d7eb
- The Attack Path Management Manifesto: https://posts.specterops.io/the-attack-path-management-manifesto-3a3b117f5e5
- Death from Above: Lateral Movement from Azure to On-Prem AD: https://posts.specterops.io/death-from-above-lateral-movement-from-azure-to-on-prem-ad-d18cb3959d4d

# Specific AD Attacks & Techniques

## NTLM Relaying
- NTLM Hacker Recipes: https://www.thehacker.recipes/ad/movement/ntlm
- Mitigating NTLM Relay Attacks on ADCS: https://support.microsoft.com/en-us/topic/kb5005413-mitigating-ntlm-relay-attacks-on-active-directory-certificate-services-ad-cs-3612b773-4043-4aa9-b23d-b87910cd3429
- Exploiting CVE-2019-1040 - Combining relay vulnerabilities for RCE and Domain Admin: https://dirkjanm.io/exploiting-CVE-2019-1040-relay-vulnerabilities-for-rce-and-domain-admin/

## Pass-the-Hash

- Performing Pass-the-Hash Attacks with Mimikatz: https://blog.netwrix.com/2021/11/30/passing-the-hash-with-mimikatz/

## Golden Tickets

- Golden Ticket Attack Tutorial by Stealthbit: https://attack.stealthbits.com/how-golden-ticket-attack-works
- Golden Ticket by Pentestlab: https://pentestlab.blog/2018/04/09/golden-ticket/
- Detecting Forged Kerberos Ticket (Golden & Silver) use in AD: https://adsecurity.org/?p=1515
- TODO: Change the password for the krbtgt account on a regular schedule: https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn745899(v=ws.11)?redirectedfrom=MSDN#krbtgt-account-maintenance-considerations

## Kerberoasting

- Kerberoasting without Mimikatz by harmj0y: https://www.harmj0y.net/blog/powershell/kerberoasting-without-mimikatz/
- Kerberoasting Attack Tutorial by Stealthbit: https://attack.stealthbits.com/cracking-kerberos-tgs-tickets-using-kerberoasting
- Tim Medin - Tickets encrypted with AES keys are succeptible to Kerberoasting, twitter thread: https://twitter.com/TimMedin/status/1501232474763894784?s=20&t=c9uASmYc0eDJNrHYTz_iOg
- Detecting Kerberoasting by Trimarc: https://www.hub.trimarcsecurity.com/post/trimarc-research-detecting-kerberoasting-activity
- Kerberoast by skelsec

## DCSync

- What is DCSync by Stealthbit: https://stealthbits.com/blog/what-is-dcsync-an-introduction/
- Mimikatz DCsync Usage, Exploitation, and Detection: https://adsecurity.org/?p=1729
- MS-DRSR: https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-drsr/f977faaa-673e-4f66-b9bf-48c640241d47

## AD DS Database Theft (NTDS.dit)

- Extracting Password Hashes from NTDS.dit: https://blog.netwrix.com/2021/11/30/extracting-password-hashes-from-the-ntds-dit-file/
- NTDS.dit: https://adsecurity.org/?p=451
- 
## DCShadow

- DCShadow explained: by Luc Delsalle of Aslid.eu: https://blog.alsid.eu/dcshadow-explained-4510f52fc19d
- DCShadow Attack: https://www.dcshadow.com/
- UncoverDCShadow: A PowerShell utility to dynamically uncover a DCShadow attack: https://github.com/AlsidOfficial/UncoverDCShadow/

## Zerologon

- Zerologon is now detected by Microsoft Defender for Identity: https://www.microsoft.com/security/blog/2020/11/30/zerologon-is-now-detected-by-microsoft-defender-for-identity/

## PetitPotam

- From Stranger to DA: https://blog.truesec.com/2021/08/05/from-stranger-to-da-using-petitpotam-to-ntlm-relay-to-active-directory/
### RPC Filters
- A Definitive Guide to the RPC Filter: https://www.akamai.com/blog/security/guide-rpc-filter
- https://www.bleepingcomputer.com/news/microsoft/windows-petitpotam-attacks-can-be-blocked-using-new-method/
- MS-EFSR Standards Assignments: https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-efsr/1baaad2f-7a84-4238-b113-f32827a39cd2
- How to secure a Windows RPC Server and how not to: https://www.tiraniddo.dev/2021/08/how-to-secure-windows-rpc-server-and.html?m=1

## Kerberos Bronze Bit Attack
- NetSPI: Kerberos Bronze Bit Overview: https://blog.netspi.com/cve-2020-17049-kerberos-bronze-bit-overview/
- NetSPI: Bronze Bit Attack: https://blog.netspi.com/cve-2020-17049-kerberos-bronze-bit-attack/
- NetSPI: Kerberos Theory: https://blog.netspi.com/cve-2020-17049-kerberos-bronze-bit-theory
- Trimarc Kerberos Bronze Bit Attack: https://www.hub.trimarcsecurity.com/post/leveraging-the-kerberos-bronze-bit-attack-cve-2020-17049-scenarios-to-compromise-active-directory

## HiveNightmare/SeriousSAM
- BHIS Admin's Nightmare: https://www.blackhillsinfosec.com/admins-nightmare-combining-hivenightmare-serioussam-and-ad-cs-attack-paths-for-profit/

## Constrained Delegation Abuse

- Wagging the Dog: Abusing Resource-Based Constrianed Delegation to Attack AD: https://shenaniganslabs.io/2019/01/28/Wagging-the-Dog.html
- Revisiting Delegate 2 Thyself: https://exploit.ph/revisiting-delegate-2-thyself.html
- Abusing KDC without Protocol Transition: https://snovvcrash.rocks/2022/03/06/abusing-kcd-without-protocol-transition.html

## Kerberos Relaying

- Relaying Kerberos over DNS using krbrelayx and mitm6: https://dirkjanm.io/relaying-kerberos-over-dns-with-krbrelayx-and-mitm6/

## Credential Protection
### LSASS RunAsPPL
- Do you really know about LSA Protection?: https://itm4n.github.io/lsass-runasppl
- Bypassing LSA Protection in Userland: https://blog.scrt.ch/2021/04/22/bypassing-lsa-protection-in-userland/

### CredentialGuard

### ASR Rules

## Misconfigurations & Attack Paths
Many of the most pervasive issues around the security of Active Directory are misconfigurations in the environment.  These misconfigurations come about in many ways, but some examples are technical debt from long running AD domains (or worse, an AD domain that was originally created as part of a Microsoft Small Business Server 2000/2003), lack of knowledge, poor official documentation, and many SysAdmins and 3rd party vendors just trying to make a thing work.

Misconfigurations can be anything from poor AD group hygeine such as too many users or nested groups in Domain Admins or other priviledged groups to improperly configured delegation and DACLs and more.

Even though Active Directory has been around for about 20 years, there's still ongoing research on AD misconfigurations, attack paths, and vulnerabilities (some of which won't or can't be fixed).

### DACL Misconfigurations
- DACL Trouble: GenericAll on OUs: https://www.adamcouch.co.uk/dacl-trouble-genericall-on-ous/

### DCOM
- Non-administrative DCOM Execution: https://simondotsh.com/infosec/2021/12/29/dcom-without-admin.html
- Lateral Movement via DCOM: Round 2: https://enigma0x3.net/2017/01/23/lateral-movement-via-dcom-round-2/

### Tools for discoverying AD Misconfigurations & Attack Paths

#### Microsoft Defender for Identity

- MDI Documentation: https://docs.microsoft.com/en-us/defender-for-identity/
- IdentityLogonEvents AdvancedHunting table: https://docs.microsoft.com/en-us/microsoft-365/security/defender/advanced-hunting-identitylogonevents-table?view=o365-worldwide

#### Pingcastle

Pingcastle is a simple way to quickly gather and view information on many common AD misconfiguration issues.  It also exposes some basic attack path information.  Provides solid advice on how to remediate any discovered issues.  A pretty solid way to get started on AD security.
https://www.pingcastle.com/

#### Adalanche
https://github.com/lkarlslund/adalanche

#### Trimarc ADChecks

- Securing Active Directory: Performing AD Security Review: https://www.hub.trimarcsecurity.com/post/securing-active-directory-performing-an-active-directory-security-review

#### Bloodhound

- Expanding Bloodhound with Plaintext Field to Compromised Accounts (CrackHound): https://www.trustedsec.com/blog/expanding-the-hound-introducing-plaintext-field-to-compromised-accounts/
- Bloodhound Cypher Cheatsheet: https://hausec.com/2019/09/09/bloodhound-cypher-cheatsheet/
- Detecting LDAP enumeration and Sharphound collector using AD Decoys: https://medium.com/securonix-tech-blog/detecting-ldap-enumeration-and-bloodhound-s-sharphound-collector-using-active-directory-decoys-dfc840f2f644
- Fixing Common AD Security Issues with Bloodhound: https://dzone.com/articles/how-to-fix-the-three-most-common-ad-security-issue
- AD Explorer, bloodhound, and AD Attack Paths: https://infosecjournal.com/issues/infosec-journal-issue-1-943327
- Attack Mapping with Bloodhound: https://stealthbits.com/blog/local-admin-mapping-bloodhound/

#### Purple Knight

https://www.purple-knight.com/

#### AD Explorer
- TrustedSec AD Explorer on Engagements: https://www.trustedsec.com/blog/adexplorer-on-engagements/
- BHIS - Domain Goodness - How I learned to love AD Explorer: https://www.blackhillsinfosec.com/domain-goodness-learned-love-ad-explorer/

#### jackdaw
https://github.com/skelsec/jackdaw

#### PowerShell
- Performing AD Reconnaissance with PowerShell: https://stealthbits.com/blog/performing-domain-reconnaissance-using-powershell/

### Github AD Resources, Tweets, & Other References

- AD-Attack-Defense by infosecn1nja: https://github.com/infosecn1nja/AD-Attack-Defense
- ADInspect by Soteria: https://github.com/soteria-security/ADInspect
- AD Sentinel KQL Rules by Kaidja: https://github.com/Kaidja/Azure-Sentinel/tree/main/Analytics%20Rules/Active%20Directory
- AD Exploitation Cheat Sheet: https://casvancooten.com/posts/2020/11/windows-active-directory-exploitation-cheat-sheet-and-command-reference/
- Practical Compromise Recovery Guidance for AD: https://m365internals.com/2021/04/27/practical-compromise-recovery-guidance-for-active-directory/
- Securing AD Service Accounts: https://forestall.io/blog/tr/activedirectory/active-directory-servis-hesaplarinin-guvenligi/
- 18 Ways to Detect Malicious Actions in Your AD Logs using SIEM: https://blueteamblog.com/18-ways-to-detect-malcious-actions-in-your-active-directory-logs-using-siem
- Attacking AD: https://zer1t0.gitlab.io/posts/attacking_ad/
- 7 Common AD Misconfigurations that Adversaries Abuse: https://www.crowdstrike.com/blog/seven-common-microsoft-ad-misconfigurations-that-adversaries-abuse/
- Offensive WMI: https://0xinfection.github.io/posts/wmi-ad-enum/
- 5 Simple AD Improvements by wald0: https://twitter.com/_wald0/status/1477067833712381953?t=jz-hwkQWKVmTuLdtTC9RDA&s=19
- Kerberoast-Detection by Blumira: https://github.com/Blumira/Kerberoast-Detection

### AD Hardening Guides:
-  White Oak Security AD Hardening Guide: https://www.whiteoaksecurity.com/blog/active-directory-security/
-  Trimarc Security - Protecting Against Privileged Crednetial Sprawl: https://www.hub.trimarcsecurity.com/post/implementing-controls-in-active-directory-protecting-against-privileged-credential-sprawl
-  Hardening Outbound NTLM on AD DCs: https://www-cert-ssi-gouv-fr.translate.goog/dur/CERTFR-2021-DUR-001/?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en-US
- AD Hardening by NathanMcNulty: https://twitter.com/NathanMcNulty/status/1282370323233402880?t=PtLDNrH8nbSjkliTJA67bA&s=19

### Videos, Conferences, and Talks
- Hacking Common AD Misconfigurations: https://www.youtube.com/watch?v=U5q2_i8bNb4
- Trimarc Presentations: https://www.hub.trimarcsecurity.com/presentations
- Sean Metcalf @ Derbycon - Red vs Blue Active Directory Attack & Defense: https://adsecurity.org/?p=1738
- SiegeCast: In Defense of Defense in Depth: https://www.youtube.com/watch?v=H6L-nVs1YWg

### Active Deception, Canaries, etc
- Digital Canaries in Coal Mines: Detecting Adversarial Enumeration: https://medium.com/@rvrsh3ll/digital-canaries-in-coal-mines-detecting-adversarial-enumeration-with-dns-and-ad-aff70c60fc8
- Microsoft Defender for Identity honeytoken accounts: https://docs.microsoft.com/en-us/defender-for-identity/manage-sensitive-honeytoken-accounts
- Detecting LDAP enumeration and Bloodhound‘s Sharphound collector using AD Decoys: https://medium.com/securonix-tech-blog/detecting-ldap-enumeration-and-bloodhound-s-sharphound-collector-using-active-directory-decoys-dfc840f2f644
- Honeypot Accounts: https://www.hub.trimarcsecurity.com/post/the-art-of-the-honeypot-account-making-the-unusual-look-normal
- Sean Metcalf: Quickest way to identify recon tools (like Bloodhound) is to set up SACLs (audit entries) on AD objects that are typically hit - Domain Admins, Domain Controller computer objects, etc.
