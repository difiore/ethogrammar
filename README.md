Ethogrammar: The Ethoinformatics Terms Dictionary
===========
Ethogrammar is the working title for the ontology being developed by the ethoinformatics project.

<!--

Search for:
(\t+?)(\w+)

Replace with:
\1* \2

-->

*Organized by domain*

## Universal`

<!--
REMOVED FROM time
* hour
* minute
* second
* time zone
* daylight savings time

REMOVED FROM date
* month
* day
* year
-->


### time

Definition:

Darwin Core *eventTime-2009-04-24*: The time or interval during which an Event occurred. Recommended best practice is to use an encoding scheme, such as ISO 8601:2004(E).

Attributes:

* timestamp
* encoding

### date

Definition:

Darwin Core *eventDate-2009-04-24*: The date-time or interval during which an Event occurred. For occurrences, this is the date-time when the event was recorded. Not suitable for a time in a geological context. Recommended best practice is to use an encoding scheme, such as ISO 8601:2004(E).

Attributes:

* datestamp
* encoding

### spatial object

Definition:

Attributes:

Notes:

* type
	Definition: blah blah blah
	* point location
		Definition: blah blah blah
	* site
	* other
* description

### site

Definition:

Attributes:

Notes:

* country
* state
* locality
* datum
* description
* projection

### point location

Definition:

Attributes:

Notes:

* latitude
* longitude
* x coordinate
* y coordinate
* datum
* altitude
* description
* collection method
	* GPS
	* reference point
	* etc.
* associated error
* projection

### physical record

Definition:

Attributes:

Notes:

* type
	* photo
	* video
	* palm prints
	* sound recording
	* dental cast
	* pressed plants
	* etc.

### measurement

Definition:

Attributes:

Notes:

* type
	* mass
	* morphometrics
	* temperature
	* etc.
* instrument
* value
* units
* details
	* landmarks
	* measurement period
	* etc.

### taxonomy

Definition:

Attributes:

Notes:

* family
* genus
* species
* higher level
* identified by

## Researcher and Logistics


### observer

Definition:

Attributes:

Notes:

* name
* sex
* date of birth
* affiliation
* age

### research group

Definition:

Attributes:

Notes:

* name
* member

### institution

Definition:

Attributes:

Notes:

* name
* address

### research project

Definition:

Attributes:

Notes:

* name
* start date
* end date
* description
* collaborating researcher
* collaborating research group
* permission
* product
* funding source

### product

Definition:

Attributes:

Notes:

* type
	* training
	* conference presentation
	* report
	* publication
	* local presentation
	* website
	* etc.
* description
* citation

### document

Definition:

Attributes:

Notes:

* type
	* MOU
	* collection permit
	* IACUC
	* import permit
	* export permit
	* research permit
	* IRB
	* Environmental Health and Safety
	* etc.
* issue date
* expiry date
* issuer

### award

Definition:

Attributes:

Notes:

* amount
* currency
* receive date
* source
* expiry date

## Demography and Life History


### individual animal

Definition:

Attributes:

Notes:

* name
* id code
* sex
* taxon
* photograph
* estimated date of birth
* dam
* sire
* individual age

### life history event

Definition:

Attributes:

Notes:

* individual animal
* date of event
* event type
	* natal dispersal
	* sexual maturity
	* disappearance
	* emigration
		* from group
	* immigration
		* to group
	* reproduction
		* individual animal
	* birth
		* natal group
	* death
		* cause of death
	* etc.

### group

Definition:

Attributes:

Notes:

* group name
* date of formation
* date of dissolution
* parent group

### census

Definition:

Attributes:

Notes:

* date recorded
* time recorded
* group
* taker
* composition
* type
	* group
	* subgroup

### physical state observation

Definition:

Attributes:

Notes:

* individual animal
* date of observation
* time of observation
* reproductive status
* health status
* body condition
* dominance rank

## Behavior

### unit of behavior

Definition:

Attributes:

Notes:

* start time
* end time
* participant
* class of behavior

### participant

Definition:

Attributes:

Notes:

* individual animal
* role
	* actor
	* recipient
	* mutual
* location

### behavior sample

Definition:

Attributes:

Notes:

* observer
* date
* group
* subject
* behavior protocol
* unit of behavior

### ethogram

Definition:

Attributes:

Notes:

* research group
* class of behavior

### class of behavior

Definition:

Attributes:

Notes:

* name
* parent

### behavior protocol

Definition:

Attributes:

Notes:

<!-- individual and group should both be prefixed by "focal" -->

* sampling rule
	* focal individual
	* focal group
	* behavior
	* ad libitium
* scheduling rule
	* instantaneous
	* continuous
* interval
* targeted duration
* ethogram
* research project

## Ecology and Environment


### tree

Definition:

Attributes:

Notes:

* taxonomy
* location
* date of death
* date first used
* marked by
* use
	* feeding
	* sleeping
	* resting
* collection

### ecological observation

Definition:

Attributes:

Notes:

* tree
* date of measurement
* measurement
	* DBH
	* height
	* crown diameter
	* etc.

### phenology monitoring data

Definition:

Attributes:

Notes:

* tree
* date of monitoring
* monitored by
* score
* amount

### meteorological sample

Definition:

Attributes:

Notes:

* date recorded
* time recorded
* recorded by
* measurement
	* temperature
	* humidity
	* precipitation
	* etc.

### other patch

Definition:

Attributes:

Notes:

* marked by
* location
* type
	* mineral lick
	* THV
	* water hole
	* sleeping tree
	* etc.
* use
	* feeding
	* water
	* shelter
	* sleeping
	* geophagy
	* etc.
* date first used
* ecological observation

### indirect sign

Definition:

Attributes:

Notes:

* type of sign
	* print
	* human activity
	* human detritus
	* food remains
	* sleeping nests
	* cavities
* time sign noted
* date sign noted
* taxonomy
* probable age of sign
* sign location
* seen by

## Captures and Samples


### capture event

Definition:

Attributes:

Notes:

* date
* method
	* trapping
	* darting
	* etc.
* observer
* site
* location
* start time
* end time
* habitat description
* weather description
* captured animal

### processing event

Definition:

Attributes:

Notes:

* start time
* observer
* site
* location
* capture event
* individual animal
* end time
* sedation method
* capture time
* release time

### dose

Definition:

Attributes:

Notes:

* drug name
* amount
* units
* time administered
* processing event

### physical observation

Definition:

Attributes:

Notes:

* collector
* time of observation
* subject
* measurement
* processing event
* date of observation
* injuries or wounds noted
* physical record
* reproductive status
* health status
* body condition
* parity
* scars and diagnostic features
* ectoparasites

### dental observation

Definition:

Attributes:

Notes:

* tooth type
* set
	* deciduous
	* permanent
* arcade
	* upper
	* lower
* side
	* left
	* right
* number in series
* wear
* eruption
* presence-absence
	* present
	* absent
* physical observation

### biological sample

Definition:

Attributes:

Notes:

* collector
* collection site
* collection date
* collection time
* individual animal
* processing event
* location
* type
	* serum
	* hair
	* scent gland swab
	* oral swab
	* vaginal swab
	* feces
	* blood
	* urine
	* milk
	* ejaculate
	* ectoparasites
	* whole blood
	* nails
	* buccal cells
	* blood cells
	* etc.
* amount
* estimated age of sample
* quality
* storage condition

### subsample

Definition:

Attributes:

Notes:

* biological sample
* amount
* quality
* storage condition
* date made

### storage condition

Definition:

Attributes:

Notes:

* medium
	* quantity
	* type
* container
	* type
	* size
* start time
* end time
* temperature

## Labwork


### experiment

Definition:

Attributes:

Notes:

* experimenter
* type
	* PCR
	* qPCR
	* NGS
	* WGA
	* sequencing
	* RNA
	* etc.
* extraction
* date run
* location
* result

### extraction

Definition:

Attributes:

Notes:

* biological sample
* amount used
* protocol used
* extractor
* date extracted
* quantification

### lab protocol

Definition:

Attributes:

Notes:

* protocol name
* protocol author
* protocol publication date
* description

### result

Definition:

Attributes:

Notes:

* result type

### genotype

Definition:

Attributes:

Notes:

* locus
* allele 1
* allele 2
* etc.

### hormone level

Definition:

Attributes:

Notes:

* value
* units
* etc.

