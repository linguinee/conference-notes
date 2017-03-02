# Accessibility vs. Security: Considerations for Online Content

Sam Dooly, Kylie Pentecost, Clare Rose, and Chelsea Seeley, Pearson

* [Regulations and Standards](#regulations-and-standards)
* [Security Considerations for People with Disabilities](#security-considerations-for-people-with-disabilities)
  * [Who benefits from accessible security measures?](#who-benefits-from-accessible-security-measures)
  * [How do disabled users respond to inaccessible security?](#how-do-disabled-users-respond-to-inaccessible-security)
  * [Considerations for mobile security](#considerations-for-mobile-security)
* [Accessible Security](#accessible-security)
  * [How can we make security accessible?](#how-can-we-make-security-accessible)
  * [What are the major challenges for an enterprise?](#what-are-the-major-challenges-for-an-enterprise)
* [Case Study: Integrating Assistive Technology in Secure High Stakes Assessments](#case-study-integrating-assistive-technology-in-secure-high-stakes-assessments)
  * [Pearson's TestNav Testing Platform](#pearsons-testnav-testing-platform)
    * [Security implications for integration of assistive technology](#security-implications-for-integration-of-assistive-technology)
  * [Security in Testing](#security-in-testing)
    * [Cheating prevention](#cheating-prevention)
    * [What else do we secure?](#what-else-do-we-secure)
    * [How do we secure the data?](#how-do-we-secure-the-data)
* [Build the Future](#build-the-future)

Sam Dooley, Software Development Manager, Online Accessible Math  
Kylie Pentecost, Product Manager, TestNav  
Clare Rose, Technical Project Manager, Shared Accessibility Services  
Chelsea Seeley, Director of Shared Accessibility Services

## Regulations and Standards

We need to meet not just accessibility standards, but security standards as well:

* FISMA
* Gramm-Leach-Bliley Act
* HIPAA

## Security Considerations for People with Disabilities

The security portal (where users authenticate) needs to be accessible – content is useful if people can't access it.

### Who benefits from accessible security measures?

* People with disabilities
* People with situational disabilities
* People who want increased productivity

### How do disabled users respond to inaccessible security?

* Lack of awareness of security risk
* Potential to use an inferior product because it's more accessible (virus protection, VPN software, etc.)
* Disable security features
* Provide access credentials to other users
* Inability to use the technology

### Considerations for mobile security

* Components of mobile accessibility and security
  * Device
  * Carrier
  * Operating system
  * Applications
* Business who support Bring Your Own Device (BYOD)

## Accessible Security

### How can we make security accessible?

* Flexible authentication – not one size fits all
* Explore biometrics as an option (reduces cognitive complexity)
* Dual modality (e.g. CAPTCHA with speech output alternative)
* Understand risks in third party assistive technologies
  * Is an external server used for content processing or storage?
  * Is data cached or stored in additional file structures on the device?

### What are the major challenges for an enterprise?

* Defining and communicating the policy
* Detection
* Enforcment
  * Data processing time
  * Blockers
* Rapidly changing standards – slow adoption
* Technical complexity (multipel configurations to understand, code for, and test)
* Accessibility solutions that were built before more stringent security guidelines were in place

## Case Study: Integrating Assistive Technology in Secure High Stakes Assessments

* Security
  * Security obligations to our clients
  * Security requirements to maintain testing constructs
  * Other security concerns
* Accessibiltiy
  * Legal obligations to provide equal access for all
  * Student use of assistive technology
  
### Pearson's TestNav Testing Platform

* App and browser-based testing platform
  * Moving away from browser towards exclusively app-based testing
* Growing alternative to paper-based testing
* Users are presented test questions in a secure testing environment

#### Security implications for integration of assistive technology

* What assistive technology do we allow?
  * Do we know which technologies are used?
  * Will the technologies maintain test security?
  * How do we determine which users should have access to the technology?
* How do we make sure it works and how do we communicate this information?
  * Internal testing
  * Vendor partnerships
  * Customer engagement

### Security in Testing

There are some necessary procedures to prevent cheating and ensure the security of the test content.

#### Cheating prevention

* Enforce date and time constraints
* One time use login credential
* Proctor unlocks credentials for use
* Disable clipboard
* ChromeOS: Kiosk Mode
* iOS: App Self Lock
* Prevent the use of other applications with the app
* Whitelist assistive technologies!

#### What else do we secure?

* Intellectual property
  * Protect the investment the customer made in content
  * Not easily replaceable
  * Prevent copying
  * Test content downloaded to client
* User responses and PII
  * Responses stored on client
  * Reduce testing time

#### How do we secure the data?

* Use https to provide basic security
* Encrypt the test content
* Encrypt the student response data
* Remove backup responses after upload to Pearson
* Remove cached test content when the app is closed

## Build the Future

* Cloud-based assistive technology whitelisting
* Designing to web standards that address security and accessibility
* More reliance on built-in operating system level features
