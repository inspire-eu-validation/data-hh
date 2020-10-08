# Feature references

**Purpose**: Verify that referenced features can be retrieved.

**Prerequisites**

**Test method**

* Verify that any feature reference in an association role is publicly accessible via HTTP, i.e. inspect all relevant properties. If a reference (@xlink:href) has a value that starts with "#", verify that an element with a `gml:id` attribute with the referenced identifier exists in the same document. If the reference starts with "http", verify that a HTTP GET request to the URI retrieves an XML document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following association roles:

* [BiomarkerThematicMetadata.describedBy](#describedBy): hh:Biomarker
* [Biomarker.aggregationUnit](#aggregationUnit1): su:StatisticalUnit
* [Disease.aggregationUnit](#aggregationUnit2): su:StatisticalUnit
* [GeneralHealthStatistics.aggregationUnit](#aggregationUnit3): su:StatisticalUnit
* [HealthServicesStatistic.aggregationUnit](#aggregationUnit4): su:StatisticalUnit
* [EnvHealthDeterminantStatisticalData.aggregationUnit](#aggregationUnit5): su:StatisticalUnit


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                         |  XPath expression    | Multiplicity    | Voidable
------------------------------------ | ---------------------|-----------------|------------
BiomarkerThematicMetadata.describedBy <a name ="describedBy"></a>	| //schema-element(hh:Biomarker)/hh:refersTo/hh:BiomarkerThematicMetadata/hh:describedBy/@xlink:href | 1..\* | No
Biomarker.aggregationUnit <a name ="aggregationUnit1"></a>	| //schema-element(hh:Biomarker)/hh:aggregationUnit/@xlink:href | 1 | No
Disease.aggregationUnit <a name ="aggregationUnit2"></a>	| //schema-element(hh:Disease)/hh:aggregationUnit/@xlink:href | 1 | No
GeneralHealthStatistics.aggregationUnit <a name ="aggregationUnit3"></a>	| //schema-element(hh:GeneralHealthStatistics)/hh:aggregationUnit/@xlink:href | 1 | No
HealthServicesStatistic.aggregationUnit <a name ="aggregationUnit4"></a>	| //schema-element(hh:HealthServicesStatistic)/hh:aggregationUnit/@xlink:href | 1 | No
EnvHealthDeterminantStatisticalData.aggregationUnit <a name ="aggregationUnit5"></a>	| //schema-element(hh:EnvHealthDeterminantStatisticalData)/hh:aggregationUnit/@xlink:href | 1 | No