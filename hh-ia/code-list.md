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

* [MeasureCategoryTypeValue](#MeasureCategoryTypeValue): http://inspire.ec.europa.eu/codelist/MeasureCategoryTypeValue


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)

**Test type**: Automated

**Notes**

The ComponentTypeValue <a name="ComponentTypeValue"></a> codelist is abstract and it should be specilized by data providers. They may use the values specified in the INSPIRE Technical Guidance document on Human Health and Safety, in particular for components related to ground water quality, lake water quality, river water quality, ambient air quality and bathing water quality. The related attribute, i.e. "component" element in the UomConcentration type is not fully implemented in the xsd, so, at the moment, the check for this codelist is not implemented.

For the MediaTypeValue <a name="MediaTypeValue"></a> codelist data providers may use the values specified in the INSPIRE Technical Guidance document on Human Health and Safety. The related attribute, i.e. "media" element in the UomConcentration type is not fully implemented in the xsd, so, at the moment, the check for this codelist is not implemented.

For the NoiseSourceTypeValue <a name="NoiseSourceTypeValue"></a> codelist the related attribute, i.e. "source" element in the UomNoise type is not fully implemented in the xsd, so, at the moment, the check for this codelist is not implemented.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression      |Multiplicity   |Voidable
---------------------------------------------------------- | -----------------------|---------------|---------------------------------
ChemicalValue <a name="ChemicalValue"></a> | //schema-element(hh:Biomarker)/hh:biomarkerName/hh:BiomarkerType/hh:chemical/@xlink:href | 1 | No
ComponentTypeValue <a name="ComponentTypeValue"></a> | //schema-element(hh:EnvHealthDeterminantConcentrationMeasure)/hh:component/@xlink:href | 1 | No
DiseaseMeasureTypeValue <a name="DiseaseMeasureTypeValue"></a> | //schema-element(hh:Disease)/hh:diseaseMeasure/hh:DiseaseMeasure/hh:diseaseMeasureType/@xlink:href | 1 (1..\* for the parent) | No
EnvHealthDeterminantTypeValue <a name="EnvHealthDeterminantTypeValue"></a> | //schema-element(hh:EnvHealthDeterminantMeasure)/hh:type/@xlink:href <br> //schema-element(hh:EnvHealthDeterminantConcentrationMeasure)/hh:type/@xlink:href <br> //schema-element(hh:EnvHealthDeterminantNoiseMeasure)/hh:type/@xlink:href <br> //schema-element(hh:EnvHealthDeterminantStatisticalData)/hh:type/@xlink:href | 1 | No
GeneralHealthTypeValue <a name="GeneralHealthTypeValue"></a> | //schema-element(hh:GeneralHealthStatistics)/hh:generalHealthName/@xlink:href | 1 | No
HealthServicesTypeValue <a name="HealthServicesTypeValue"></a> | //schema-element(hh:HealthServicesStatistic)/hh:healthServiceType/@xlink:href | 1 | No
MatrixValue <a name="MatrixValue"></a> | //schema-element(hh:Biomarker)/hh:biomarkerName/hh:BiomarkerType/hh:matrix/@xlink:href | 1 | No
MediaTypeValue <a name="MediaTypeValue"></a> | //schema-element(hh:EnvHealthDeterminantConcentrationMeasure )/hh:media/@xlink:href | 1 | No
NoiseSourceTypeValue <a name="NoiseSourceTypeValue"></a> | //schema-element(hh:EnvHealthDeterminantNoiseMeasure )/hh:source/@xlink:href | 1 | No
StatisticalAggregationMethodValue <a name="StatisticalAggregationMethodValue"></a> | //schema-element(hh:EnvHealthDeterminantStatisticalData)/hh:statisticalMethod/@xlink:href | 1 | No
MeasureCategoryTypeValue <a name="MeasureCategoryTypeValue"></a> | //schema-element(hh:EnvHealthDeterminantMeasure)/hh:category/@xlink:href <br> //schema-element(hh:EnvHealthDeterminantConcentrationMeasure)/hh:category/@xlink:href <br> //schema-element(hh:EnvHealthDeterminantNoiseMeasure)/hh:category/@xlink:href | 0..1 | No
