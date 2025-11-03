<!---Note: Please keep the div below in the main branch and when publishing the pre-release version of the DAK (v0.9.9). For official published versions, please delete the div from the file.-->
<div>
<p> This SMART Guidelines L2 specifications and set of implementation tools are still undergoing development. </p>
<p> Content is for demonstration purposes only. </p>
</div>{:.stu-note}


### Introduction 
Extreme heat events globally have led to a rise in related mortality and morbidity, but the adverse health effects of hot weather and heatwaves are largely preventable. Prevention requires a portfolio of actions at different levels: from health system preparedness coordinated with meteorological early warning systems to timely public and medical advice. These actions can be integrated in a defined Heat-Health Action Plan (HHAP). 
Important elements for the successful implementation of HHAP are the heat-related health information plans and operational plans for health care and social services within the health system. A heat-related health information plan defines what is communicated, to whom and when, including the specific target audience, the means of communication, as well as the contents and time the information is to be delivered. An operational plan provides clear guidance to healthcare workers and healthcare facilities about what actions need to be taken, linked to the heat-health warnings issued. Together, these are used to ensure that all relevant parties have the information they need to prepare the health system to respond to heat events.
Alert messages work best when tailored and targeted to their intended audiences, including healthcare workers.  These messages encompass not only the types of information provided, but also ensuring the correct healthcare system actors and systems, often dictated by the impact area of the heat event, are mobilised in a timely manner.
To augment existing "last mile" channels of communication to healthcare workers, digital technology can be leveraged to ensure more efficient, effectively and targeted messaging. In particular, existing standards such as the Common Alerting Protocol (CAP) from the World Metrological Organization (WMO) - which is designed to provide a consistent format for emergency alerting across various technologies - can be harnessed in conjunction with a wide range of internet, short message systems (SMS), or application-based solutions, to optimize the healthcare response to heat events.  

#### Purpose of this IG
This IG lays out business specifications for a Heat-Health Alert System (HHAS), where one or several CAP-formatted alerts can be sent to targeted healthcare worker recipients, and can record the outcomes of any human interactions upon receipt of the alert. The IG leverages existing free and open standards and is driven by use cases and requirements for effectively alerting the healthcare workers that will be impacted by a heat event.
As Member States are increasingly looking to adopt digital solutions as part of the implementation or iteration of a HHAP, this document provides a baseline set of requirements for a HHAS solution that is interoperable with other standards-based health solutions. With the baseline requirements met, it is also anticipated that Member States will further adapt and extend these specifications to suit their needs, most likely working with a local technology partner of their choice to implement a digital solution.
This document is therefore software-agnostic and provides a starting point for Member States to design, develop and deploy a HHAS digital and data information systems solution for national use in whichever format best suits their needs.

#### Target audience

The primary target audience of this document is the national authorities tasked with implementing or overseeing their country's HHAP, in particular those coordinating the heat health information plans, managing digital systems, and designing and implementing operational plans for health care and social services within the health system. The document may also be useful to government partners such as local businesses, international organizations, non-governmental organizations and trade associations, that may be required to support Member States in developing or deploying a HHAS solution within existing data systems and technical resources.

#### Scope
##### In Scope
This IG specifically focuses on how to design the integration of health information systems from the climate and the health sectors to interoperate and function in coordination to digitally transmit a heat event CAP alert to healthcare workers and facilities. The approach is based on the required data to identify and target specific healthcare workers, leveraging facility location and/or healthcare worker registries. This document describes a specification for such a CAP Messaging system, including:
- Use cases arising from the operation of a HHAS, including the sequence of steps involved in executing a HHAS solution; 
- A core data set with data elements and digital services that can be leveraged by HHAS to identify and target specific healthcare workers, such as facility location and/or healthcare worker registries, as well as health guidance to healthcare workers;
- Approaches for implementing a HHAS, including considerations for integrating with existing emergency response and health information systems, as well as existing communication platforms.

##### Out of Scope
Aspects that are considered out of the scope of this work are:
- Digital documentation on the manner of production and publication of the CAP message. These are assumed to be generated by established Member State meteorological, emergency and/or health services, and disseminated through existing national or regional warning systems in a CAP format;
- Detailed protocols for emergency medical response or hospital surge capacity management. These are addressed in existing healthcare emergency preparedness plans;
- The specific content of the heat-health guidance to healthcare workers and healthcare facilities. This will vary by region and national context and should be developed by relevant public health authorities;
- The process of training healthcare workers to use the HHAS;
- Delivering alert messages to general public;
- Considerations for monitoring and evaluation of HHAS roll-out and use.

#### Assumptions
This document operates under the assumption that Member States can utilize Hazard Early Warning Systems (HEWS) to generate CAP-compliant heat event alerts as a foundational approach. This acknowledges the immediate need for scalable solutions while recognizing that integrating impact-based data into CAP for enhanced public health protection is a longer-term objective. For additional details:
- CAP is a standardized data interchange that is open-source and XML-based, with clearly defined elements, and the ability to support data exchange across multiple dissemination channels, allowing a single input to generate multiple outputs for downstream dissemination. CAP-enabled systems can therefore facilitate easier integration with other national and international information systems; 
- HHAPs Guidelines include the inclusion of early warning systems as crucial components in protecting public health during extreme heat events. These systems, encompassing both hazard-based (HEWS) and impact-based (Heat Health Warning Systems - HHWS) approaches, aim to provide timely alerts to mitigate heat-related risks. Hazard warnings focus on the intrinsic characteristics of the impending event, such as heatwave intensity (temperature, humidity). Impact warnings, conversely, translate these characteristics into potential consequences for people, infrastructure, and livelihoods (i.e. a 'thermal temperature' calculation which measures the health risks of how heat directly affects people). While impact warnings offer more actionable information, hazard warnings remain more accessible, particularly for resource-constrained countries, which requires additional coordination and data;
- The categorization of heat events within CAP necessitates further development. CAP supports categorization of events by using Event Type Codes. Coded values, if formatted properly, can alleviate the dimension of language as an issue to resolve when processing an alert. Applying a code to each item in a list is desirable for automated systems and systems that deal across languages. This codification further enables advanced processing of alerting systems and automations. For example, a coded value for a pre-defined event type allows consumers to have a pre-defined response to any alert message associated with that event type;
- Currently, the Event Type Codes in CAP are 'Temperature' as a broad category (Tier I) and 'Heat wave' as a more specific (Tier II) category. This is a challenge as heat events are diverse in their categorization, and evidence suggests events be differentiated based on temperature indicators, thermal (heat-stress) indicators, and heatwave-intensity indices. Countries differ in how these various heat events are defined, calculated, and their implications. As such, the current absence of standardization in heat event categorization necessitates further development of the protocol, where 'Temperature' and 'Heat-Wave' require alternative and additional specifications;
- The generic term heat event is used in the current documentation to encompass the various categories, given the calculations required to trigger the heat event are out of scope for this documentation. Ultimately, regardless of the term assigned to the event or alert, the social responsibility of an alerting authority is to effectively communicate the hazards and concerns associated with a subject event. In each case, representatives of the alerting authorities that chose these terms felt the chosen term was the correct one for that situation.


The requirements outlined are intended to allow for HHAS solutions to meet the needs of a country's HHAP, while still being usable in other national and local contexts.<br>

The technological specification for a HHAS solution is intended to be flexible and adaptable for each Member State to meet its diverse public health needs as well as the diverse needs of individuals around the world. It is assumed that there is no one-size-fits-all solution, and so the specification must remain flexible and software-agnostic, while minimizing the amount of digital infrastructure required.<br>

An overarching assumption is that multiple digital products will be implemented to operationalize the requirements described in this document. This allows for support of local and sustainable development so that Member States have a broad choice of appropriate solutions without excluding compliant products from any source.<br>

The following assumptions are made about Member States' responsibilities as foundational aspects of setting up and running a HHAS solution:
- Member States have access to reliable and accurate **meteorological and/or emergency services** capable of generating and disseminating timely heat-wave forecasts and warnings; 
- Member States possess or are in the process of developing **functional health information systems** that can store and manage relevant data, including healthcare worker registries, health facility databases, and patient records.
- Member States **maintain up-to-date registries** of healthcare workers, including their contact information, specializations, and locations, as well as comprehensive databases of healthcare facilities with their capacities and services;
- Member States have access to **reliable and accessible communication infrastructure**, including internet connectivity, mobile networks, and other communication channels, to enable the dissemination of alerts and information;
- Member States have established or are developing **comprehensive HHAPs** that outline clear roles, responsibilities, and procedures for responding to heat events;
- Member States have established **mechanisms for coordination** between meteorological services, public health authorities, and healthcare providers;
- Member States have the **capacity to maintain, update, and support** the HHASs, including technical expertise and resources;
- Member states will provide **adequate training** to relevant personnel including healthcare workers on the use of the HHAS system and heat-related health protocols.


### L1 Narrative guidelines
References used in this implementation guide are listed below:

- [Heat and health in the WHO European Region: updated evidence for effective prevention. World Health Organization. Regional Office for Europe. 2021](https://iris.who.int/handle/10665/339462);
- [Updating the evidence related to heat-health action planning: 21-22 November 2018, Bonn, Germany: meeting report. World Health Organization. Regional Office for Europe. 2019](https://iris.who.int/handle/10665/346259);
- [Improving public health responses to extreme weather/heat-waves: EuroHEAT: technical summary. World Health Organization. Regional Office for Europe. 2009](https://iris.who.int/handle/10665/107935);
- [Report of a scoping meeting for the selection of indicators to monitor the impact of extreme heat on maternal, newborn and child health: Geneva, Switzerland, 24-25 April 2023. World Health Organization. 2024](https://iris.who.int/handle/10665/378102);
- [Public health advice on preventing health effects of heat: new and updated information for different audiences. World Health Organization. Regional Office for Europe. 2011](https://iris.who.int/handle/10665/341580);
- [EuroHEAT: improving public health responses to extreme weather/heat-waves: summary for policy-makers. World Health Organization. Regional Office for Europe. 2009](https://iris.who.int/handle/10665/107934);
- [Heat-health action plans: guidance. World Health Organization. Regional Office for Europe. 2009](https://iris.who.int/handle/10665/107888);
- [Heat-waves: risks and responses. World Health Organization. Regional Office for Europe. 2004](https://iris.who.int/handle/10665/107552).

Other, non-WHO, references used in this implementation guide are listed below:
- [User guide Weather-health alerting system. UK Health Security Agency. Met Office. 2025](https://assets.publishing.service.gov.uk/media/67f3aeaed3f1efd2ce2ab897/WHA_User_Guide.pdf);
- [Treatment and Prevention of Heat-Related Illness. New England Journal of Medicine. Sorensen Cecilia, Hess Jeremy. 2022. doi: 10.1056/NEJMcp2210623](https://doi.org/10.1056/NEJMcp2210623);
- [Heat Alert and Response Systems to Protect Health: Best Practices Guidebook. Health Canada, Water, Air and Climate Change Bureau Healthy Environments and Consumer Safety Branch. 2012](https://www.canada.ca/content/dam/hc-sc/migration/hc-sc/ewh-semt/alt_formats/pdf/pubs/climat/response-intervention/response-intervention-eng.pdf);
- [Common Alerting Protocol Message Broker for Last-Mile Hazard Warning System in Sri Lanka: An Essential Component. SSRN Electronic Journal. 10.2139/ssrn.1568001. 2007](https://www.researchgate.net/publication/228242993_Common_Alerting_Protocol_Message_Broker_for_Last-Mile_Hazard_Warning_System_in_Sri_Lanka_An_Essential_Component).

### L2 Operational guidelines

- Implementation tools:

   - [Link to the editable files of business processes, in .bpmn format](https://worldhealthorganization.github.io/smart-l2-hhas/business-processes.html)
   
   - [Link to core data dictionary](https://worldhealthorganization.github.io/smart-l2-hhas/dictionary.html)
 
   - Decision-support logic is not available at the moment. 

   - Scheduling logic is not available at the moment.

   - Indicators are not available at the moment.
 
   - [Link to functional and non functional requirements](https://worldhealthorganization.github.io/smart-l2-hhas/system-requirements.html).

### L3 Machine readable guidelines
The L3 FHIR Implementation Guide for the HHAS L2 SMART Guidelines is yet to be published. Links will be published here as soon as they're available.

### L4 Executable guidelines
Reference implementations representing the L4 layer for the the HHAS L2 Guidelines are not yet available. Links will be published here as soon as they're available.

### L5 Dynamic guidelines
Content representing the L5 layer for the HHAS L2 SMART Guidelines are not yet available. Links will be published here as soon as they're available.

### Contact Us
<p>Please let us know about your experience in using this L2 specifications and questions you may have by contacting us at <a href= "mailto:SMART@who.int?subject = HHAS L2 Feedback">SMART@who.int</a></p>

### License
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 3.0 IGO License][cc-by].

[![CC BY 3.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by-nc-sa/3.0/igo/
[cc-by-image]: https://i.creativecommons.org/l/by-nc-sa/3.0/igo/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%203.0-lightgrey.svg

For more license details please see the [license page](https://worldhealthorganization.github.io/smart-l2-hhas/license.html).

### Providing Feedback
{% include feedback.md %}

<!---Note: Please keep the dsiclaimer note below in the main branch and when publishing the pre-release version of the DAK (v0.9.9). For official published versions, please delete the note from the file.-->
### Disclaimer
The specification herewith documented is a demo working specification and may not be used for any implementation purposes. This draft is provided without warranty of completeness or consistency and the official publication supersedes this draft. No liability can be inferred from the use or misuse of this specification or its consequences.