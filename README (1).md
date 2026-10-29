# PayGo Financial Technologies Ltd. — GDPR & SOC 2 Assessment

> Compliance assessment case study covering GDPR data protection obligations and SOC 2 Security and Availability controls.

## Overview

This repository documents an assessment of PayGo Financial Technologies Ltd., a Dublin-based fintech company providing digital payment services to individuals and small businesses in Ireland and other EU countries. The scenario describes approximately 120 employees and a cloud-based environment supported by third-party service providers.

**Assessment focus:** GDPR processing activities, data flows, compliance gaps, SOC 2 controls, supporting evidence, and remediation priorities.

**Source:** `PAYGO BUSINESS LIMITED.xlsx` (original assessment workbook).

## Contents

| Section | Description |
| --- | --- |
| [Scope](#scope) | Assessment scope and open questions |
| [GDPR Data Inventory](#gdpr-data-inventory) | Personal data processing activities |
| [Data Flows](#data-flows) | Movement, storage and deletion of data |
| [GDPR Gap Assessment](#gdpr-gap-assessment) | GDPR requirements, findings and actions |
| [SOC 2 Controls](#soc-2-controls) | Security and Availability control assessment |
| [SOC 2 Evidence Register](#soc-2-evidence-register) | Evidence requests and completion status |
| [Remediation plan](#remediation-plan) | Prioritized corrective actions and ownership |

## Key assessment themes

- Validate retention schedules, deletion testing, privacy notices and records of processing activities.
- Confirm third-party roles, processing locations and international data transfer arrangements.
- Document access reviews, role-based permissions and multi-factor authentication coverage.
- Establish evidence of timely security alert review and incident response exercises.
- Verify backup restoration testing and change approval records.

> **Note:** Findings and statuses below reflect the supplied case study, not an independently verified audit or certification.

## Detailed assessment

### Scope

#### Organisation / business context

PayGo Financial Technologies Ltd. is a fintech company headquartered in Dublin,Ireland, which provides a digital payment platform for individuals and small businesses across Ireland and other EU countries. The company has 120 employees and relies on cloud infrastructure and external providers for payment processing, identity verification, customer support, payroll and email communications.

#### GDPR assessment scope

The GDPR assessment covers seven personal data processing activities: Customer Registration, Identity Verification, Payment Processing, Customer Support, Employee Administration, Security Monitoring, and Card Payments.

#### Proposed SOC 2 scope

The proposed SOC 2 assessment will cover PayGo's digital payment platform, supporting cloud infrastructure, and relevant systems and services involved in payment processing, identity verification, access management, security monitoring, incident response, backup and recovery, and change management.; ; The assessment will focus on the Security and Availability Trust Services Criteria, including relevant controls operated by external service providers.

#### Systems identified in scenario

The system identified in this scnario includes;PayGo web and mobile applications,PayGo payment platform and database,; Customer support ticketing system,; Human Resources system,; Central logging platform,cloud hosting environment and identity verification system

#### Third-party providers

The third party providers provided in this case study are; Identity verification provider,External payment processor,customer support, payroll and email providers.cloud hosting

#### Scope limitations / unresolved questions

1. Third-Party Providers and International Data Transfers
- Confirm the processing and storage locations of all third-party providers.
- Determine whether personal data is transferred outside the EU/EEA and identify any applicable international data transfer arrangements.
- Confirm whether each third-party provider acts as a data controller, data processor, or joint controller for the relevant processing activities.
- When was each third-party provider's last security risk assessment conducted, and how frequently are these assessments performed?; ; 2. Access Management
- Have all system access permissions been reviewed and mapped to approved job roles?
- Has PayGo confirmed that employees have only the access necessary to perform their responsibilities?; ; 3. Multi-Factor Authentication (MFA)
- Why has MFA coverage across all in-scope systems not been documented?
- Has MFA been enabled across all in-scope systems?
- Who is responsible for managing, monitoring, and documenting MFA coverage?; ; 4. Backup and Recovery
- When was the last backup restoration test conducted?
- How frequently are backup restoration tests performed?
- Were backups successfully restored during testing?
- Are backup restoration test results documented and available for review?; ; 5. Incident Response
- Who is responsible for organizing and conducting incident response testing?
- Why have incident response procedures not been tested during the past 12 months?
- When is the next incident response exercise scheduled?; ; 6. Change Management
- Who is responsible for approving system changes before deployment?
- Are all system changes tested and approved before deployment?
- Are change approvals and testing results consistently documented?
- What measures are in place to ensure the change management process is followed?

### GDPR Data Inventory

| Processing Activity | Personal Data Categories | Data Subjects | Apparent Processing Time | System Used | External Receipent(If Identified) | Retention Period | Information not specified/to confirm |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Customer Registration | Fullname,Date of birth, email address, residential address,phone number | Customers registering for Paygo | Not Specified | PayGo web and mobile applications | — | While the account is active for five years after account closure. | Deletion procedures and evidence of deletion for customer registration data need to be confirmed. |
| Security Monitoring | User account identifier, login time, IP address,; authentication result, relevant system events | System users (Employees,Customer) | Not Specified | Central logging platform | — | 12 Months | Period access review evidence for the central logging platform is missing. |
| Identity Verification | Name,date of birth,address,identity document details,verfication results. | Customers undergoing identity verification. | Not Specified | — | Identity Verification provider | Five years after account closure | The identity verification provider's processing location, data protection role and applicable international transfer arrangements need confirmation. |
| Customer Support | Customer name, contact details, ticket description,; screenshots or attachments submitted by customers | Customers requesting support | Not Specified | Customer support ticketing system | — | Three years after ticket closure | Completed periodic access reviews for the customer support system are missing. Deletion procedures and evidence of deletion also need verification. |
| Payment Processing | Transaction reference, amount, currency, date, status,; payer and recipient account identifiers | Individual payers and recipients | Not Specified | PayGo payment platform and database | — | seven years | The justification for the seven-year transaction retention period needs confirmation, as the case study does not document the justification for every retention period. |
| Employee Administration | Employee name, contact details, job title, department,; payroll details | Employees | Not Specified | Human Resources system | — | Six years after employment ends. | Evidence of deletion of employee records after the retention period needs verification. |
| Card Payments | Payment token, card brand, last four digits of the card; number, transaction authorisation result | Individual Cardholders | Not Specified | — | External payment processor | Not Specified | The retention period for card-specific data is not separately specified. The external payment processor's deletion arrangements need confirmation. |

### Data Flows

| Processing Activity | Data Source | System or Recipient | Use/Movement described by scenario | Storage or retention information | Deletion practice or Evidence gap |
| --- | --- | --- | --- | --- | --- |
| Customer Registration | The customer registering for Paygo | PayGo web and mobile applications | Customer registration information is collected through PayGo's web and mobile applications. | While the account is active for five years after account closure. | Evidence that customer account information is deleted after the retention period needs confirmation. |
| Security Monitoring | System generated activity and authentication logs | Central logging platform | User login activities, authentication results and system events are recorded in the central logging platform. | 12 Months | Evidence that security logs are deleted after 12 months needs confirmation. |
| Identity Verification | Customer identity information and verification results;exact collection route not specified. | Identity verification provider | Customer identity information is processed by an external identity verification provider to verify identity. | Five years after account closure | Deletion practices and evidence of deletion by the external identity verification provider need confirmation. |
| Customer Support | The customer requesting support | Customer support ticketing system | Customer contact details, ticket descriptions and submitted attachments are processed through the customer support ticketing system. | Three years after ticket closure | Evidence that support tickets and attachments are deleted after the retention period needs confirmation. |
| Payment Processing | Transaction information generated through customer payment activities on paygo's payment platform. | PayGo payment platform and database | Transaction information is processed and recorded through PayGo's payment platform and database. | seven years | Evidence that transaction records are deleted after the seven-year retention period needs confirmation. |
| Employee Administration | Employee and HR administration records; exact collection menthod not specified. | Human Resources system | Employee personal and payroll information is processed through the Human Resources system. | Six years after employment ends. | Evidence that employee records are deleted six years after employment ends needs confirmation. |
| Card Payments | Not specified. | External payment processor | Card-related payment information is processed by an external payment processor for transaction authorisation. | Not Specified | Retention and deletion arrangements for card-specific data held by the external payment processor need confirmation. |

### GDPR Gap Assessment

| GDPR requirement / Article | What the requirement means for PayGo | Scenario evidence | Finding | Assessment status | Potential risk | Recommended action | Additional evidence needed |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Article 5(1)(e) | Storage limitation | PayGo has not documented the justification for every retention period | Justification for retention period not documented | Partially Compliant | Risk of data being kept longer than required. | There should be clear documentation of justification for every retention of data | Documentation explaining the legal or business justification for PayGo's retention periods. |
| Article 5(2) | Accountability | Insufficient evidence to demonstrate compliance | Incomplete vendor documentation. | Partially Compliant | Risk of data leakage | Provider records should be accurate and provide consistent identification of Data protection roles, Processing locations, Applicable international transfer arrangements, Recent security risk assessments and Documented risk assessments and ensure regular ongoing monitoring are completed for all providers. | Complete vendor records showing data protection roles, processing locations, international transfer arrangements and security risk assessments. |
| Article 13 | Information provided to data subjects | Privacy notice does not clearly identify every recipient category or explain applicable retention periods | Lack of transparency. | Non Compliant | Loss of customer trust | Customers have a right to transparency. All privacy noticed should be reviewed and clearly identify recipeient category and explain retention periods. | Deletion testing reports and records confirming that personal data is deleted when required. |
| Article 17 | Right to erasure | Deletion arrangements require verification | A weakness in verifying deletion practices. | Requires Verification | Risk of data being kept longer than required. | Verification for deletion of records should be implemented. A designated control owner within IT or information security to coordinate peridoic deletion testing scghedule and ensure external providers submit appropriate evidence of deletion. | PayGo's current privacy notice and evidence of what information is provided to customers. |
| Article 28 | Processor requirements | External provider arrangements require assessment | A weakness in provider arrangements | Partially Compliant | Risk of unidentified security weakness | An regular assessment of the external provider's arrangements should be implemented to spot security risks. | Data processing agreements and updated vendor records showing provider responsibilities and relevant data protection arrangements |
| Article 30 | Records of processing activities | Processing records are incomplete | Access permissions may not be adequately reviewed | Partially Compliant | Risk of being unable to demonstrate GDPR Complaince due to incomplete processing records. | Management should investigate the root cause of incomplete GDPR processing records and assign responsibility to a designated data protection or business process owner. A clear completion deadline should be established and periodic reviews should be conducted to ensure records remain accurate, complete and compliant with GDPR requirements.All reviews,approvals,and corrective actions should be documented for accountability and audit purposes. | Updated records of processing activities showing what personal data PayGo processes, why it processes it, and who receives it. |
| Article 32 | Security of processing | Missing access review evidence and security control assurance | Inadequate periodic review of access permissions | Partially Compliant | Risk of unauthorised access to or misuse of personal data due to inadequate access reviews. | A consistent access review should be coducted at intervals,such as quaterly with a documented review schedule and evidence should be documented.Management should monitor each completion, ensure inapppropriate access is promptly removed. | Completed access review reports and security alert monitoring records |

### SOC 2 Controls

| Control area | Relevant Trust Services Category / criterion | Policy or control described | Scenario evidence / limitation | Assessment (weakness or evidence gap) | Potential risk | Recommended action | Further evidence needed |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Access Management | Security — CC6.3 | The entity authorizes, modifies, or removes access to data, software, functions, and other protected; ; information assets based on roles, responsibilities, or the system design and changes, giving consid-; eration to the concepts of least privilege and segregation of duties, to meet the entity’s objectives. | Some system permissions have not been mapped to approved job roles. | Incomplete mapping of system permissions to approved job roles. | Unauthorised access to information | System access should be granted and reviewed according to approved job roles and responsibilities | Approved job roles and responsibilities, user access permissions reports, and access management policy |
| Access Management | Security — CC6.3 | The entity authorizes, modifies, or removes access to data, software, functions, and other protected; ; information assets based on roles, responsibilities, or the system design and changes, giving consid-; eration to the concepts of least privilege and segregation of duties, to meet the entity’s objectives. | Completed periodic access reviews are missing for the customer support system and central logging platform. | PayGo cannot provide sufficient records demonstrating that reviews were completed. | Risk of unauthorised access to sensitive information due to unverified access permissions | PayGo should conduct periodic reviews for the customer support system and central logging platform and document the results. | Documented access review reports showing who performed the reviews, when they were completed, which permissions were reviewed, and whether any issues were resolved. |
| Access Management. | Security — CC6.1 | The entity implements logical access security software, infrastructure, and architectures over protected information assets to protect them from security events to meet the entity's objectives. | Multi-factor authentication (MFA) coverage across all in-scope systems has not been documented. | PayGo cannot demonstrate MFA coverage across all in-scope systems due to incomplete documentation | Risk of unauthorised access, data theft and user impersonation if MFA is not enabled across all in-scope systems | PayGo should review MFA coverage across all in-scope systems and document results. | MFA coverage report showing which in-scope systems have MFA enabled, supported by system configuration records |
| Security Monitoring | Security — CC7.2 | The entity monitors system components and the operation of those components for anomalies that are indicative of malicious acts, natural disasters, and errors affecting the entity's ability to meet its objectives; anomalies are analyzed to determine whether they represent security events. | Security monitoring records do not establish that all critical alerts are reviewed within defined timeframes. | PayGo cannot demonstrate that critical security alerts are reviewed within defined timeframes. | Risk of delayed detection and response to security incidents, potentially leading to data breaches or increased security damage | Investigate gaps in security alert review records, assign responsibility for monitoring critical alerts, and ensure reviews are completed and documented within defined timeframes | SIEM alert logs showing alert timestamps, review timestamps, assigned reviewers and actions taken. |
| Incident Response | security -CC7.2 | Monitor systems for anomalies and indicators of compromise. | Security monitoring records do not establish that all; critical alerts are reviewed within defined timeframes. | Incident response procedures have not been tested in the past 12 months, so their effectiveness has not been demonstrated | PayGo may be unprepared to respond effectively to security threats, causing delays and greater damage. | Review and update incident response procedures, assign testing responsibilities, and conduct regular incident response exercises to assess their effectiveness | Incident response playbook, completed exercise reports, test results, and records of corrective actions |
| Backup and Recovery | Availability-A1.3 | Recovery plan procedures are tested.This means restore tests,DR exercises, and documented results. | PayGo cannot demonstrate that its backups have been successfully restored during testing | PayGo cannot demonstrate that backup restoration testing has been completed successfully due to missing test evidence | Risk of data loss and prolonged business disruption if backups cannot be successfully restored | Conduct regular backup restoration tests, document the results, and investigate and resolve any restoration failures. | Backup restoration test reports showing test dates, systems tested, results, and any corrective actions taken |
| Change Management | Security — CC8.1 | The entity authorizes, designs, develops or acquires, configures, documents, tests, approves, and; implements changes to infrastructure, data, software, and procedures to meet its objectives. | Change records do not consistently demonstrate; approval and testing before deployment. | Change records do not consistently provide evidence of approval and testing before deployment | Risk of system failures, security vulnerabilities and service disruptions due to changes that may not have been properly approved or tested before deployment. | Ensure all system changes are approved and tested before deployment, with documented evidence of approvals and test results | Change request records, documented approvals, test plans, completed test results and deployment records. |

### SOC 2 Evidence Register

| Control area | Evidence required | Status based on case study | Purpose of evidence | What remains to be confirmed |
| --- | --- | --- | --- | --- |
| Access Management | Approved job roles and user access permission reports. | Partially Complete | To confirm that system access permissions are appropriate for employees' approved job roles and responsibilities | Identify unmapped system permissions and confirm that they are assigned to the appropriate approved job roles. |
| Access Management | MFA coverage report showing which in-scope systems have MFA enabled, supported by system configuration records | Partially Complete | To confirm multi-factor authentication (MFA) coverage across all in-scope systems is documented. | Identify all in-scope systems and confirm that MFA is enabled and documented for each system |
| Access Management | Documented access review reports showing who performed the reviews, when they were completed, which permissions were reviewed, and whether any issues were resolved. | Missing | To confirm that Completed periodic access reviews are up to date for the; customer support system and central logging platform. | Confirm whether periodic access reviews were completed for the customer support system and central logging platform, and obtain records showing the review dates, reviewers and any corrective actions taken. |
| Security Monitoring | SIEM alert logs showing alert timestamps, review timestamps, assigned reviewers and actions taken. | Partially Complete | To confirm that security monitoring records demonstrate that all critical security alerts are reviewed within defined timeframes | Review SIEM alert logs to confirm that all critical alerts were reviewed within defined timeframes, including alert timestamps, review timestamps, assigned reviewers and actions taken. |
| Incidence response | Incident response playbook, completed exercise reports, test results, and records of corrective actions | Not Completed | To confirm whether incident response procedures have been tested during the past 12 months and whether the tests demonstrated their effectiveness | Review the incident response playbook, investigate why testing has not been conducted, and obtain completed exercise reports and test results to confirm the procedures are effective. |
| Backup and Recovery | Backup restoration test reports showing test dates, systems tested, results, and any corrective actions taken | Evidence Missing | To confirm that PayGo's backups can be successfully restored following a system failure or data loss | Determine whether backup restoration tests have been conducted, investigate why evidence is missing, and obtain documented test results. |
| Change Management | Change request records, documented approvals, test plans, completed test results and deployment records. | Partially Complete | To confirm that system changes were properly approved and tested before deployment | Review change request records, documented approvals, completed test results and deployment dates to confirm that system changes were approved and tested before deployment |

### Remediation plan

| Finding and scenario evidence | GDPR obligation and/or SOC 2 criterion | Assessment status | Potential risk / business impact | Corrective action | Priority (High/Medium/Low) | Proposed responsible role | Evidence required for completion |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Paygo has not documented the justification for its retention period. | Storage Limitation-Article 5(1)(e) | Partially Compliant | Personal data could be kept longer than necessary leading to GDPR non-compliance, Data breach and unauthorised access | Paygo should identity the retention periods, review personal data collected and include justifications for each retention period. | High priority due to the risk of non-compliance with GDPR's Storage Limitation principle. | Data Protection Officer | Documented data retention schedule showing retention periods and justifications for each category of personal data. |
| Paygo's deletion has not been tested across all systems and external providers | Right to Erasure-Article 17 | Partially Compliant | Personal data could be kept longer than necessary leading to GDPR non compliance | Paygo should identity all the systems where perosnal data are stored including that of its external provider, review personal data collected and test deletion of records across these systems as well as documenting it and resolving any errors from testing | High priority due to the risk of non-compliance with GDPR's right to erasure principle. | Data Protection Officer | Completed deletion test reports, test results and deletion logs covering PayGo's systems and external providers |
| Its privacy notice does not clearly identify every; category of recipient or explain all applicable retention; periods. | Information provided to data subjects - Article 13 | Partially Compliant | Loss of customer's trust and GDPR non-compliance due to lack of transparency | Review its privacy notice and include missing information which includes recipients or categories of recipients and retention period of data | High priority due to the risk of non-compliance with GDPR's information provided to data subjects principle. | Data Protection Officer | Updated Privacy notice |
| The Record of Processing Activities is incomplete | Records of processing activities-Article 30 | Partially Compliant | GDPR non-compliance, difficulty demonstrating compliance and poor visibility of where and how data is processed. | Identify all processing activities, review existing records, and update missing information where necessary | High priority due to the risk of non-compliance with GDPR's processing activities principle. | Data Protection Officer | Updated record of processing activities |
| Provider records do not consistently identify data protection roles, processing locations, Applicable international transfer arrangements,Recent security risk assessments and documented risk assessments and ongoing monitoring are incomplete for some providers. | Processor requirements-Sector 28 | Partially Compliant | Risk of unidentified security weakness | Identify all processing activities, review existing records, and update missing information where necessary | High priority due to the risk of non-compliance with GDPR's processor requirement principle. | Data Protection Officer | Updated provider records showing that gaps in Data protection roles,Processing locations,International transfer arrangements,Recent security risk assessments have been addressed. |
| Some system permissions have not been mapped to approved job roles | Security — CC6.3 | Partially Compliant | Unauthorised access to information | Review all system permissions and match against job roles to be certain each inidividual has access to the data they need. | High priority due to the risk of unauthorised access to sensitive information | IT Security Team | Completed job roles and responsibilities, user access permissions reports, and access management policy |
| Completed periodic access reviews are missing for the customer support system and central logging platform. | Security — CC6.3 | Partially Compliant | Risk of unauthorised access to sensitive information due to unverified access permissions | Review access reviews,complete any outstanding reviews for customer support system and central logging platform and document results. | High priority due to the risk of unauthorised access to sensitive information | IT Security Team | Documented access review reports showing who performed the reviews, when they were completed, which permissions were reviewed, and whether any issues were resolved. |
| Multi-factor authentication (MFA) coverage across all in-scope systems has not been documented. | Security — CC6.1 | Not documented | Risk of unauthorised access, data theft and user impersonation if MFA is not enabled across all in-scope systems | Review MFA coverage, address any gaps identified, and document the results. | High priority due to the risk of unauthorised access to sensitive information | IT Security Team | Updated MFA coverage report supported by system configuration records |
| Security monitoring records do not establish that all critical alerts are reviewed within defined timeframes. | Security — CC7.2 | Partially Compliant | Risk of delayed detection and response to security incidents, potentially leading to data breaches or increased security damage | Review SIEM alert logs showing alert timestamps, review timestamps, assign reviewers and actions taken,address any gaps identified and document results. | High priority due to the risk of unauthorised access to sensitive information | Security Operations Team | SIEM logs, timestamps, and investigation records |
| Security monitoring records do not establish that all; critical alerts are reviewed within defined timeframes. | Security -CC7.2 | Partially Compliant | PayGo may be unprepared to respond effectively to security threats, causing delays and greater damage. | Conduct an incident response tabletop exercise.; ; Identify and address any weaknesses discovered.; ; Document the test results and corrective actions taken. | High priority due to delay in responding to cyber attack leading to delayed containment, greater data loss, and increased business disruption. | IT Security Team | Exercise reports, test results, and corrective action records |
| PayGo cannot demonstrate that its backups have been successfully restored during testing | Availability-A1.3 | Partially Compliant | Risk of data loss and prolonged business disruption if backups cannot be successfully restored | Conduct regular backup restoration tests, document the results, and investigate and resolve any restoration failures. | High priority due to possibilty of permanent data loss, prolonged system downtime, and disruption to payment services. | IT Infrastructure Team | Test reports, restoration logs, and records of corrective actions |
| Change records do not consistently demonstrate approval and testing before deployment. | Security — CC8.1 | Partially Compliant | Risk of system failures, security vulnerabilities and service disruptions due to changes that may not have been properly approved or tested before deployment. | Reviewing change records, enforcing approvals, and documenting testing results. | High priority due to possibilty of system failures, security vulnerabilities, or disruption to payment services. | IT Change Management Team | Change requests, approval records, and testing results |

## Usage

Read this `README.md` directly on GitHub, or open the original Excel workbook to review the source formatting and worksheet structure.

## Disclaimer

This is a case-study assessment and should not be treated as legal advice, a completed SOC 2 examination, or proof of GDPR compliance.
