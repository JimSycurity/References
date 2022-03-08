# General AD Security References
This is primarily an exercise for me to organize links and info, but doing it publically as it may be of use to others.  This is a continual work in progress (hopefully).

## Microsoft Official Guidance:
- Best Practices for Securing Active Directory:  https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory
- Securing Domain Controllers Against Attack: https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/securing-domain-controllers-against-attack
- Monitoring Active Directory for Signs of Compromise: https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/monitoring-active-directory-for-signs-of-compromise
- Implementing Least-Privilege Administrative Models: https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/implementing-least-privilege-administrative-models
- Stopping Active Directory Attacks & Other Post-Exploition Behavior with AMSI & Machine Learning: https://www.microsoft.com/security/blog/2020/08/27/stopping-active-directory-attacks-and-other-post-exploitation-behavior-with-amsi-and-machine-learning/


## ADSecurity.org 
- Securing Domain Controllers to Improve Active Directory Security: https://adsecurity.org/?p=3377
- Beyond Domain Admins - Domain Controller & AD Administration: https://adsecurity.org/?p=3700
- Mimikatz DCsync Usage, Exploitation, and Detection: https://adsecurity.org/?p=1729
- NTDS.dit: https://adsecurity.org/?p=451
- Attack Methods for Gaining Domain Admin Rights in AD: https://adsecurity.org/?p=2362
- Beyond Domain Admins - Domain Controller & AD Administration: https://adsecurity.org/?p=3700
- Detecting Forged Kerberos Ticket (Golden & Silver) use in AD: https://adsecurity.org/?p=1515

## Pwndefend
- Rapid AD Hardening Checklist: https://www.pwndefend.com/2022/02/26/rapid-active-directory-hardening-checklist/
- Post Compromise AD Checklist: https://www.pwndefend.com/2021/09/15/post-compromise-active-directory-checklist/

# Specific AD Attacks & Techniques

## Golden Tickets

- Golden Ticket Attack Tutorial by Stealthbit: https://attack.stealthbits.com/how-golden-ticket-attack-works
- Golden Ticket by Pentestlab: https://pentestlab.blog/2018/04/09/golden-ticket/
- Detecting Forged Kerberos Ticket (Golden & Silver) use in AD: https://adsecurity.org/?p=1515

## Kerberoasting

- Kerberoasting without Mimikatz by harmj0y: https://www.harmj0y.net/blog/powershell/kerberoasting-without-mimikatz/
- Kerberoasting Attack Tutorial by Stealthbit: https://attack.stealthbits.com/cracking-kerberos-tgs-tickets-using-kerberoasting
- Tim Medin - Tickets encrypted with AES keys are succeptible to Kerberoasting, twitter thread: https://twitter.com/TimMedin/status/1501232474763894784?s=20&t=c9uASmYc0eDJNrHYTz_iOg

## DCSync

- What is DCSync by Stealthbit: https://stealthbits.com/blog/what-is-dcsync-an-introduction/
- Mimikatz DCsync Usage, Exploitation, and Detection: https://adsecurity.org/?p=1729

## AD DS Database Theft (NTDS.dit)

- NTDS.dit: https://adsecurity.org/?p=451
- 
## DCShadow

- DCShadow explained: by Luc Delsalle of Aslid.eu: https://blog.alsid.eu/dcshadow-explained-4510f52fc19d
- DCShadow Attack: https://www.dcshadow.com/

## Zerologon

- Zerologon is now detected by Microsoft Defender for Identity: https://www.microsoft.com/security/blog/2020/11/30/zerologon-is-now-detected-by-microsoft-defender-for-identity/
- 
## Constrained Delegation Abuse

- Wagging the Dog: Abusing Resource-Based Constrianed Delegation to Attack AD: https://shenaniganslabs.io/2019/01/28/Wagging-the-Dog.html
- Revisiting Delegate 2 Thyself: https://exploit.ph/revisiting-delegate-2-thyself.html
- Abusing KDC without Protocol Transition: https://snovvcrash.rocks/2022/03/06/abusing-kcd-without-protocol-transition.html

## Misconfigurations & Attack Paths
Many of the most pervasive issues around the security of Active Directory are misconfigurations in the environment.  These misconfigurations come about in many ways, but some examples are technical debt from long running AD domains (or worse, an AD domain that was originally created as part of a Microsoft Small Business Server 2000/2003), lack of knowledge, poor official documentation, and many SysAdmins and 3rd party vendors just trying to make a thing work.

Misconfigurations can be anything from poor AD group hygeine such as too many users or nested groups in Domain Admins or other priviledged groups to improperly configured delegation and DACLs and more.

Even though Active Directory has been around for about 20 years, there's still ongoing research on AD misconfigurations, attack paths, and vulnerabilities (some of which won't or can't be fixed).


### DACL Misconfigurations
- DACL Trouble: GenericAll on OUs: https://www.adamcouch.co.uk/dacl-trouble-genericall-on-ous/

### Tools for discoverying AD Misconfigurations & Attack Paths

#### Microsoft Defender for Identity

#### Pingcastle

Pingcastle is a simple way to quickly gather and view information on many common AD misconfiguration issues.  It also exposes some basic attack path information.  Provides solid advice on how to remediate any discovered issues.  A pretty solid way to get started on AD security.
https://www.pingcastle.com/

#### Adalanche

#### Trimarc ADChecks

- Securing Active Directory: Performing AD Security Review: https://www.hub.trimarcsecurity.com/post/securing-active-directory-performing-an-active-directory-security-review


#### Bloodhound

- Expanding Bloodhound with Plaintext Field to Compromised Accounts (CrackHound): https://www.trustedsec.com/blog/expanding-the-hound-introducing-plaintext-field-to-compromised-accounts/
- Bloodhound Cypher Cheatsheet: https://hausec.com/2019/09/09/bloodhound-cypher-cheatsheet/

#### Purple Knight

https://www.purple-knight.com/

### Github AD Resources

- AD-Attack-Defense by infosecn1nja: https://github.com/infosecn1nja/AD-Attack-Defense
- ADInspect by Soteria: https://github.com/soteria-security/ADInspect
- AD Sentinel KQL Rules by Kaidja: https://github.com/Kaidja/Azure-Sentinel/tree/main/Analytics%20Rules/Active%20Directory

### AD Hardening Guides:
-  White Oak Security AD Hardening Guide: https://www.whiteoaksecurity.com/blog/active-directory-security/
-  Trimarc Security - Protecting Against Privileged Crednetial Sprawl: https://www.hub.trimarcsecurity.com/post/implementing-controls-in-active-directory-protecting-against-privileged-credential-sprawl
