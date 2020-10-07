# Code lists

**Purpose**: Verify that code lists extensions can be accessed.

**Prerequisites**

**Test method**

* Verify that any code list extensions are publicly accessible via HTTP, i.e. inspect extensible code list values property elements. If a reference (@xlink:href) has a value that does not start with http://inspire.ec.europa.eu/codelist/, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following empty code lists:

* [ChemicalValue](#ChemicalValue): http://inspire.ec.europa.eu/codelist/ChemicalValue

* [ComponentTypeValue](#ComponentTypeValue):  http://inspire.ec.europa.eu/codelist/ComponentTypeValue

* [DiseaseMeasureTypeValue](#DiseaseMeasureTypeValue): http://inspire.ec.europa.eu/codelist/DiseaseMeasureTypeValue

* [EnvHealthDeterminantTypeValue](#EnvHealthDeterminantTypeValue): http://inspire.ec.europa.eu/codelist/EnvHealthDeterminantTypeValue

* [GeneralHealthTypeValue](#GeneralHealthTypeValue): http://inspire.ec.europa.eu/codelist/GeneralHealthTypeValue

* [HealthServicesTypeValue](#HealthServicesTypeValue): http://inspire.ec.europa.eu/codelist/HealthServicesTypeValue

* [MatrixValue](#MatrixValue):  http://inspire.ec.europa.eu/codelist/MatrixValue

* [MediaTypeValue](#MediaTypeValue): http://inspire.ec.europa.eu/codelist/MediaTypeValue

* [NoiseSourceTypeValue](#NoiseSourceTypeValue): http://inspire.ec.europa.eu/codelist/NoiseSourceTypeValue

* [StatisticalAggregationMethodValue](#StatisticalAggregationMethodValue): http://inspire.ec.europa.eu/codelist/StatisticalAggregationMethodValue


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression      |Multiplicity   |Voidable
---------------------------------------------------------- | -----------------------|---------------|---------------------------------
TO BE COMPLETED
