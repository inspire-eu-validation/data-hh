# Human Health and Safety theme-specific requirements

**Purpose**: Verify that the features provided in the dataset adhere to the theme-specific requirements specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following checks shall be manually performed for every feature of the relevant feature types in the dataset (if present):

* Statistical information on the spatial data theme Human Health and Safety must refer to spatial objects as defined in the spatial data theme Statistical Units.
* Where possible, the ICDValue code list shall be used to identify the disease name.
* Raw measurement data shall be based on ISO/TS 19103:2005.
* Health determinant statistical data shall be modelled as health statistical data characterized by a measurement value based on ISO/TS 19103:2005 and a statistical aggregation method.
* Health determinant coverages shall be represented using the spatial object types defined in Section 6 of Annex I. For continuous coverages, a subtype of the CoverageByDomainAndRange class shall be used whose domain is restricted to measurement values based on ISO/TS 19103:2005.


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-HH](./README.md#ref_TG_DS_HH) 5.3.1.2.1.; 5.3.1.2.2.; 5.3.1.2.3.

**Test type**: Manual

**Notes** 

## Messages


## Contextual XPath references

