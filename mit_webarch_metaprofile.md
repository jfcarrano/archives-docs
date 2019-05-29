# MIT Libraries Department of Distinctive Collections Web Archiving Metadata Application Profile
## Contents
| Field                                                       |                                        |
| ----------------------------------------------------------- | -------------------------------------- |
| [Collector](#collector)                                     | Required                               |
| [Title](#title)                                             | Required                               |
| [Identifier_CollectionID](#identifier_collectionid)         | Required                               |
| [Identifier_URL](#identifier_url)                           | Required                               |
| [Date](#date)                                               | Required                               |
| [Creator](#creator)                                         | Required (if known)                    |
| [Description](#description)                                 | Required                               |
| [Appraisal_Information](#appraisal_information)             | Required                               |
| [Conditions_Governing_Access](#conditions_governing_access) | Required                               |
| [Rights](#rights)                                           | Required                               |
| [Language](#language)                                       | Required                               |
| [Relation](#relation)                                       | Required                               |
| [Extent](#extent)                                           | Optional                               |
| [Source_of_Description](#source_of_description)             | Optional (strongly encouraged)         |
| [Contributor](#contributor)                                 | Optional (required if creator unknown) |
| [Genre/Form](#genreform)                                    | Optional                               |
| [Subject](#subject)                                         | Optional                               |

Note: this information largely refers to seed-level description. MIT collections in Archive-It are in two large groupings and are already fully described at that level. The fields used there generally followed this guidance.

## Collector
|                         | Information                                                                                    |
| ----------------------- | ---------------------------------------------------------------------------------------------- |
| Definition              | The organization responsible for curation and stewardship of an archived website or collection |
| Standard usage for DDC | Massachusetts Institute of Technology. Libraries. Department of Distinctive Collections   |
| Standards               | OCLC data dictionary element: Collector, DACS Chapter: 2.2                                     |
| Note                    | Required                                                                                       |

| Crosswalks  |                                                     |
| ----------- | --------------------------------------------------- |
| Dublin Core | Contributor                                         |
| EAD         | ```<repository>```                                  |
| MARC 21     | 583 subfield h, 710, 852 subfield a, 852 subfield b |
| MODS        | ```<location><physicalLocation>```                  |
| schema.org  | schema:OwnershipInfo                                |

## Title
|                         | Information                                                                                                                                                                                                                                                                       |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | The name by which an archived website or collection is known                                                                                                                                                                                                                      |
| Standard usage for DDC | The Aga Khan Program for Islamic Architecture at the Massachusetts Institute of Technology (AKPIA@MIT) website                                                                                                                                                                    |
| Standards               | OCLC data dictionary element: Title, DACS: 2.3, RDA: 2.3                                                                                                                                                                                                                          |
| Note                    | Required. Because we have very broad collections in Archive-It, this most often refers to the seed title. Apply the type of website to the end of the title to allow for easy differentiation between sites. For instance, “blog” or “Instagram” at the end if separate captures. |

| Crosswalks  |                                                                             |
| ----------- | --------------------------------------------------------------------------- |
| Dublin Core | Title                                                                       |
| EAD         | ```<unittitle>```                                                           |
| MARC 21     | 245, 246, 730, 740                                                          |
| MODS        | ```<titleInfo>```,```<title>```,```<titleInfo type=“alternative”><title>``` |
| schema.org  | schema:name                                                                 |
## Identifier_CollectionID
|                         | Information                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Definition              | A unique identifier for the for the collection being described                                                            |
| Standard usage for DDC | The DDC collection identifier such as MC-#### for manuscript collections or AC-#### for archival collections             |
| Standards               | DACS Chapter: 2.1                                                                                                         |
| Note                    | Required. Repeatable if the collection falls under multiple collections, for instance a center that is interdisciplinary. |

| Crosswalks  |                    |
| ----------- | ------------------ |
| Dublin Core | Identifier         |
| EAD         | ```<unitid>```     |
| MARC 21     | 090                |
| MODS        | ```<identifier>``` |
| schema.org  | schema:identifier  |
## Identifier_URL
|                         | Information                                                                                                                                                                                                                                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Internet address for an archived website or collection                                                                                                                                                                                                                                                            |
| Standard usage for DDC | The seed URL, for instance https://economics.mit.edu                                                                                                                                                                                                                                                              |
| Note                    | Required. Seed URL will be added automatically in Archive-It. Used in ArchivesSpace in a digital object as the identifier. Can be used in Archive-It for URL’s for where the seed was previously hosted. Create a custom field called “previous_URL”, for instance previous_URL: http://web.mit.edu/economics/www |

| Crosswalks  |                    |
| ----------- | ------------------ |
| Dublin Core | Identifier         |
| EAD         | ```<dao href= >``` |
| MARC 21     | 856 subfield u     |
| MODS        | ```<url>```        |
| schema.org  | schema:url         |
## Date
|                         | Information                                                                                                                                                                                                                       |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | A single date or span of dates associated with the capture of an archived website or collection                                                                                                                     |
| Standard usage for DDC | 2018-07-04 – ongoing                                                                                                                                                                                                              |
| Standards               | OCLC data dictionary element: Date, DACS Chapter: 2.4                                                                                                                                                                              |
| Note                    | Required. This will automatically be generated in Archive-It. Mostly used at the collection level or in ArchivesSpace and should at least list the date when crawling started. If seed becomes inactive, list end date there too. |

| Crosswalks  |                                                                                 |
| ----------- | ------------------------------------------------------------------------------- |
| Dublin Core | Date                                                                            |
| EAD         | ```<unitdate>```                                                                |
| MARC 21     | 008 bytes 07-14, 245 subfield f, 260 subfield c, 264 subfield c, 583 subfield c |
| MODS        | ```<dateCaptured>```                                                            |
| schema.org  | schema:dateCreated                                                              |
## Creator
|                         | Information                                                                                                                                                                                                                                                                                                                                                                       |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Use this element for an organization or person when you are certain of the principal responsibility for having created the intellectual content                                                                                                                                                                                                                                   |
| Standard usage for DDC | The creator’s name, for instance: Massachusetts Institute of Technology. Computer Science and Artificial Intelligence Laboratory                                                                                                                                                                                                                                                  |
| Standards               | OCLC data dictionary element: Creator, DACS Chapter: 2.6, RDA Section 3                                                                                                                                                                                                                                                                                                           |
| Note                    | Required if known. Repeatable. If possible, use the agent name listed in ArchivesSpace. If they do exist there, use the VIAF and the LC Name Authority File when filling in a name. If one does not exist, derive one that follows LCNAF guidelines. In case of doubt, use Contributor for creators that may not have principal responsibility for creating intellectual content. |

| Crosswalks  |                                                                                            |
| ----------- | ------------------------------------------------------------------------------------------ |
| Dublin Core | Creator                                                                                    |
| EAD         | ```<origination><persname>```, ```<origination><corpname>```, ```<origination><famname>``` |
| MARC 21     | 100, 110, 700, 710                                                                         |
| MODS        | ```<creator>```                                                                            |
| schema.org  | schema:creator                                                                             |
## Description
|                         | Information                                                                                                                                    |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | One or more notes explaining the content, context, and other aspects of an archived website or collection                                      |
| Standard usage for DDC | Briefly describe the scope and content of the collection or seed. Include what the page(s) is about and some information about the creator(s). |
| Standards               | OCLC data dictionary element: Description, DACS Chapter: 3.1                                                                                   |
| Note                    | Required                                                                                                                                       |

| Crosswalks  |                                                                            |
| ----------- | -------------------------------------------------------------------------- |
| Dublin Core | Description                                                                |
| EAD         | ```<abstract>```, ```<accruals>```, ```<bioghist>```, ```<scopecontent>``` |
| MARC 21     | 500, 505, 520, 540, 541, 545, 555, 561, 584                                |
| MODS        | ```<abstract>```, ```<note>```                                             |
| schema.org  | schema:description                                                         |
## Appraisal_Information
|                         | Information                                                                                                                                                                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | This element provides information about the rationale for appraisal decisions                                                                                                                                                                                             |
| Standard usage for DDC | Provide a reason why the website seed is being crawled and seed scoping decisions regarding what level of crawl and blocking hosts etc. After describing seed scoping decisions append: “If you would like to see the full scoping details, please contact the collector” |
| Standards               | OCLC data dictionary element: Description, DACS Chapter: 5.3                                                                                                                                                                                                              |
| Note                    | Required. Write these in a human readable format in general categories of scoping rules.                                                                                                                                                                                  |

| Crosswalks  |                                    |
| ----------- | ---------------------------------- |
| Dublin Core | Description                        |
| EAD         | ```<appraisal>```, ```<acqinfo>``` |
| MARC 21     | 583                                |
| MODS        | ```<abstract>```, ```<note>```     |
| schema.org  | schema:description                 |
## Conditions_Governing_Access
|                         | Information                                                                                                                                                                                                                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Statement of conditions that restrict user access to the archived content                                                                                                                                                                                                                                                 |
| Standard usage for DDC | For MIT records, note any restrictions based on the [Institute Records Access Policy](https://libraries.mit.edu/archives/managing/policy-access.html). For manuscript collections, note any restrictions based on the donor agreement for new collections or the access note in the finding aid for existing collections. |
| Standards               | OCLC data dictionary element: Rights, DACS Chapter: 4.1                                                                                                                                                                                                                                                                   |
| Note                    | Required                                                                                                                                                                                                                                                                                                                  |

| Crosswalks  |                                            |
| ----------- | ------------------------------------------ |
| Dublin Core | Rights                                     |
| EAD         | ```<accessrestrict>```                     |
| MARC 21     | 506                                        |
| MODS        | ```<accessCondition>```                    |
| schema.org  | schema:license, schema:isAccessibleForFree |
## Rights
|                         | Information                                                                                                                                                                              |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Standardized statement of permissions for re-use granted by intellectual property law or other legal agreements                                                                          |
| Standard usage for DDC | Insert standard rights statement for archival or manuscript collection. Once the guidance from MIT Libraries is available, use the applicable rights statement from rightsstatements.org |
| Standards               | OCLC data dictionary element: Rights, DACS Chapter: 4.1                                                                                                                                  |
| Note                    | Required                                                                                                                                                                                 |

| Crosswalks  |                                            |
| ----------- | ------------------------------------------ |
| Dublin Core | Rights                                     |
| EAD         | ```<userestrict>```                        |
| MARC 21     | 540, 542                                   |
| MODS        | ```<accessCondition>```                    |
| schema.org  | schema:license, schema:isAccessibleForFree |
## Language
|                         | Information                                                                                                 |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| Definition              | The language(s) of the archived content, including visual and audio resources with language components      |
| Standard usage for DDC | English                                                                                                     |
| Standards               | OCLC data dictionary element: Language, DACS Chapter: 4.5                                                   |
| Note                    | Required. Repeatable field. Use again if multiple languages. Use language as listed in ArchivesSpace field. |

| Crosswalks  |                                |
| ----------- | ------------------------------ |
| Dublin Core | Language                       |
| EAD         | ```<langmaterial><language>``` |
| MARC 21     | 008 bytes 35-37, 041, 546      |
| MODS        | ```<language>```               |
| schema.org  | schema:inLanguage              |
## Relation
|                         | Information                                                                                                                                                                         |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | The archival collection which the collection belongs                                                                                                                                |
| Standard usage for DDC | The collection name such as, Massachusetts Institute of Technology, Aga Khan Program for Islamic Architecture records                                                               |
| Standards               | OCLC data dictionary element: Relation                                                                                                                                              |
| Note                    | Required. In Archive-It, we provide this information through the Related Archival Materials plug-in. In ArchivesSpace the Archival and Digital Object will be linked to a resource. |

| Crosswalks  |                                                                  |
| ----------- | ---------------------------------------------------------------- |
| Dublin Core | Contributor                                                      |
| EAD         | ```<unittitle>``` (of parent component), ```<relatedmaterial>``` |
| MARC 21     | 580, 730, 773, 787                                               |
| MODS        | ```<relatedItem>```                                              |
## Extent
|                         | Information                                                       |
| ----------------------- | ----------------------------------------------------------------- |
| Definition              | An indication of the size of an archived website or collection.   |
| Standard usage for DDC | 1 archived website                                                |
| Standards               | DACS Chapter: 2.5                                                 |
| Note                    | Optional field. More appropriate in ArchivesSpace than Archive-It |

| Crosswalks  |                                     |
| ----------- | ----------------------------------- |
| Dublin Core | Format                              |
| EAD         | ```<physdesc><extent>```            |
| MARC 21     | 300, 347                            |
| MODS        | ```<physicalDescription><extent>``` |
| schema.org  | schema:description                  |
## Source_of_Description
|                         | Information                                                                                                                                |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Definition              | Information about the gathering or creation of the metadata itself, such as sources of data or the date on which source data was obtained. |
| Standard usage for DDC | Description by <name> based on archived web page captured Sept. 22, 2016; title from title screen (viewed Oct. 27, 2016)                   |
| Standards               | DACS Chapter: 7.1.8                                                                                                                        |
| Note                    | Optional field (though strongly encouraged)                                                                                                |

| Crosswalks  |                                                      |
| ----------- | ---------------------------------------------------- |
| Dublin Core | Description                                          |
| EAD         | ```<processinfo>```                                  |
| MARC 21     | 588                                                  |
| MODS        | ```<note>```                                         |
| schema.org  | schema:description, schema:disambiguatingDescription |
## Contributor
|                         | Information                                                                                                                                                                                                                                                                           |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | An organization or person secondarily responsible for the content of an archived website or collection                                                                                                                                                                                |
| Standard usage for DDC | The contributor name, such as: Massachusetts Institute of Technology. Computer Science and Artificial Intelligence Laboratory                                                                                                                                                         |
| Standards               | OCLC Data Dictionary Element: Contributor, RDA Section 3, RDA 20, 22                                                                                                                                                                                                                  |
| Note                    | Optional, required if creator unknown. Repeatable field. If possible use, the agent name listed in ArchivesSpace. If it does not do exist there, use the VIAF and the LC Name Authority File when filling in a name. If one does not exist, derive one that follows LCNAF guidelines. |

| Crosswalks  |                                                                                                  |
| ----------- | ------------------------------------------------------------------------------------------------ |
| Dublin Core | Contributor                                                                                      |
| EAD         | ```<controlaccess><persname>```, ```<controlaccess><corpname>```, ```<controlaccess><famname>``` |
| MARC 21     | 700                                                                                              |
| MODS        | ```<name>```                                                                                     |
| schema.org  | schema:contributor                                                                               |
## Genre/Form
|                         | Information                                                                                                                                      |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Definition              | A term specifying the type of content in an archived website or collection                                                                       |
| Standard usage for DDC | Websites, Department website, News article, etc.                                                                                                 |
| Note                    | Optional field. Use the genre/form as they exist in ArchivesSpace. If not there, use one from an appropriate authority such as the LCGFT or AAT. |

| Crosswalks  |                                  |
| ----------- | -------------------------------- |
| Dublin Core | Type                             |
| EAD         | ```<controlaccess><genreform>``` |
| MARC 21     | 655                              |
| MODS        | ```<genre>```                    |
| schema.org  | schema:genre                     |
## Subject
|                         | Information                                                                                                                                                                              |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Definition              | Primary topic(s) describing the content of an archived website or collection                                                                                                             |
| Standard usage for DDC | One or more subjects that describe the content. Such as 'Computers'                                                                                                                      |
| Note                    | Optional field. If possible, use a subject listed in ArchivesSpace. If no subject, use a Subject Heading listed in FAST. If one does not exist, derive one that follows LCSH guidelines. |

| Crosswalks  |                                                                           |
| ----------- | ------------------------------------------------------------------------- |
| Dublin Core | Subject                                                                   |
| EAD         | ```<controlaccess>```                                                     |
| MARC 21     | 600, 610, 611, 630, 647, 648, 650, 651, 653, 654, 656, 657, 658, 662, 69x |
| MODS        | ```<subject>```                                                           |
| schema.org  | schema:about                                                              |

## Sources

Most elements taken from the [University of Virginia Library Web Archiving Metadata Application Profile](https://docs.google.com/document/d/1M5kTUtUjob7YB7MpEd_Jl5lRsuZprxNZQZ6rELmJjeE/edit) and the OCLC [“Decriptive Metadata for Web Archiving”](https://www.oclc.org/research/publications/2018/oclcresearch-descriptive-metadata.html) report. In cases where additional fields were added the relevant standards and crosswalks are cited. Thanks to Elizabeth England, Eric Hanson, and Amy Wickner for feedback and suggestions.
