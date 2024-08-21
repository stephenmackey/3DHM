# 4	Implementation

<a name="Section4.1"><a/>

## 4.1	Package Structure

The CITS 3DHM CITS inherits its package structure from the E-ARK Common Specification for Information Packages and is shown in [Figure 3](#fig3). It can be seen that additional folders have been added for Paradata, Other and optionally Authentication Documentation at root and representation level, but otherwise the structure is identical. 

<a name="fig3"></a>\

![Example Information Package Folder Structure](/specification/figs/fig_2_data_model_structure.svg "Data Model Structure")

**Figure 2:** Example Information Package Fol.der Strcuture
 
Multiple formats of the same 3D model that have been created through transformation events may be included in a single package and held in individual Representations (for example proprietary BIM models and STEP-IFC derivations). Information related to a transformation event (software used, parameters etc) should be included in the relevant documentation/paradata folder and details of the event recorded in PREMIS. 3D models of the same physical object can also be created via different means (e.g point cloud vs CAD based) and it a matter for the repository to determine if it considers these models to be the same or a different intellectual entity and thus whether they should be in the same or different information packages. Should models created via different methods be included in the same package then Rights information and Paradata may differ for each model and should therefore be held at Reepresentation level. Submission Agreements between Producer and Archive should detail whether different capture/creation versions of the same physical object are permitted in a single information package.

It is strongly recommended that as much documentation as possible related to the creation, context, provenance and terms of use of the model is included in the information package such as for example: licence terms, project overview, model creation and transformation information. The CITS 3DHM recommends the inclusion of such information related to the production of the model in a documentation/paradata sub-folder and related to archiving and use of the model in a documentation/other sub-folder. If model Authentication information (such as data quality rules) is included with the model then this can also be included in the optional documentation/authentication folder. Further information on model Authentication is provided in the accompagnying Guideline. The inclusion of a Submission Agreement in the information package is also recommended, located in the documentation/other sub-folder.

A similar folder structure is recommended within each Representation to hold information specific to that model format or derivation (for example data transformation processes, specific license information). 
Futher information on Paradata, its production, standards etc is included in the accompanying Guideline.

Specific requirements for the CITS 3DHM folder structure are as follows:

**3DHM1:** the package MUST have at least one Representation in the Representations folder.

**3DHM2:** the Documentation folder at package and representation level SHOULD have a sub-folder named Paradata.  This is an extension of CSIPSTR16.

**3DHM3:** the Documentation folder at package and representation level SHOULD include a sub-folder named Other. This is an extension of CSIPSTR16.

**3DPM4:** the Documentation folder at package level and representation level MAY include a sub-folder named Authentication. This is an extension of CSIPSTR16.

<a name="Section4.2"><a/>

## 4.2	Metadata and Supporting Information

<a name="Section4.1.2"><a/>

### 4.2.1	Descriptive Metadata
The package should contain general Descriptive Metadata about the digitised object and may contain specific Descriptive Metadata about the individual 3D model Representations. According to the Common Specification for Archival Description (CSAD) “Descriptive metadata can be expressed according to many current standards (i.e., MARC, MODS, Dublin Core, TEI Header, EAD, VRA, FGDC, DDI) or a locally produced XML schema”. Users may find that existing standards do not provide sufficient elements to adequately describe the creation of 3D models. This can be overcome through the use of specialised 3D Model schemas (i.e. CARARE, LIDO) and creation of locally produced, well formed schema as described in the CSIP and CSAD. The use of standards however is encouraged and greater extensibility can be achieved through use of for example the CIDOC-CRM (Common Resource Model) and extensions. Serialisation methods for metadata are not prescribed in the CSIP but use of METS and PREMIS which are only serialised in XML is mandatory, and hence encoding of additional, descriptive metadata in XML is preferable. Although CIDOC-CRM is primarily encoded in RDF, a schema is available for serialisation in XML.

**3DHM5:** the information package SHOULD contain Descriptive Metadata about the digitised object according to a current standard (such as MARC, MODS, Dublin Core, TEI Header, EAD, VRA, FGDC, DDI, CARARE, LIDO, CIDOC-CRM) or a locally produced, well formed schema located within the metadata/descriptive folder.

**3DHM6:** the information package MAY contain Descriptive Metadata about the Representations of the digitised object according to a current standard (such as MARC, MODS, Dublin Core, TEI Header, EAD, VRA, FGDC, DDI, CARARE, LIDO, CIDOC-CRM) or a locally produced schema located in the representation/metadata/descriptive folders.

<a name="Section4.2.2"><a/>

### 4.2.2	Preservation Metadata
Good practice in the management of 3D Heritage Model data requires that Information Packages include Preservation Metadata, specifically information related to:

•	Provenance
•	Reference
•	Fixity
•	Context

According to the CSPM: “When using Preservation Metadata together with the Common Specification for Information Packages (CSIP) (http://earkcsip.dilcis.eu), it is recommended that these are included in the information package in PREMIS format. Although this is not mandatory, all tools claiming to be able to validate CSIP compliant Information Packages must also be able to validate PREMIS metadata once it exists within the package. The two high-level requirements for the use of PREMIS in Common Specification IPs are that:

•	All Preservation Metadata is created according to official PREMIS guidelines;
•	All PREMIS metadata is referenced from the amdSec/digiprovMD element of the appropriate METS file.

It is recommended that users review the CSPM.

CITS 3DHM recommends the inclusion of PREMIS files at Representation level to include  provenance, rendering environment, origination information and if it exists Authentication information.

**3DHM6:** there SHOULD be (a) PREMIS file(s) produced according to CSPM and the requirements of this CITS in the representation/metadata/preservation folder of each Representation of the Information Package containing Preservation Metadata.

<a name="Section4.2.3"><a/>

### 4.2.3	Rights Metadata
From the Principle above, detailed Rights information should be recorded within PREMIS. As such a PREMIS file should be included at either package or in each Representation to contain this. 

**3DHM7:** there SHOULD be (a) PREMIS file(s) produced according to CSPM and the requirements of this CITS in the metadata/preservation folder of the Information Package or within each representation in the metadata/preservation folders containing Rights information related to all models or to individual models.

<a name="Section4.2.4"><a/>

### 4.2.4	Paradata
Paradata is defined as supporting textual material which concerns the conditions under which the model digitization (creation) took place, (who did it, where, what were the environmental conditions), the intended purpose of the model (documentation, research, communication), the reasons of decisions taken in the digitization process leading to the final result, and for reconstructions, the references to the documentation supporting the choice of added parts (images, drawings, reports, archaeological/historical interpretation).

Standards do not exist for the recording of Paradata but considerable work has been done in recommending best practice in the documentation of the process of creation of 3D models. Further information is included in the accompanying Guideline to this specification.

Within this 3D Heritage Model specification a specific folder for Paradata is defined as a sub-folder of the  Documentation folder at root or Representation level. Within the CITS the concept of Paradata is extended to include any unstructured textual material related to the creation, processing, transformation, rendering or quality or the model(s).

<a name="Section4.2.5"><a/>

### 4.2.5	Creating, Transforming and Rendering Hardware and Software
Details of the hardware and software used in the creation and transformation and required for the rendering of Heritage 3D Models can be captured in some specialised Descriptive Metadata schemas, described in event based ontologies such as the CRMdig extension of CIDOC-CRM, captured in PREMIS Preservation Metadata within object (creating application and extensions), environment function (rendering environment), event and agent entity semantic units or can be recorded as simple, unstructured text.

<a name="Section4.3"><a/>

## 4.3	METS

<a name="Section4.3.1"><a/>

### 4.3.1	Use of METS in CITS 3DHM
CSIP specifies that METS files should be located at the root of the package folder structure (Root METS) and optionally in each of the Representations within its respective root folder (Representation METS). CITS 3DHM has a requirement to contain at least one Representation and so will contain at minimum a root METS and a Representation METS file. 

<a name="Section4.3.2"><a/>

#### 4.3.2	Root METS File
The root METS file must adhere to the requirements of the CSIP and Information Package specifications. In addition, there are specific requirements for CITS 3DHM and in some cases, the level of the CSIP or package requirements have been increased (but never decreased).

<a name="Section4.3.3><a/>

#### 4.3.3	Root METS root element
CITS 3DHM does not change or extend any of the requirements for the Root METS root element. Information is given below regarding the specific content type attributes to be used in CITS 3DHM.

<a name="Section4.3.4"><a/>

### 4.3.4	Root METS header element (element metsHdr)
There are no specific requirements in CITS 3DHM for the root METS header section.

<a name="Section4.3.5"><a/>

### 4.3.5	Root METS descriptive metadata section (element dmdSec)
There are no specific requirements in CITS 3DHM for the root METS descriptive metadata section.

<a name="Section4.2.9"><a/>

### 4.3.6	Root METS administrative metadata section (element amdSec)
The administrative metadata section contains four sub-sections each used to record different types of metadata for package content: technical metadata (element techMD) records technical metadata, rights metadata (element rightsMD) records intellectual property rights information, source metadata (element sourceMD) records descriptive technical or rights metadata for an analogue source for a digital object, and digital provenance metadata (element digiprovMD) records digital preservation information, e.g. audit information for an object’s lifecycle.

The CSIP (and METS) categorise preservation metadata as administrative metadata, specifically digital provenance metadata (following the available guidelines published in the  Guidelines for using PREMIS with METS for exchange: http://www.loc.gov/standards/premis/guidelines2017-premismets.pdf) and hence all PREMIS  metada should be referenced from a single or multiple digiprovMD elements within the amdSec. 

Note that CSPM requires that all PREMIS is referenced from the digiprovMD element, including PREMIS Rights information and not via a separate rightsMD statement. 

<a name="Section4.3.6"><a/>

### 4.3.6	Root METS file metadata section (element fileSec)
The CSIP does not make use of the METS fileSec element mandatory, but it is strongly recommended. In CITS 3DHM the use of the METS fileSec element at the package level becomes mandatory, such as to reference the METS files within each representation and to reference the file groups containing Paradata Documentation, Authentication Documentation and Other Documentation.

<a name="Section4.3.7"><a/>

### 4.3.7	Root METS structural map (element structMap)
The METS structural map element is the only mandatory element in the METS specification. It provides an overview of the components described in the METS document. It can also link the elements in the structure to associated content files and metadata. In CITS 3DHM the package structMap describes the high-level structure of all the content in the package and links to at least one Representation. To allow for the inclusion of multiple Heritage Model representations in each package, the CITS 3DHM specification requires that each Heritage  Model has a discrete div element.

The representation METS.xml is referenced from the package METS.xml via the <mptr> element, and hence the requirements for the structMap element within the package METS.xml (CSIP requirements CSIP80 to CSIP118) are unchanged. Because a Representation is present, the need for a Content Division in the package METS.xml structMap is not required (CSIP101 to CSIP105).

The structural map should reference the documentation/paradata file group located in the documentation/paradata sub-folder by means of a separate div element.

The structural map should reference the documentation/other file group located in the documentation/other sub-folder by means of a separate div element.

If present, the structural map should reference the documentation/authentication file group located in the documentation/authentication sub-folder by means of a separate div element.

Implementers are welcome to define additional structural maps for their internal purposes by repeating the structMap element. The specific requirements for elements, sub-elements and attributes for CITS 3DHM, which differ from the CSIP, are listed in the following table. 

<a name="Section4.3.8"><a/>

### 4.3.8	Representation METS Files
The Representation METS files are used to describe the data structure as included in the data folder of each Representation (model representations) via the structMap element and to reference additional descriptive and preservation metadata.

#### 4.3.8.1	Representation METS root element
CITS 3DHM does not change or extend any of the requirements for the Representation root element but particular notice is drawn to the specific requirements of a Representation METS root element and the specific content type attributes to be used in CITS 3DHM.

#### 4.3.8.2	Representation METS header element (element metsHdr)
There are no specific requirements for the header element in a CITS 3DHM Representation METS. The 3DHM Representation metsHdr element should comply with the metsHdr requirements in the appropriate Information Package profile and can be used to identify specific agents related to a Heritage Model representation.

#### 4.3.8.4	Representation METS descriptive metadata section (element dmdSec)
There are no specific requirements in CITS 3DHM for the Representation METS descriptive metadata section.

#### 4.3.8.5	Representation METS administrative metadata section (element amdSec)
The administrative metadata section contains four sub-sections each used to record different types of metadata for package content: - technical metadata (element techMD) records technical metadata,; - rights metadata (element rightsMD) records intellectual property rights information; - source metadata (element sourceMD) records descriptive technical or rights metadata for an analogue source for a digital object; and – digital provenance metadata (element digiprovMD) records digital preservation information, e.g. audit information for an object’s lifecycle.

The CSIP (and METS) categorise preservation metadata as administrative metadata, specifically digital provenance metadata (following the avaiable guidelines published by the PREMIS EC guidelines: http://www.loc.gov/standards/premis/guidelines2017-premismets.pdf) and hence all preservation metadata should be referenced from single or multiple digiprovMD elements within the amdSec.

Note that CAPM requires that all PREMIS is referenced from the digiprovMD element, including PREMIS Rights information and not via a separate rightsMD statement. 

There are no specific requirements in CITS 3DHM for the Representation METS administrative metadata section.

#### 4.3.6	Representation METS file metadata section (element fileSec)
The CSIP does not make use of the METS fileSec element mandatory, but it is strongly recommended. In CITS 3DHM the use of the METS fileSec element at the Representation  level becomes mandatory, such as to reference the file groups containing data, Paradata Documentation, Authentication Documentation and Other Documentation.

#### 4.3.7	Representation METS structural map (element structMap)
The METS structural map element is the only mandatory element in the METS specification and is hence mandatory within the Representation METS. There must be one structural map present in each representation METS file following the requirements of the CSIP. 

The structural map should reference the documentation/paradata file group located in the documentation/paradata sub-folder by means of a separate div element.

The structural map should reference the documentation/authentication file group located in the documentation/paradata sub-folder by means of a separate div element.

The structural map should reference the documentation/other file group located in the documentation/other sub-folder by means of a separate div element.

Implementers are welcome to define additional structural maps for their internal purposes by repeating the structMap element. The specific requirements for elements, sub-elements and attributes for 3DHM CITS, which differ from the CSIP, are listed in the following table. 

## 4.4	PREMIS

<a name="Section4.4.1"><a/>

### 4.4.1	Use of PREMIS in CITS 3D PM
The use of PREMIS within the 3DHM CITS must follow the requirements of the CSPM which can be found at: https://dilcis.eu/content-types/cits-premis. 

Some PREMIS semantic units take the form of containers which comprise multiple sub (or even sub-sub) semantic units. Sub or sub-sub semantic units are not detailed in this specification if the container above has a level of MAY. Use of semantic units not listed should follow the requirements of the PREMIS data dictionary including the level (obligation). From the principles above:

**3DHM6:** there SHOULD be (a) PREMIS file(s) produced according to CITS PREMIS and adjusted to the requirements of this CITS in the metadata/preservation folder of the Information Package.

**3DHM7:** there SHOULD be (a) PREMIS file(s) produced according to CITS PREMIS and conforming to the adjusted requirements of this CITS in each Representation of the Information Package in the representation/metadata/preservation folder.

Following CSPM the CITS 3DHM follows the requirements and recommendation of the PREMIS Data Dictionary which can be found at: https://www.loc.gov/standards/premis/v3/premis-3-0-final.pdf.

<a name="Section4.4.2"><a/>

### 4.4.2	Attribute values and controlled vocabularies
Use of controlled vocabularies for the values of semantic units is encouraged within the PREMIS Data Dictionary and through best practice. Specific controlled vocabularies for semantic units are not provided by the CITS but their use is encouraged. If local vocabularies are used within the repository then these should be included within each package.

<a name="Section4.2.3"><a/>

### 4.2.3	Use of PREMIS at package level
PREMIS can be used in addition METS at package level to record Preservation and Rights Metadata. Note that if PREMIS is used then the requirements of the CSPM apply and those provided by the CITS 3DHM are in addition to these.

**3DHM65** Preservation information for the entire package (e.g. provenance, preservation actions) MAY be recorded within a PREMIS file located in the metadata/preservation folder and must follow guidelines set out in CSPM. 

**3DHM66** Rights for the entire package (e.g. copyright, license, other, rights grants) MAY be recorded within a PREMIS file located in the metadata/preservation folder using the PREMIS Rights semantic unit and must follow the guidelines set out in CSPM. Each individual rights statement (copyright, licence,  other, rights granted) must be held in a separate rightsStatement. Designation of the basis for the right or permission can be taken from the vocabulary available at: http://id.loc.gov/vocabulary/preservation/rightsBasis.html which are: license, copyright, statute, other. Information on rights associated with the rights basis can be included within the otherRightsInformation PREMIS semantic unit container using values from available controlled vocabularies.

<a name="Section4.2.4"><a/>

### 4.2.4	Use of PREMIS at Representation level
PREMIS can be used in addition METS at Representation level to record Preservation and Rights Metadata. Preservation information can include details of the object creating application via the creatingApplication semantic container and the required rendering environment via the Environment entity. Note that if PREMIS is used then the requirements of the CITS Preservation apply and those provided by the CITS 3DHM are in addition to these.

**3DHM67:** Preservation information for each Representation (e.g. provenance, preservation actions, creating application, rendering environment) MAY be recorded within a PREMIS file located in the representation/metadata/preservation folder and must follow guidelines set out in CITS PREMIS. 

**3DHM68** Rights information for specific Representations of the 3D model (e.g. copyright, license, other, rights grants) MAY be recorded within a PREMIS file located in the metadata/preservation folder of each Representation using the PREMIS Rights semantic unit and must follow the guidelines set out in CSPM. Each individual rights statement (copyright, licence,  other, rights granted) must be held in a separate rightsStatement. Designation of the basis for the right or permission can be taken from the vocabulary available at: http://id.loc.gov/vocabulary/preservation/rightsBasis.html which are: license, copyright, statute, other. Information on rights associated with the rights basis can be included within the otherRightsInformation PREMIS semantic unit container using values from available controlled vocabularies.

**3DHM48:**  Heritage Model authentication events MAY be recorded within a  PREMIS file located in each representation/metadata/preservation folder, using the PREMIS event semantic unit and should follow guidelines set out in CSPM. Values for eventTypes, eventDetailInformation and eventOutcomeInformation  should take values from a controlled vocabulary and events should be linked to their respective objects using a linking object identifier.
