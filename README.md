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

## Universal

<!--
	REMOVED FROM time
	* hour
	* minute
	* second
-->

* time
	* timestamp
	* encoding
	* time zone
	* daylight savings time
* date
	* month
	* day
	* year
* spatial object
	* type
		* point location
		* site
		* other
	* description
* site
	* country
	* state
	* locality
	* datum
	* description
	* projection
* point location
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
* physical record
	* type
		* photo
		* video
		* palm prints
		* sound recording
		* dental cast
		* pressed plants
		* etc.
* measurement
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
* taxonomy
	* family
	* genus
	* species
	* higher level
	* identified by

## Researcher and Logistics

* observer
	* name
	* sex
	* date of birth
	* affiliation
	* age
* research group
	* name
	* member
* institution
	* name
	* address
* research project
	* name
	* start date
	* end date
	* description
	* collaborating researcher
	* collaborating research group
	* permission
	* product
	* funding source
* product
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
* document
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
* award
	* amount
	* currency
	* receive date
	* source
	* expiry date

## Demography and Life History

* individual animal
	* name
	* id code
	* sex
	* taxon
	* photograph
	* estimated date of birth
	* dam
	* sire
	* individual age
* life history event
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
* group
	* group name
	* date of formation
	* date of dissolution
	* parent group
* census
	* date recorded
	* time recorded
	* group
	* taker
	* composition
	* type
		* group
		* subgroup
* physical state observation
	* individual animal
	* date of observation
	* time of observation
	* reproductive status
	* health status
	* body condition
	* dominance rank

## Behavior

* unit of behavior
	* start time
	* end time
	* participant
	* class of behavior
* participant
	* individual animal
	* role
		* actor
		* recipient
		* mutual
	* location
* behavior sample
	* observer
	* date
	* group
	* subject
	* behavior protocol
	* unit of behavior
* ethogram
	* research group
	* class of behavior
* class of behavior
	* name
	* parent
* behavior protocol
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

* tree
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
* ecological observation
	* tree
	* date of measurement
	* measurement
		* DBH
		* height
		* crown diameter
		* etc.
* phenology monitoring data
	* tree
	* date of monitoring
	* monitored by
	* score
	* amount
* meteorological sample
	* date recorded
	* time recorded
	* recorded by
	* measurement
		* temperature
		* humidity
		* precipitation
		* etc.
* other patch
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
* indirect sign
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

* capture event
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
* processing event
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
* dose
	* drug name
	* amount
	* units
	* time administered
	* processing event
* physical observation
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
* dental observation
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
* biological sample
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
* subsample
	* biological sample
	* amount
	* quality
	* storage condition
	* date made
* storage condition
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

* experiment
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
* extraction
	* biological sample
	* amount used
	* protocol used
	* extractor
	* date extracted
	* quantification
* lab protocol
	* protocol name
	* protocol author
	* protocol publication date
	* description
* result
	* result type
* genotype
	* locus
	* allele 1
	* allele 2
	* etc.
* hormone level
	* value
	* units
	* etc.

