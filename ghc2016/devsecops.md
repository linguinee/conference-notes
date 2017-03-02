# Rugged Software and the DevSecOps Security Journey

Shannon Lietz, DevSecOps Leader  
Myoki Spencer, Staff Software Engineer

* [DevSecOps](#devsecops)
  * [Benefits of DevOps + Security](#benefits-of-devops--security)
  * [Get Involved](#get-involved)
* [Evaluate Attacks for a Basic Application](#evaluate-attacks-for-a-basic-application)
  * [Most Common Attacks](#most-common-attacks)
* [Hands-On Attack Map Exercise](#hands-on-attack-map-exercise)

SEI estimates that 90% of reported security incidents result from exploits against defects in the design or code of software…

## DevSecOps

The practice of developing safer software sooner by involving all needed parties in the creative process and practicing continuous improvement from high fidelity actionable feedback with context.

* A mindset and holistic approach
* A collection of processes and tools
* A means of building security and compliance into software
* A community driven effort
* A strategy driven by learning and experiments

NOT

* A one-size-fits-all approach
* A single tool or method
* Just a means of adding security into continuous delivery
* Invented by vendors
* A strategy driven by perfection and compliance

### Benefits of DevOps + Security

* Higher engagement; all of us vs. the attackers
* Greater attack resiliency; reduced impact
* Less waste; better hygiene
* Customer focus; increased trust
* Increased context; better decision quality
* Faster time to market; faster learning
* Security built-into SDLC; less refactoring

### Get Involved

* devsecops.org
* @devsecops on Twitter
* DevSecOps on LinkedIn and Github
* ruggedsoftware.org

## Evaluate Attacks for a Basic Application

* White Hat: "Ethical Hackers"
* Black Hat: Unethical/Illegal Hackers
* Red Team: Attackers
* Blue Team: Defenders

### Most Common Attacks

* Cross Site Scripting (XSS)
  * Injecting JS into a form and making it part of the application
* SQL Injection
  * Little Bobby Tables
* Command Injection
* Insecure Direct Object References
  * e.g. gymnasticsgym.com/parent/results?id=34300
  * Changing the id means being able to view other kids' data
* Security Misconfiguration
  * e.g. using a default password, forgetting to turn off the admin panel
  * Easily picked up by scanners
* Sensitive Data Exposure
  * Not encrypting things like passwords and credit card information
* Missing Function Level Access Control
* Cross Site Request Forgery (SCRF)
  * Using a previous login session
* Using Components with Known Vulnerabilities

## Hands-On Attack Map Exercise

RailsGoat is a vulnerable version of the Ruby on Rails Framework both versions 3 and 4. It includes vulnerabilities from the OWASP Top 10, as well as some "extras" that the initial project contributors felt worthwhile to share. This project is designed to educate both developers, as well as security professionals.

* [RailsGoat Wiki](https://github.com/OWASP/railsgoat/wiki)
* [RailsGoat](https://insecurerails.herokuapp.com/login)
