# Google Summer of Code 2021 Final Report
![OWASP](https://user-images.githubusercontent.com/53997924/129850114-e9e3c295-259c-4eb6-b5af-dd445ff39fac.png)

* ### Student Developer: [Aman V. Singh](https://github.com/prince-7)
* ### Organisation - [OWASP Foundation](https://github.com/OWASP)
* ### Project -  [SecureTea-Project](https://github.com/OWASP/SecureTea-Project)
* ### Mentors - [Rejah Rahim](https://rejahrehim.com/) & [adeyosemanputra](https://github.com/adeyosemanputra)
* ### GSoC Project - [SecureTea - Improvement in Features](https://summerofcode.withgoogle.com/projects/#5509391828123648)

_________________________________________________________________________________________________________________________________

## About SecureTea Project
The OWASP SecureTea Project focuses on providing a one-stop security solution for various devices (personal computers / servers / IoT devices).

### The project has these features:
- [x] Intrusion Detection System
- [x] Firewall
- [x] AntiVirus
- [x] Server Log Monitor
- [x] System Log Monitor
- [x] Local Web Deface Detection & Prevention System
- [x] Auto Web Server Patcher
- [x] IoT Anonymity checker
- [x] Auto report generation using OSINT
- [x] Notifying suspicious activities using various mediums (Twitter, Telegram, Slack, Gmail, SMS, AWS & more)
- [x] Interactive GUI for ease of setting up
- [x] History Logger
- [x] GUI with authentication for Enterprise networks
- [x] Social Engineering
- [x] Eligibility traces based method for automatic blacklisting of ip addresses

_________________________________________________________________________________________________________________________________

### GSoC'21 Summary
#### Tasks Propsed in Proposal:-
* Add Web Application Firewall Feature
* Improve features (IDS, Firewall)
* Complete the web GUI and remote monitoring
* Zero bugs - Fix the currently identified bugs
* Improve Detecting Website Defacements Based on Machine Learning Techniques and Attack Signatures

#### Summary of my Work During GSoC'21:-
* #### [WhatsApp Integration](https://github.com/OWASP/SecureTea-Project/pull/275)
  * Added Whatsapp for remote monitoring and Notifications.
  * Whatsapp Integration using Twilio WhatsApp sandbox.
  * Wrote Unit Testing Modules for Whatsapp Integration.
  * [Documentation for usage of Module.](https://github.com/OWASP/SecureTea-Project/pull/279)

![image](https://user-images.githubusercontent.com/53997924/130048495-4e1f70e3-84e3-4b67-af78-f3c8d0308e09.png)
Video:
https://user-images.githubusercontent.com/53997924/130046965-04c5f504-21c3-431a-896f-92a52ddc799d.mp4

* #### [Improvement in Network Intrution Detection Feature](https://github.com/OWASP/SecureTea-Project/pull/284)
  * Add new R2L attack detection modules to IDS
  * Added DNS Amplification detection and test modules.
  * Added BGP Abuse detection and test modules.


* #### [Signature Based Defacement detector](https://github.com/OWASP/SecureTea-Project/pull/288)
  * The signature-based detection is fast and efficient for known attacks, and therefore it is used to improve the processing speed for common types of known defacement attacks.
  * The attack signatures are manually extracted from defaced web pages.We manually review the HTML code of each defaced web page to find patterns that commonly appear in defaced pages to construct the list of attack signatures. The attack signatures are stored and can be
updated when new defaced pages are detected.
![image](https://user-images.githubusercontent.com/53997924/130053424-4313e7f2-c9a5-46bc-9ad0-35f1e258a552.png)

* #### [Improve Detecting Website Defacements Based on Machine Learning Techniques](https://github.com/OWASP/SecureTea-Project/pull/295)
  * [Issue Link](https://github.com/OWASP/SecureTea-Project/issues/285) 
  *  This web defacement detection model will work for static as well as dynamic Webpages (The current version of the feature is only for static pages as it compares the hash changes). This model has 3 ways to detect defacement in consecutive order:-
     * Detection based on the change in the hash of external files(CSS, js, images, etc) used in the webpage.
     * Detection based on Attack signature(This data would accumulate from previous incidents of defacement).
     * Detection using machine learning(Using Random Forest Algorithm)


  * The steps to achieve this task were be:-
    * Collecting Attack Signatures from defacement incidents.
    * Building the dataset of defaced website and using the 2-gram method and then vectorized using the term frequency (TF) method.
    * Traning the model using defaced and non-deface datasets using Random Forest Algorithm.
    * Integrating the model with the project and other techniques.
    * [Wrtiting unit test modules](https://github.com/OWASP/SecureTea-Project/pull/304)
    * [Documentation](https://github.com/OWASP/SecureTea-Project/pull/306)

![image](https://user-images.githubusercontent.com/53997924/129408776-d4973fa7-0ff3-42fa-acb9-81d51aecc42c.png)

![image](https://user-images.githubusercontent.com/53997924/129408936-41f8dab4-22a3-4a00-ac73-d6fa1e79d706.png)

Video: https://user-images.githubusercontent.com/53997924/130015911-e656a59b-0f74-4f28-b4a5-6358f84585ac.mp4

* #### [Add Web Application Firewall Feature to the Web Interface(GUI)](https://github.com/OWASP/SecureTea-Project/pull/307)
  * WAF can be run from the GUI web interface from now.

![image](https://user-images.githubusercontent.com/53997924/129452529-74fc0c72-7ee6-4a94-b4e3-6077a9937ddc.png)

* #### Zero bugs - Fixed the identified bugs
  * [SweetAlert Node Module Error](https://github.com/OWASP/SecureTea-Project/issues/271)
    * [Fix For Sweetalert](https://github.com/OWASP/SecureTea-Project/pull/272)
  * [Fix for NetfilterQueue Issue](https://github.com/OWASP/SecureTea-Project/pull/274)
  * [Workflow Fix](https://github.com/OWASP/SecureTea-Project/pull/280)
  * [Fix for socketio error](https://github.com/OWASP/SecureTea-Project/pull/283)
  * [Bug Fix](https://github.com/OWASP/SecureTea-Project/pull/289)
  * [Repaired the broken WorkFlow](https://github.com/OWASP/SecureTea-Project/pull/291)
  * [Refactored Code](https://github.com/OWASP/SecureTea-Project/pull/292)
  * [Few Bug Fixes and Code Refactoring](https://github.com/OWASP/SecureTea-Project/pull/294)

_________________________________________________________________________________________________________________________________


### Timeline
|Title  |ID      | Type | Date(2021) |
| ----- | ------ | ---- | -----|
| **First Phase**              |
|SweetAlert Node Module Error |[#271](https://github.com/OWASP/SecureTea-Project/issues/271) | Issue | 20 May |
|Fix for NetfilterQueue Issue  |[#274](https://github.com/OWASP/SecureTea-Project/pull/274) | PR |21 May|
|Fix For Sweetalert  |[#272](https://github.com/OWASP/SecureTea-Project/pull/272) | PR | 28 May |
|Whatsapp Integration  |[#275](https://github.com/OWASP/SecureTea-Project/pull/275) | PR |28 May |
|Documentation for Whatsapp Integration  |[#279](https://github.com/OWASP/SecureTea-Project/pull/279) | PR | 30 May |
|Workflow Fix  |[#280](https://github.com/OWASP/SecureTea-Project/pull/280) | PR | 1 June |
|Fix for socketio error  |[#283](https://github.com/OWASP/SecureTea-Project/pull/283) | PR | 18 June |
|New Attack Detection Modules for IDS |[#284](https://github.com/OWASP/SecureTea-Project/pull/284) | PR | 18 June |
|New Feature: Improvement in Detecting Website Defacements Based on Machine Learning Techniques and Attack Signatures|[#285](https://github.com/OWASP/SecureTea-Project/issues/285) | Issue | 24 June | 
|Signature Based Defacement detector |[#288](https://github.com/OWASP/SecureTea-Project/pull/288) | PR | 6 July |
|Bug Fix |[#289](https://github.com/OWASP/SecureTea-Project/pull/289) | PR | 9 July |
|Repaired the broken WorkFlow |[#291](https://github.com/OWASP/SecureTea-Project/pull/291) | PR | 13 July |
| **Second Phase** |
|Refactored Code |[#292](https://github.com/OWASP/SecureTea-Project/pull/292) | PR | 23 July |
|Few Bug FIxes and Code Refactoring |[#294](https://github.com/OWASP/SecureTea-Project/pull/294) | PR | 31 July |
|New Feature: Improvement in Detecting Website Defacements Based on Machine Learning Techniques |[#295](https://github.com/OWASP/SecureTea-Project/pull/295) | PR | 4 Aug |
|Improvement in ML Deface Dataset and Fixed Unit Test |[#304](https://github.com/OWASP/SecureTea-Project/pull/304) | PR | 14 Aug |
|Documentation for IDS, Web Deface Module |[#306](https://github.com/OWASP/SecureTea-Project/pull/306) | PR | 14 Aug |
|GUI support Added for WAF |[#307](https://github.com/OWASP/SecureTea-Project/pull/307) | PR | 15 Aug |
|Update .travis.yml to fix the travis build |[#309](https://github.com/OWASP/SecureTea-Project/pull/309) | PR | 15 Aug |
|Optimizing ML model |[#310](https://github.com/OWASP/SecureTea-Project/pull/310) | PR | 15 Aug |
|New Gifs |[#315](https://github.com/OWASP/SecureTea-Project/pull/315) | PR | 19 Aug |
|Inserted Demo Videos in the Documentation |[#316](https://github.com/OWASP/SecureTea-Project/pull/316) | PR | 19 Aug |
|Update dev_guide.md |[#317](https://github.com/OWASP/SecureTea-Project/pull/317) | PR | 19 Aug |
|Fixing Travis Build |[#318](https://github.com/OWASP/SecureTea-Project/pull/318) | PR | 19 Aug |


* List of All PRs:- https://github.com/OWASP/SecureTea-Project/pulls?q=is%3Apr+author%3Aprince-7
* List of All Commits:- https://github.com/OWASP/SecureTea-Project/commits?author=prince-7

_________________________________________________________________________________________________________________________________

### Contribution graph and status
![image](https://user-images.githubusercontent.com/53997924/130078329-baa3b625-7b66-4b09-bba8-a3883c89a624.png)
