
The user scenarios are narratives that describe how the different personas may interact with each other and with the digital system. The user scenario is provided to help the reader better understand how the system will be used and how it would fit into existing workflows.


**User scenario for dissemination of a heat event alert through Healthcare Facility Managers**


<div>
<table border="1">
	<tbody>
		<tr>
			<td><strong>Key personas</strong></td>
			<td> <strong>National Alert Generating Agency:</strong> National Meteorological and Hydrological Service (NMHS) <br>
<strong>National Alert Authorizing Agency:</strong> National Public Health Authority <br>
<strong>Alerting Officer:</strong> Albert  <br> <strong>Facility Manager: </strong>Ben <br> <strong>Health worker:</strong> Melinda
</td>
		</tr>
		<tr>
			<td colspan="2">
			<p>
			Early this morning, the National Meteorological and Hydrological Service (NMHS) issued a heat event alert for several districts via the Common Alerting Protocol (CAP) to the National Public Health Authority. As the National Alert Authorizing Agency, the National Public Health Authority followed a comprehensive health risk assessment - developed from close collaboration of national, regional, and local climate, weather, and health communities and policy developers and decided to approve further dissemination of the heat event alert. Upon approval, the heat event alert was transmitted in CAP format via the national heat-health alert system to the impacted district's Regional Public Health Authorities. </p>
<p>Albert, a senior officer at one of the impacted Regional Public Health Authorities, received the CAP alert through the heat-health alert system. His agency serves as the aggregator of alerts for local health stakeholders. Using the heat-health alert system's integrated web-based tool, Albert reviews the affected geographic areas on a map and starts configuring the alert message for localized dissemination, according to his local Heat Health Action Plan's guidelines. He adjusts the CAP message to reflect district-specific risk factors and actionable guidance tailored to facility managers. He further adapts the CAP to ensure the language matches the local dialects of the targeted districts and ensures the alert content and the attached guidance matches the language used in those communities. Because the heat-health alert system is interoperable with the national health facility registry, the list of concerned health care facilities is automatically retrieved, together with relevant information (health facility ID, health facility address, health facility managers' first and last names, etc.). Albert reviews the auto-generated list of recipients and digitally transmits the localized CAP alert to the designated facilities, including embedded operational guidance aligned with HHAP protocols </p>
<p>
Ben, the manager of a health facility, logs into his health facility's Health Information System (HIS) using his unique ID to begin his daily tasks. Upon login, he receives a system notification about the heat event alert from the regional authority. He opens the message and sees the event severity level (severe), the predicted timeline of the event (start: next day; duration: 5 days), and the certainty of the event. He can also download the guidance outlining facility-level preventive measures and specific risk populations to prioritize. After reviewing the message, Ben formally acknowledges receipt and comprehension of the alert content by clicking the "Acknowledge" button in the HIS. Throughout the day, Ben initiates dissemination of the alert by following facility operational guidelines, including:
- alerting health workers via HIS notifications, email, SMS, social media, and in-person briefings;
- creating and assigns tasks in the HIS to facilitate accountability and track HHAP implementation; and
- ensuring that frontline health workers understand their roles and the actions to be performed.</p>
<p>Ben remains confident that the coordinated actions, triggered by the alert system and empowered by the HHAP, will mitigate health risks among patients and staff during the heatwave period.
			</p>
			</td>
			</tr>
			<tr>
			<td>Corresponding business processes  </td>
		<td> This scenario refers to the following business processes:<br> A. Issue and disseminate a heat event alert <br> B. Implement HHAP</td>
			</tr>
		</tbody>
</table>
</div>

**User scenario for direct dissemination of a heat event alert to health workers**

<div>
<table border="1">
	<tbody>
		<tr>
			<td><strong>Key personas</strong></td>
			<td> <strong>National Alert Generating Agency:</strong> National Meteorological and Hydrological Service (NMHS) <br> <strong>National Alert Authorizing Agency:</strong> Ministry of Health  <br> <strong>Alerting Officer: </strong> Carlos <br> <strong>	Health worker:</strong> Andrea
</td>
		</tr>
		<tr>
			<td colspan="2">
			<p>
			Today, the National Meteorological and Hydrological Service (NMHS), acting as the National Alert Generating Agency, forecasted an upcoming heat event based on nationally determined thresholds. They generate and transmit a heat event alert following the Common Alerting Protocol (CAP) format to the Ministry of Health (MoH). After performing a comprehensive risk assessment, the MoH classified the event severity to "moderate" and approved the dissemination of the alert to frontline health workers  </p>
<p>Carlos works as an Alert Aggregator System Monitor  within the Ministry of Health. He's responsible for aggregating health alerts, reviewing and adapting the alert content for alignment with predefined protocols or guidance, and disseminating the alerts to healthcare facilities and/or healthcare workers. The ministry recently developed and implemented a health alert system that helps the alert aggregators, such as Carlos, to perform most of their day-to-day activities, such as adapting the alert messages (including adding translations in different languages), sending the alerts, performing CRUD (create/read/update/delete) actions on system users, viewing the alerts recipients, and more. Since the heat-health alert module, integrated in this system, is aligned with the heat-health action plan (HHAP), the system automatically enhanced the CAP alert with appropriate guidance for the health workers according to pre-defined logic, therefore there is no need for manual adaptation for this type of alert. The guidance includes critical information for operationalizing the HHAP, including at-risk populations, potential impacts on health and social care services, and a list of actions to be performed depending on the heat event severity level.  </p>
<p>
Using a web-based tool within the heat-health alert module, Carlos reviews the autogenerated map which indicates the targeted geographic areas. The health alert system is interoperable with the Health Information System (HIS), therefore the heat-health alert module is capable to retrieve automatically from the health workers registry the list of recipients which is represented by the health workers in those areas. Carlos does a final review of the alert message content, confirms that the alert should be disseminated directly to healthcare workers as well (besides dissemination to healthcare facilities), reviews the recipients list and sends the CAP alert message.</p>
<p>Andrea is a clinical social worker who's serving a rural community. Today she's visiting an elderly man to support him with developing digital skills so that he can access digital services offered by the local health facility. Andrea receives 2 SMS messages. She opens them and can see that both are related to a heat event alert sent by the Ministry of Health. Once opened on a phone with internet connection, the HHAS receives automatically an acknowledgment marking the alert reception. The first SMS includes information about the severity level of the alert, the risk groups concerned and a link to actionable guidance. The second one includes recommendations on how to identify the signs and symptoms of occupational heat stress and how to mitigate the potential impact [resting immediately in a cool place when experiencing muscular spasms (particularly in the legs, arms or abdomen), periodically drinking non-alcoholic fluids, regardless of the activity level, and eating cold foods, particularly salads and fruit with high water content, etc.]. Recognizing that herself as well as her client  is part of at-risk group (vulnerable elderly cohort and health-care workers), Andrea integrates preventative actions, aligning with the CAP alerts information, into her care plan. The local authorities provide small incentives for operationalizing the HHAP so Andrea logs her planned interventions in the HIS to track HHAP implementation and qualify for local incentives. 
			</p>
			<p> Energized by timely information, Andrea is heading to her client - confident that these measures will help mitigate heat-related harm.</p>
			</td>
			</tr>
			<tr>
			<td>Corresponding business processes  </td>
		<td> This scenario refers to the following business processes:<br> A. Issue and disseminate a heat event alert <br> B. Implement HHAP</td>
			</tr>
		</tbody>
</table>
</div>

**How to interpret user scenarios**

User scenarios can be helpful tools not only to better understand the context in which a digital tool would operate, but also for some insights into what key data elements would need to be recorded and accounted for in the database. Additionally, the context in which the tool would operate, illuminated by the user scenarios, provides insight into some functional and non-functional requirements that the system would also need.

As examples, the scenarios identify: 
- key data elements that need to be recorded and/or calculated;
- decision-support logic that can be automated in the system;
- key functional and non-functional requirements that should be included in the system.
