# Business Processes - SMART L2 HHAS v0.1.0

* [**Table of Contents**](toc.md)
* [**Business Requirements**](business-requirements.md)
* **Business Processes**

## Business Processes

A business process, or process, is a set of related activities or tasks performed together to achieve the objectives of the health programme area, such as registration, counselling, referrals. Workflows are a visual representation of the progression of activities (tasks, events, interactions) that are performed within the business process. The workflow provides a “story” for the business process being diagrammed and is used to enhance communication and collaboration among users, stakeholders and engineers. The workflows included in this IG depict processes that have been generalized across different contexts and may not reflect the variability and nuances across different settings. The simplicity of the workflow may not adequately illustrate the nonlinear steps that may occur.

### Overview of Key Business Processes

The following table describes the workflows of the included processes.

| | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Issue and disseminate a heat event alert | HHAS.A | * National Alert Generating Agency
* National Alert Authorizing Agency
* Alerting Officer
 | To issue a CAP alert, decide on its dissemination and send targeted messages to health care facilities/health care workers. | *Starting point: The National Alert Generating Agency issues and sends/publishes a CAP alert for a heat event.** Issue a heat event CAP alert
* Decide on alert dissemination authorization
* Review the system generated message(s)
* Review and validate the list of recipients
* Send targeted message(s)
 |
| 2 | Implement HHAP operational plan | HHAS.B | * Healthcare facility manager
* Healthcare worker
* Surveillance Officer
* Client
 | To acknowledge the reception and understanding of the information provided within a CAP alert, act on targeted message(s) and submit heat event report(s). | *Starting point: The health facility manager/health care worker receives the targeted message(s).** Acknowledge the message(s) reception
* *(Health facility manager)* Send message(s) to health-care workers
* *(Health care worker)* Act on targeted message(s): 
* Perform actions that reduce occupational heat stress;
* Evaluate client symptoms against case definition;
* Report cases that meet the heat-related case definition.
 
* *(Surveillance officer)* Conduct heat event investigation 
* *(Surveillance officer)* Compile and submit heat event report 
 |

The picture below presents the overview of the business processes included in this guide.

![](./Overview_HHAS.svg) 

Note:

* The source files of the business processes designed for this guide can be downloaded [here](HHAS L2_BPMN files.zip).

#### A. Business process for issuing and disseminating a heat event alert

**Objective:** To issue a CAP alert, decide on its dissemination and send targeted messages to health care facilities/health care workers.

![](./HHAS_A.svg) 

**Business process "HHAS.A Issue and disseminate a heat event alert" notes and annotations:**

1. Forecast an upcoming heat event
* The National Alert Generating Agency uses climatological information and weather forecasts to identify upcoming heat events. Estimations concluding that predefined thresholds will be breached represent the trigger point for a HHAS workflow. The decision to issue or not a heat event alert should be determined from close collaboration of climate, weather, and health communities and policy developers and represents a judgment call of the group of people involved in the decision-making process.

1. Issue a heat event CAP alert (“Alert”)
* The Alert originator issues a heat event alert in the form of a Common Alerting Protocol (CAP) alert;
* The Alert should follow a CAP format, which is an open, non-proprietary digital message format for all types of alerts and notifications. CAP assists with clear quick action-oriented messaging through machine-to-machine dissemination and to a variety of partners and the public, through a generic XML format;
* One of the most used methods for disseminating CAP alerts is via the publish/subscribe mechanism, also known as CAP alert feeds, compliant with one of the three Internet standards for news feeds: Really Simple Syndication (RSS), Atom Syndication Format (ATOM), or message queue telemetry transport (MQTT) protocol. The subscribed actors, including the National Alert Authorizing Agency, can fetch the alert, usually via an alert aggregator service integrated into the HHAS solution;
* Beside the commonly used publish/subscribe mechanism for disseminating CAP alerts, other solutions can be implemented for delivering the CAP alerts (e.g. Mobile Alert Communication Management (mACM) Integrating the Healthcare Enterprise (IHE) profile). The dissemination method and technology remain a decision to be made during implementation;
* Guidelines: 
* Common alerting protocol (CAP 1.2), ITU-T X.1303 bis[1](#fn1);
* Common Alerting Protocol Version 1.2, OASIS[2](#fn2);
* Common Policies and Practices (Version 03)[3](#fn3);
* Mobile Alert Communication Management (mACM) IHE profile[4](#fn4);
 

1. Decide on Alert dissemination authorization
* The National Alert Authorizing Agency decides if the alert needs to be disseminated to health care facilities and/or healthcare workers. If available, decision-support logic integrated into the HHAS can help with the decision-making process;
* The decision process to authorize a heat-event and the group or Agency tasked to abide by that authorization process, should be decided on and developed through a co-design approach. Co-design involves the collaboration and active participation of multiple groups in the collective development to meet the diverse needs of those likely to benefit from heat event and heat-health related warnings. Important groups involved in the co-design process would include, NHMS, health ministries and associated agencies, social services, the emergency services, environmental health policy- and decision-makers, representatives of specific target (heat vulnerable/at risk/indigenous) groups for warnings and the public;
* Based on the co-design process, the Alert Authorizing Agency should make an interpretation of the hazard forecasts and impact estimates. Contextual factors, such as concurrent hazards which may hamper the population's ability to adapt their behaviours or environments (e.g., wildfires), pressures on the delivery of health and social care services (e.g., COVID-19 pandemic) and other indirect factors that might determine the general level of heat-related vulnerability such as the cost of energy for cooling.

1. Dissemination to health-care workers authorized?
* The Alert dissemination may be approved or disapproved;
* If approved, the system may include a confirmation of approval before further dissemination.

1. Review the system generated message(s)
* Once approved, the HHAS enhances automatically the Alert content with guidance from the pre-developed HHAP, based on pre-defined logic;
* The Alerting Officer receives a notification via the HHAS of a new Alert on subscribed CAP Feed and reviews the Alert, including the enhancements proposed by the HHAS.

1. Adaptation needed?
* The Alerting Officer determines if any additional enhancements are required for needs contextualized to the regions of impact.

1. Determine if direct dissemination to health workers is necessary
* The Alerting Officer follows the operational guidance from the local Heat Health Action Plan to determine if the alert must be sent directly to health care workers as well or only to healthcare facilities (health service managers).

1. Retrieve and review the list of recipients
* The affected area indicated in the Alert is the main criterion used to determine who should be the recipients of the message(s);
* The Alerting Officer identifies the impacted healthcare facility/healthcare workers through local mapping and healthcare registries;
* The HHAS can automatically retrieve the list of recipients from the health facility registry and/or health worker registry if those are available and interoperable with the HHAS. The Alerting Officer can review and update the list, for example add or remove recipients, as necessary[5](#fn5).

1. Send targeted message(s)
* The Alert, containing targeted information, is sent to the health care facilities and/or health care workers via appropriate distribution mechanisms;
* Upon receipt of the Alert, recipients are expected to confirm delivery through acknowledgment mechanisms. These may include: 
* explicit acknowledgments: manual confirmation actions such as clicking a receipt link or replying to the message;
* o implicit acknowledgments: automated system-level confirmations, such as read receipts or system logs.
 

1. Generate targeted message(s) with extra guidance
* The CAP message should be adapted based on the contextual factors of the heat event alert. In addition to the CAP standard elements (urgency, severity, certainty, etc.) included in the CAP alert provided by the Alert Generating Agency, contextualized details should be included, such as the potential impacts, disaggregated by vulnerable groups, and clear actions to reduce risk. Risk messaging can be co-developed in advance of a hazard with affected populations to help increase their preparation, based on the level of severity;
* Other improvements could include language adaptation or communication style of the healthcare facilities/workers, such as preference for adaptation measures;
* The resulting CAP message should be altered directly on the CAP Feed Service and maintain CAP message structure.

#### B. Business process for implementing HHAP operational plan

**Objective:** To acknowledge the reception and understanding of the information provided within a CAP alert, act on targeted message(s) and submit heat event report(s).

![](./HHAS_B.svg) 

**Business process "HHAS.B Implement HHAP operational plan" notes and annotations:**

1. Receives targeted message(s) for healthcare facility managers
* The targeted message(s) with guidance based on the HHAP and any extra local specificity is received by the health service managers. The managers should thoughtfully assess whether all the actions suggested in the messages are appropriate for their specific work environments, prioritizing the health and wellbeing of both clients (or patients) and staff;
* The acknowledgement for the message reception can be performed: 
* formally, via an explicit action such as confirming the alert reception by clicking a button, a link or by sending an email, etc.;
* informally and automatically performed by the system, for example, through the “read receipt” mechanism.
 

1. Send message(s) to healthcare workers
* Message(s) is(are) disseminated to the front-line health workers for their action and follow-up, in accordance with HHAP operational plans;
* The guidance can include specific actions to be performed by the health care workers to reduce potential negative impacts for the health system clients and/or advice on how to avoid exposure to occupational heat stress.

1. Perform actions that reduce occupational heat stress
* The health workers are one of the risk groups exposed to occupational heat stress, therefore they should perform the necessary actions to mitigate the negative impact the heat event can have on their mental and physical health.

1. Experiences heat-related illness
* The heat event alert is sent in advance of the onset date of the heat wave. Therefore, there is usually a delay between the date when a heat event alert is received by the health workers and the first impact on the health system is perceived, for example when the clients start experiencing heat-related illnesses and present to healthcare facilities. This delay might represent a couple of days or weeks, depending on how much time in advance the heat event is forecasted and the alert is sent;
* Prior to starting the clinical investigation, the client is identified and registered in the system. These activities are usually performed using paper registers or existing PCPOSS and are reflected in a DAK as a standalone "Registration" workflow. The "Registration" business process is not detailed in this DAK due to its generic nature.

1. Evaluate client symptoms against case definition
* The health worker evaluates the health status of clients presenting with a heat-related illness. The symptoms are evaluated against heat-related case definition used in the country or region;
* The health worker takes appropriate actions, according to the HHAP and other clinical guidance;
* In clinical settings, health care workers should apply clinical judgment to respond appropriately to each patient’s or client’s individual needs. They should understand the health risks associated with extreme heat and know how to take protective measures. If a patient or client appears to be at risk of overheating—such as living in an excessively hot room or home—health care workers should know what actions need to be performed to ensure their immediate safety;
* Guidance: 
* Public health advice on preventing health effects of heat: new and updated information for different audiences[6](#fn6);
* Treatment and Prevention of Heat-Related Illness | New England Journal of Medicine[7](#fn7).
 

1. Is the definition of a heat-related case met?
1. Report case
* A case that meets the definition of a heat-related case is reported to the surveillance team;
* Reporting the cases related to a heat event should be done as soon as they are detected, to allow for a real-time syndromic surveillance. This leads to better response time and actions, for example the surveillance data (daily deaths, daily calls to health information lines, daily ambulance calls, daily emergency room visits, occupancy rate of emergency room beds, etc.) might show increases in morbidity and mortality which might result in a decision to increase the alert level;
* The reporting of heat-related cases should be done via the HHAS or other digital tools interoperable with the HHAS, such as dedicated surveillance modules.

1. Continue HHAP response
* The HHAP is followed and implemented for each heat event and heat season, until the deactivation point is reached. This usually happens after an assessment of criteria concluding that the meteorological and health conditions are no longer a threat;
* To account for any “lag effect” in health impacts and ensure that the deactivation of an alert is not premature, some communities continue heat-alert activities for a few days after extreme heat conditions expire;
* Guidance: 
* Heat-Health Alerting system: guidance for health and social care providers[8](#fn8);
* Heat Alert and Response Systems to Protect Health: Best Practices Guidebook[9](#fn9).
 

1. Determine if heat event investigation threshold is reached
* The impact-based thresholds for heat-related cases are established based on health data reported by healthcare workers. Reaching a pre-determined threshold can be an important criterion when deciding if a heat event investigation needs to be performed. The threshold values should be defined according to country specific guidelines and guidance documents.

1. Heat event investigation needed?
1. Conduct heat event investigation
* The surveillance officer performs a heat event investigation, focusing on assessing the impact of the heat event on health and on the effectiveness of the HHAP implementation. The investigation may require the involvement and expertise of an epidemiologist specialised in heat-related cases;
* Potential indicators that could be included in the analysis: 
* number of daily heat-related deaths relative to historical baseline;
* number of daily emergency calls during the heat event;
* number of daily emergency room visits and hospitalizations during the heat event.
 
* Guidance: 
* Heat Alert and Response Systems to Protect Health: Best Practices Guidebook[9](#fn9).
 

1. Compile and submit heat event report
* The Surveillance Officer compiles and submits the heat event report based on the data reported by the healthcare workers and the heat event investigation conducted, if any. The reports inform further adjustments to the HHAP by providing relevant information for stakeholders, such as data that better explain the temperature-mortality relationships or the cost-effectiveness of interventions. The development of the HHAP is an iterative process that should include conclusions made based on surveillance and reporting data generated for past heat events;
* The quality of reports can be influenced by the capacity of the health system to deliver surveillance data;
* Guidance: 
* Heat Alert and Response Systems to Protect Health: Best Practices Guidebook[9](#fn9);
* “9.4 Use of surveillance data and monitoring in HHAPs”, Heat and health in the WHO European Region: updated evidence for effective prevention[10](#fn10).
 

1. Provide other relevant clinical services
* The health worker might provide other relevant clinical and support services, including referrals, if the case is evaluated as not being a heat-related case. The services needed are specific to each client and clinical condition(s).

1. Receives targeted message(s) for healthcare workers
* A trigger event for the implementation of the HHAP operational plan is the reception of targeted message(s) directly by the health care workers. This step implies that the message(s) is(are) directly disseminated to health care workers, without waiting for the information to be sent by the health service managers. This represents a streamlined workflow, based on strong DPI components and reliable distribution mechanisms;
* The acknowledgement for the message reception can be performed: 
* formally, via an explicit action such as confirming the alert reception by clicking a button, a link or by sending an email, etc.;
* informally and automatically performed by the system, for example, through the “read receipt” mechanism.
 

-------

**References:**

1 [SERIES X: DATA NETWORKS, OPEN SYSTEM COMMUNICATIONS AND SECURITY. Secure applications and services – Emergency communications. Common alerting protocol (CAP 1.2). Geneva: International Telecommunication Union; 2014](https://www.itu.int/en/ITU-D/Emergency-Telecommunications/Documents/2020/T-REC-X.1303bis-201403-.pdf) [↩](#ref1)

2 [Common Alerting Protocol Version 1.2, OASIS Standard](https://docs.oasis-open.org/emergency/cap/v1.2/CAP-v1.2-os.html) [↩](#ref2)

3 [Common Policies and Practices (Version 03)](https://docs.google.com/document/d/1h_6mtP8WMnyxKyzN_YTI4N2XR9QuTWs3/edit?pli=1&tab=t.0) [↩](#ref3)

4 [Mobile Alert Communication Management (mACM) IHE profile](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_Suppl_mACM.pdf) [↩](#ref4)

5 [Classification of digital interventions, services and applications in health: a shared language to describe the uses of digital technology for health, 2nd ed.](https://iris.who.int/handle/10665/373581) [↩](#ref5)

6 [Public health advice on preventing health effects of heat: new and updated information for different audiences. World Health Organization. Regional Office for Europe. 2011](https://iris.who.int/handle/10665/341580) [↩](#ref6)

7 [Treatment and Prevention of Heat-Related Illness. New England Journal of Medicine. Sorensen Cecilia, Hess Jeremy. 2022. doi: 10.1056/NEJMcp2210623](https://doi.org/10.1056/NEJMcp2210623) [↩](#ref7)

8 [Heat-Health Alerting system: guidance for health and social care providers. UK Health Security Agency. 2024](https://www.gov.uk/guidance/heat-health-alerting-system-guidance-for-health-and-social-care-providers) [↩](#ref8)

9 [Heat Alert and Response Systems to Protect Health: Best Practices Guidebook. Health Canada, Water, Air and Climate Change Bureau Healthy Environments and Consumer Safety Branch. 2012](https://www.canada.ca/content/dam/hc-sc/migration/hc-sc/ewh-semt/alt_formats/pdf/pubs/climat/response-intervention/response-intervention-eng.pdf) [↩](#ref9)

10 [Heat and health in the WHO European Region: updated evidence for effective prevention. World Health Organization. Regional Office for Europe. 2021](https://iris.who.int/handle/10665/339462) [↩](#ref10)

