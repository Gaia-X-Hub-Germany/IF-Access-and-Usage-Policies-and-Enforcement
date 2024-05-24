
| ID | Description       | Initiating  | Scope | Reference | Need | Comments | Details |
| :- | :---------------  | :---------  | :---- | :-------- | :--- | :------- | :------ |
| 1a | Create a PII principal - PII Controller Secure channel | PII Controller | YES | Extension | Exchange digitally Consent related artefacts securely (prevent usurpation of identity and tampering of artefacts) | Non Functional Requirement | Did com controller used in OCM/ CloudPCM  (used to share invitation link) then OID Protocol used OID for VCI and VP Possible to extend with custom protocol |
| 1b | Create a PII Controller – PII Controller Secure channel | PII Controller | YES | Extension | Exchange digitally Consent and PII Access related artefacts securely (prevent usurpation of identity and tampering of artefacts) | Non Functional Requirement | Did com controller used in OCM/CloudPCM(used to share link) then OID Protocol used |

2a
Receiving Privacy Notice – Human Readable
PII Principal
YES
ISO 29184
ISO/GDPR conformity – Enabling
PII Principal to decide if he
consents on collection and usage
of PII Data by a PII Collector for a
specific purpose.
CloudPCM- OCM used for issuance of a
Credential
Resolving "Privacy notice" is in the Consent Mgt
Plugin
Challenge 1: Definition of Privacy notice and how
to embed the content in the credential such that it
is tamper proof.
Solution Idea :
The evidence like a Hash of file. (But drawback
: insufficient as not showing/giving access to
the details of the notice.
"ZUGFeRD", JSON, pdf ,
Challenge 2 : If a link with hash is used as evidence,
a broken link would result in an invalid consent but
then a technical solution would be needed to
revoke the consent automatically.
Challenge 3 : the privacy notice content might need
to be "Private". 2 examples :
if the notice includes personal information.
if the notice is derived from a product
sold/licensed.by e.g. a lawyer
If you verify the validity of the consent and
understand what was consented to, the content of
the privacy notice is needed.
Solution Ideas :
Decentralised Ledger tamper- proof but public
?
The public ledger can be protected. (e.g.
encryption key as an attribute in the
consent to enable holder to access
content of the notice)
Misusing techno approach like DID Method
and its resolution to retrieve a DID document.
(instead of a DID document, retrieval of the
privacy notice)
Challenge 4: The privacy notice has to be accessible
for different PII Controller (e.g. in Health sector
several doctors for instance)
Other requirement : Versioning of privacy notice.
Embedded link shall point to one specific Version.
2b
Provide Privacy Notice - Human Readable
PII Controller
ISO 29184
3
Receiving Consent Receipts
PII Principal
YES
ISO 29184 / 27560
ISO/GDPR conformity –Enabling
PII Principal to make inquiries
and complaints toward PII
controller
4
Sending Consent Receipts
PII Controller
YES
ISO 29184 / 27560
ISO/GDPR conformity –Enabling
PII Principal to make inquiries
and complaints toward PII
controller
5a
Delivering a principal consent information to a PII
Controller who sent previously a Privacy Notice.
PII Principal
YES
ISO 29184 / 27560
ISO/GDPR conformity – Enabling
PII Principal to decide if he
consents on collection and usage
of PII Data by PII Controller and
Processor
Issuer of Credential is here opposite to Privacy
notice and Consent Receipt : The Cloud PCM (PII
Principal)
Either with
synchronous REDIRECT to the PII Controller shall
happen to continue the process on the PII
Controller side.
This REDIRECT is triggered from the Plugin when
giving Consent
or asynchronous delayed consent
The retrieval of the Consent Credential by the PII
Controller (OCM) can trigger an action at the PII
Controller side e.g. "Sending Consent Receipt" Sys
UC 4
5b
Delivering a revocation about a consent
information to a PII Controller who sent previously
a Privacy Notice.
PII Principal
YES
ISO 29184 / 27560
ISO/GDPR conformity –Enabling
PII Principal to revoke previously
consented privacy notice.
6
Receiving and Storing consent information (or
revocation) in Consent Record for further
processing
PII Controller
YES
ISO 29184 / 27560
ISO/GDPR conformity –Enabling
PII Controller to fullfill his legal
obligations (incl. revocation)
7a
Present a consent information to request PII access
and ...upon success : 7b
PII Controller
YES
Extension
Automate collection of PII Data
(through the consent
information)
7b
Receiving in return of 7a access key and address to
a PII hosted by another PII Controller
PII Controller
Extension
Automate collection of PII Data
(through the consent
information)
8a
Receiving consent information for PII access
request and...if the consent is successfully verified
(8b) provide access keys and address to a PII under
my control (8c)
PII Controller
Extension
Automate collection of PII Data
(through the consent
information)
8b
Verify a consent legitimacy to confirm if 8a is
successfull or not
PII Controller
YES
Extension
Automate collection of PII Data
(through the consent
information)
8c
Providing access keys and address to a PII under
my control
PII Controller
Extension
Automate collection of PII Data
(through the consent
information)
9
Extension of Services 2 to 8 to handle not only a
consent on a PII type but on a very specific instance
of PII Data. (The consent is not valid for the PII type
in general but ONLY for a unique PII_identifier)
PII Controller / PII
Principal
YES
Extension
handling of uniquely identified PII
data set.And not only PII type.
To clarify how to
enable this and such
that the artefacts
remain ISO Conform.
(How does the ISO
understand a consent
on PII type with a PII
identifier ? Is the
identifier only
informational and an
example of a PII Type
or does it restrict the
consent to that
identifier ?)
10
- Automated Consent functions limitation for
Principal with legal representant- Forward Privacy
Notice / Delegate Consent function to another PII
Principal (An official Legal representative of the
under aged PII Principal)
PII Principal
NO
Extension
Enable Use Case where the
Principal is not yet legally in age
to give himself a consent
(Child/Parent)
Note : PII Controller
would not be able to
find the other principal
(only the contact of the
one who sends the
consent is known)
11
Same as 5 but the consent shall contain
additionally:- legal representative PII Principal
Information who signed the consent.
PII Principal
NO
Extension
Enable Use Case where the
Principal is not yet legally in age
to give himself a consent
(Child/Parent)
Note : PII Controller
would not be able to
find the other principal
(only the contact of the
one who sends the
consent is known)
12
Browse and Read Consent Artefacts and their
status (Privacy Notice received, Consent given,
Consent Receipt received, Consent revoked or
declined)
PII Principal
YES
ISO/GDPR conformity –Enabling
PII Principal to make inquiries
and complaints toward PII
controllers
13
Browse and maintain Consent Records
PII Controller
NO
ISO/GDPR conformity –Fullfill a
part of the legal responsibilities
of a PII Controller
14
Validate PII Attributes
PII Controller
NO
Extension
Enabling PII controller to validate
if the PII attributes collected
match expectation the controller
expectation
xx
PII Processor functions
PII Processor
ISO 29184
NOT IN SCOPE
Current assumption :
functionalities for
Processors do not have
to be part of a MVP PII
Controller (Collect for
purpose X) then
Processor (working on
purpose X with
collected data). E.g.
Access to Data via
Credentials ? Are
processors using their
own systems or the
one from the
Controller to process
the data ? Probably it
depends.
Technical Enablers - or Artefacts needed for the
Services
A
Digital Identifier for Principal and Controller in
Privacy Notice to enable M2M Readable extensions
-
Extension
Process automatically:- granting
consent- revoking consent-
enable PII automated collection
from another PII Controller
B
Digital Identifier for Principal and Controller to
create Secure Channel
-
Extension
- Needed to enable
Item 1,2- Distinct
Identifiers from A !!
C
Tamper resistant and verifiable Consent (through
VC)
Extension
Process automatically:- granting
consent- revoking consent-
enable PII automated collection
from 3rd party
- Needed to ensure
consent can not be
tampered and
transferred to 3rd
Party to enable further
functions :
D
Consent Credential and Access Control Integration
Extensio
