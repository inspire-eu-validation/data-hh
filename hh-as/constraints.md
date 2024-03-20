# Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following check shall be manually performed for every feature in the dataset:

* The [COD](#COD) attribute shall be provided only if the [diseaseMeasureType](#diseaseMeasureType) attribute of diseaseMeasure takes a value that represents mortality.

The following checks are automatically performed for every feature in the dataset:
* _Disease_ feature type:
  * At least one of [pathology](#pathology) and [COD](#COD) attributes must not be empty (OCL: inv:self.COD->Empty implies self.pathology-> notEmpty inv:self.pathology->Empty implies self.COD -> notEmpty).

* _EnvHealthDeterminantMeasure_ feature type:
  * An environmental health determinant measure shall be provided either as measure (attribute [measure](#measure)) or category of measure (attribute [category](#category)).


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-HH](./README.md#ref_TG_DS_HH) 5.3.2.1.2

**Test type**: Manual + Automated

**Notes** 

Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity       |Voidable
---------------------------------------------------------- | ------------------------------------- | ------------------|----------
COD <a name="COD"></a> | //schema-element(hh:Disease)/hh:COD/@xlink:href | 0..1 | No
pathology <a name="pathology"></a> | //schema-element(hh:Disease)/hh:pathology/@xlink:href | 0..1 | No
diseaseMeasureType <a name="diseaseMeasureType"></a> | //schema-element(hh:Disease)/hh:diseaseMeasure/hh:DiseaseMeasure/hh:diseaseMeasureType/@xlink:href | 1 | No
measure <a name="measure"></a> | //schema-element(hh:EnvHealthDeterminantMeasure)/hh:measure <br> //schema-element(hh:EnvHealthDeterminantNoiseMeasure)/hh:measure <br> //schema-element(hh:EnvHealthDeterminantConcentrationMeasure)/hh:measure | 0..1 | No
category <a name="category"></a> | //schema-element(hh:EnvHealthDeterminantMeasure)/hh:category/@xlink:href <br> //schema-element(hh:EnvHealthDeterminantNoiseMeasure)/hh:category/@xlink:href <br> //schema-element(hh:EnvHealthDeterminantConcentrationMeasure)/hh:category/@xlink:href | 0..1 | No
