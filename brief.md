Version: NAFATH-V4
Track: Software

## Overview
Protecting an organization's systems requires security across several connected technology areas. Software security helps protect applications from vulnerabilities and unauthorized access. Artificial intelligence security focuses on protecting AI systems from attacks and ensuring their reliability. Mobile security protects applications and user information on smartphones and tablets. Networking security helps prevent attacks that could interrupt communication or redirect internet traffic. Cybersecurity identifies security risks and helps organizations respond to threats and vulnerabilities. Data security focuses on protecting sensitive information and understanding the software components used in systems.

These six areas work together to strengthen an organization's overall security. A weakness in one area can affect other parts of the system. Therefore, organizations need to understand and manage security risks across all six areas.
## Software
According to the Twelve-Factor App methodology, application configuration and secrets, such as database passwords and API keys, should be stored in environment variables instead of directly in the source code. This separation protects sensitive credentials from being exposed when code is shared or published. Environment variables also allow developers to change configuration between development, testing, and production without modifying the code, making applications easier to manage.

Resource: The Twelve-Factor App - III. Config - https://12factor.net/config
## AI
Machine learning systems can face several adversarial attacks, including evasion, poisoning, and privacy attacks. Evasion attacks manipulate inputs after a model has been trained to produce incorrect predictions. Poisoning attacks introduce malicious data or changes during training to influence the model's behavior. Privacy attacks attempt to extract sensitive information from models or their training data. The main differences involve when the attack occurs and what the attacker wants to achieve.

Resource: NIST - Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://doi.org/10.6028/NIST.AI.100-2e2025
## Mobile
The OWASP Mobile Application Security Verification Standard (MASVS) is a security standard that provides requirements for protecting mobile applications. It covers important areas such as secure data storage, cryptography, authentication, network communication, and code quality. Developers and security testers use MASVS to assess whether a mobile app meets these requirements. It helps identify security weaknesses, guide testing activities, and improve the protection of applications and user information.

Resource: OWASP - Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/
## Networking
BGP route hijacking occurs when a network announces IP routes it is not authorized to originate, potentially redirecting internet traffic through the wrong network. Resource Public Key Infrastructure (RPKI) helps prevent this by using Route Origin Authorizations (ROAs) to verify which networks may announce specific IP prefixes. Network operators can reject invalid announcements. However, RPKI origin validation does not verify the entire network path, so some routing attacks remain possible.

Resource: RIPE NCC - BGP Origin Validation - https://www.ripe.net/manage-ips-and-asns/resource-management/rpki/bgp-origin-validation/
## Cybersecurity
Log4Shell (CVE-2021-44228) was a critical security vulnerability in Apache Log4j 2, a Java logging library. Attackers could exploit its JNDI lookup feature through malicious log messages, potentially executing unauthorized code on vulnerable servers. It was especially dangerous because Log4j was widely used and the attack could be triggered remotely. Apache initially released version 2.15.0, then provided stronger fixes in later versions by disabling or removing unsafe lookup behavior.

Resource: Apache Logging Services - Security - https://logging.apache.org/security.html

## Data
A Software Bill of Materials (SBOM) is a structured inventory of the components and dependencies used in a software application. It helps organizations identify vulnerable libraries and manage software supply chain risks. An SBOM should include essential information such as component names, versions, producers, unique identifiers, dependency relationships, the SBOM author, and a timestamp. This information makes it easier to track software components and respond when security vulnerabilities are discovered.

Resource: CISA - Minimum Elements for a Software Bill of Materials (SBOM) - https://www.cisa.gov/sites/default/files/2025-08/2025_CISA_SBOM_Minimum_Elements.pdf

## Misconception in My Track
A common misconception in software development is that storing passwords and API keys directly in source code is safe as long as the repository is private. However, private repositories can still be exposed through accidental sharing or unauthorized access. The Twelve-Factor App methodology recommends separating configuration from code and storing it in environment variables. This reduces the risk of exposing credentials when code is shared and makes configuration easier to manage across different deployments. The section "III. Config — Store config in the environment" explains why configuration should remain separate from source code.
## Open Question
How can large software development teams securely manage and rotate API keys and database passwords across multiple applications without exposing sensitive information?
