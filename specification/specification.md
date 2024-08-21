# 3 Specification

<a name="Section3.1:><a/>

## 3.1	Requirements Structure
The Content Information Type Specification for 3D Heritage Model data aims to define the necessary elements required to preserve the accessibility and authenticity of 3D Heritage Model data over time and across changing technical environments. The specification elevates the level (and adjusts the cardinality) of some of the requirements set out in the Common Specification (CSIP) and package specifications (namely SIP and AIP) and adds new requirements for the package structure, descriptive metadata, preservation metadata and accompanying METS files. The specification sets out general principals that underpin the specific requirements and further context for the requirements and principals can be found in the accompanying guideline to this document.

<a name="Section3.2:><a/>

## 3.2	Principals

<a name="Section3.2.1:><a/>

### 3.2.1	Principal – data formats and representations
The E-ARK 3D Heritage Model content specification should be data agnostic, i.e. any type of data or data format for 3D models can be packaged for long-term archiving and none is excluded; however the use of open-standards and the inclusion in packages of multiple representations is encouraged to reduce the risk of data format obsolescence. Where open 3D model data formats exist (e.g. STEP-IFC for BIM) their use alongside original, proprietary data formats is strongly encouraged.

<a name="Section3.2.2:><a/>

### 3.2.2	Principal – use of PREMIS
From the CSIP and Common Specification for Preservation Metadata (CSPM): 
•	PREMIS should be used to record detailed technical metadata;
•	Technical information should be included in PREMIS metadata by using extension schemas;
•	Information about agents carrying out preservation actions must be recorded in the PREMIS  metadata (this is because METS agents describe agents relevant for generic IP level events such as the creation or submission of the package, not the preservation of the data);
•	Event descriptions should be included in PREMIS metadata. Use of the official PREMIS event vocabulary (https://id.loc.gov/vocabulary/preservation/eventType.html) is recommended;
•	Detailed rights information should be included in PREMIS. High-level rights information in METS indicates restrictions. Detailed, object-specific rights information should be included in the PREMIS metadata;
•	File format information for all files should be included as Persistent Unique Identifier (PUID) values in the appropriate PREMIS semantic units.

Desirable technical and preservation metadata in the context of the 3DHM CITS can include:
•	Reference to the content information standard (e.g. STEP-IFC);
•	Information about the generating system (Creating Agent software);
•	A description of the environment used to render the model.

Event descriptions can include:
•	Creation events;
•	Conversion or change events;
•	Model authentication events.

Detailed technical metadata in the context of the 3D Heritage CITS can include:
•	File format, characterisation,  checksums;
•	Relationships (is part, contains parts).

Rights information can include:
•	Access rights;
•	License restrictions;
•	Copyright owner.

Use of PREMIS must conform to the requirements of the CSPM. 

<a name="Section3.3:><a/>

## 3.3	Use Cases for Archiving of Heritage Model Data
Further detail of the use cases for long-term archiving of 3D Heritage Model data are given in the accompanying Gguideline. In summary, the use cases for archiving of 3D Heritage Model data  are determined to be:
1.	To enable long-term archiving of 3D Heritage Model data whilst preserving the authenticity and accessibility of the data over time;
2.	To enable inter-organisational exchange of 3D Heritage Model data whilst facilitating the understanding of the provenance, context and means to render;
3.	To enable acceptance of 3D Heritage Model data submission packages (SIPs) at a central repository. 

