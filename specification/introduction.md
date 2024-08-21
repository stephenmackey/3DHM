# 2	Introduction

<a name="Section2.1"><a/>

## 2.1	Purpose
The purpose of this document is to describe the Content Information Type Specification for 3D Heritage Model data (CITS 3DHM). The specification is designed to be used for the transfer to archives as well as for records exchange between different organisations and repositories. This specification is supported by METS profiles for the Root and Representation METS files and an accompanying Guideline document.

<a name="Section2.2"><a/>

## 2.2	Scope
Use of 3D data is widespread across many domains, with a plethora of applications and data formats. This 3DHM content specification limits its scope to the area of 3D models of cultural heritage artefacts, buildings and sites that have been produced by methods such as:

•	Point cloud models (for example by: photogrammetry, laser scanning, structured light);
•	CAD based models (including building information models, BIM amd heritage building information models, HBIM);
•	Volumetric models (computer tomography);
•	GIS models; and
•	Procedural modelling (reconstructions).

Further background on this can be found in the accompanying Guideline document.
The scope of the CITS may evolve in future to accommodate other production technologies. The 3DHM CITS has a related specification for 3D Product Model data, CITS 3DPM.

<a name="Section2.3"><a/>

## 2.3	Layered Data Model 
This section introduces the role of the CITS 3DHM and its dependencies on the basic structures of the Information Package.

>This specification is created based on the requirements of the Common Specification for Information Packages (CSIP),  the specification for Submission Information Packages (E-ARK SIP) and the specification for Archival Information Packages (E-ARK AIP). To fully understand its requirements, we highly recommend that users review the requirements and the terminology of the source documents, before using this specification.

The data model structure is based on a layered approach for information package definitions [Figure 2](#fig2). The Common Specification for Information Packages (CSIP) forms the outermost layer. The general SIP, AIP and DIP specifications add respectively, submission, archiving and dissemination information to the CSIP specification. The third layer of the model represents specific content information type specifications, such as this 3D Heritage Model specification. Additional layers for business-specific specifications and local variant implementations of any specification can be added to suit the needs of the organisation.

<a name="fig2"></a>\

![Data Model Structure](/specification/figs/fig_2_data_model_structure.svg "Data Model Structure")

**Figure 2:** Data Model Structure
 
Every level in the data model structure inherits metadata entities and elements from the higher levels. In order to increase adoption, a flexible schema has been developed. This will allow for extension points where the schema in each layer can be extended to accommodate additional information on the next specific layer until, finally, the local implementation can add specific entities or metadata elements to satisfy specific local needs. Extension points can be implemented by:

•	Embedding foreign extension schemas (in the same way as supported by METS [http://www.loc.gov/standards/mets/] and PREMIS [http://www.loc.gov/standards/premis/]). These both support increasing the granularity of existing metadata elements by using more detailed data structures as well as adding new types of metadata;
•	Substituting metadata schemas for standards more appropriate for the local implementation. 
The structure allows the addition of more detailed requirements for metadata entities, for example, by:
•	Increasing the granularity of metadata elements by using more detailed data structures; or 
•	Adding local controlled vocabularies.

For consistency, design principles are reused between layers as much as possible.
