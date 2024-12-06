# Blood-donation-management-system
SCOPE:
The Blood Donation Management System aims to manage blood donation operations, making it easier to match blood donors with recipients. The system provides functionalities for registering donors and recipients, managing blood requests, and searching for donors based on blood type or location. Admin users will have the capability to approve, match, and manage blood transfusion requests. The scope also includes potential enhancements, such as incorporating a notification system and generating statistics for insights.

OBJECTIVE:
1.	Facilitate Donor and Recipient Registration:
Allow users to register as donors or recipients by providing their details, such as blood type, availability, and contact information.

2.	Streamline Blood Request Management:
Admins can review and approve blood transfusion requests, match available donors with recipients, and monitor the status of each request.

3.	Provide an Efficient Search Functionality:
Enable users to find suitable donors based on criteria like blood type and geographical location.

4.	Improve User Communication:
Notify recipients about the availability of matching donors through an integrated notification system.

5.	Generate Useful Statistics:
Analyse stored data to create reports that can help admins make data-driven decisions, such as identifying high-demand blood types or the most active donor regions.

LIMITATIONS:
1.	Dependency on Manual Data Entry:
The accuracy of the information in the system relies on users providing correct and complete data during registration and blood request submissions.

2.	Geographical Constraints:
The system may face limitations in matching donors and recipients if there aren't enough registered users within certain regions, impacting the ability to fulfil blood requests.

3.	Data Privacy and Security:
Personal information such as contact details must be stored securely to prevent unauthorized access, which requires strong data protection measures.

ENTITIES AND ATTRIBUTES:
1. Donor:
Donor-ID (primary key), Name, Age, blood-type, Contact numbers Address, Last-Donation-Date.

2. Donation:
Donation-id (primary key, Donor-ID (Foreign key), Date-of-Donations, Blood-Quantity, Blood-Type, Donation-Centre.

3. Blood-Inventory:
Inventory - Id (primary Key), blood-type, Quantity- Available, Expiry date, storage Location, Donation-ID (Foreign key).

4. Recipient:
Recipient_id (primary Key), name, age, Blood type-Needed, Hospital- ID (Foreign key) Contact Number, Request Date.

5. Hospital:
Hospital-Id (primary key, Hospital-Name, location, Contact-Number, Blood-bank- Affiliation, emergency-level.

6. Blood-Request:
Request (primary key), Recipient-id (foreign key), Blood-Type-Requested, Quantity-Requested, fulfilment status. Request-Date.

RELATIONSHIPS:
1. Donor-Donation:
Relationship: A donor can make multiple donations but each donation is linked to one donor.
Degree: Binary
Cardinality: one-to-many

2. Donation - Blood Inventory:
Relationship: Each donation updates the blond inventory; one inventory record contain record of one or more donations
Degree: binary
Cardinality: one-to-many

3. Recipient-Blond request:
Relationship: A recipient can make multiple blood request and each request has separate recipient.
Degree: Binary
Cardinality: one-to- many

4. Blood Inventory-Hospital:
Relationship: A hospital has access to more than one blood inventory and each inventory record can be accessed by more than one hospital if needed.
Degree: Binary
Cardinality: many-to-many

5. Hospital-Recipient:
Relationship: A hospital can serve multiple recipient and each recipient in associated with one hospital.
Degree: Binary
Cardinality: one-to-many

6. Blood Request-Blood inventory:
Relationship: each blood request form access more than one inventory record and each inventory satisfy multiple blood request.
Degree: binary
Cardinality: many-to-many

DOCUMENTATION:
The ER Diagram Contains the system entities, attributes, relationships and rules. The main thing is to ensure accurate relationship, degree, Cardinality. Analysing potential Chasm and fan trap is also Crucial to refine the ERD.


5.	No Real-Time Blood Availability Tracking:
The system relies on user-reported availability rather than real-time tracking of blood inventory in hospitals and blood banks.

6.	Limited Automation in Matching:
While the system may assist admins in matching donors with recipients, the actual process may still require manual decision-making.
