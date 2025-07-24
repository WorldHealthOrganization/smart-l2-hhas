
This page lists and describes digital services relevant for a HHAS system, derived from the business requirements defined at the operational level (L2). 

For more details about end-users and related stakeholders, see the [Generic Personas](personas.html).

**Digital Services for a HHAS**

|Digital Service| Description |
|----------------|-------------|
|CAP Editor | Software tool or interface that allows authorized users to create, modify, and format CAP alert messages.  |
|HHAS Alert Reporter | Software tool that disseminates the message and can also ask for updates on its status. |
|HHAS Alert Aggregator | Software tool receives alerts from a reporter and keeps track of what happens to them as they are sent out.  |
|Health Worker Registry| A database that stores and manages information about healthcare workers, including their contact details, roles, specializations, and availability. This registry can be used to create a list of enterprise IDs for health workers.  |
|Health Facility Registry| A database that maintains information about healthcare facilities, such as hospitals, clinics, and emergency centers. This registry can include details about their location, capacity, services, and infrastructure. |

For additional actor definitions, see the [Digital Documentation of COVID-19 Certificates (DDCC) Implementation Guide](https://worldhealthorganization.github.io/ddcc/actors.html). Additionally, Integrating the Healthcare Enterprise (IHE) maintains a [repository with common actors](https://profiles.ihe.net/GeneralIntro/ch-A.html) used in IHE profiles.

### Key generic personas interacting with the system 
Generic personas in HL7 FHIR are represented using profiles of the various entity resources , such as [Practitioner](http://hl7.org/fhir/practitioner), [PractitionerRole](http://hl7.org/fhir/practitionerrole), and [RelatedPerson](http://hl7.org/fhir/relatedperson).



  
