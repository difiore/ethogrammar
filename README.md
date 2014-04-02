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

CHANGELOG

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

REMOVED FROM site
* projection

RENAMED WITHIN site
* datum (now zone)

REMOVED FROM point location
* projection (synonymous with datum)
* latitude
* longitude
* x coordinate
* y coordinate

ADDED TO point location
* verbatimCoordinates
* verbatimLatitude
* verbatimLongitude
* verbatimCoordinateSystem
* verbatimSRS

-->


### time

Definition:

tdwg:eventTime: The time or interval during which an Event occurred. Recommended best practice is to use an encoding scheme, such as ISO 8601:2004(E).

Notes:

The timestamp and its encoding should specify information including hour, minute, second, time zone, and DST.

Attributes:

* timestamp
* encoding

### date

Definition:

tdwg:eventDate: The date-time or interval during which an Event occurred. For occurrences, this is the date-time when the event was recorded. Not suitable for a time in a geological context. Recommended best practice is to use an encoding scheme, such as ISO 8601:2004(E).

Notes:

The datestamp and its encoding should specify information including month, day, and year.

Attributes:

* datestamp
* encoding

### spatial object

Definition:

A generic class encompassing positional information

Notes:

See dcterms:Location; for metadata to incorporate, see also tdwg:locationAccordingTo, tdwg:georeferencedBy, tdwg:georeferenceSources, tdwg:georeferenceRemarks, tdwg:georeferenceVerificationStatus

Attributes:

* type :: The type of spatial object, most often a point location or site.
	1. point location :: A location that is defined as a single point in space.
	2. site :: A location that is defined as an area in space
	3. other :: Miscellaneous class encompassing all other types of spatial data
* description :: A description specifying characteristics of the spatial object (suggest removal as both site and point location have their own description attributes)

### site

Definition:

A class of positional information in which the location is defined as an area in space.

Notes:

Attributes:

* country :: The name of the country or major administrative unit in which the Location occurs. Recommended best practice is to use a controlled vocabulary such as the Getty Thesaurus of Geographic Names (from tdwg:country)
* state :: A territorial and constitutional community forming part of a federal union [http://en.wikipedia.org/wiki/Federated_state]
* locality :: A local region, municipality, or community; equivalent to tdwg:verbatimLocality
* zone :: A zone defined under the Universal Transverse Mercator (UTM) coordinate system
* description :: Additional attributes describing the site; equivalent to tdwg:locationRemarks

### point location

Definition:

A class of positional information in which the location is defined as a single point in space.

Notes:

Attributes:

* datum :: A set of values used to define a specific geodetic system [http://en.wikipedia.org/wiki/Datum_(geodesy)]; see also tdwg:geodeticDatum
* altitude :: The elevation or range of elevation; see also tdwg:verbatimElevation, tdwg:minimumElevationInMeters, tdwg:maximumElevationInMeters, tdwg:verbatimDepth, tdwg:minimumDepthInMeters, tdwg:maximumDepthInMeters, tdwg:minimumDistanceAboveSurfaceInMeters, tdwg:maximumDistanceAboveSurfaceInMeters
* description :: Additional attributes describing the point location; equivalent to tdwg:locationRemarks
* collection method :: how the point location was determined; see also georeferenceProtocol
	1. GPS
	2. reference point
	3. etc.
* associated error :: See also tdwg:coordinatePrecision, tdwg:coordinateUncertaintyInMeters

### physical record

Definition:

Notes:

see also tdwg:materialSampleID (which includes original specimens but not derived media, measurements, etc.)

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

* family
* genus
* species
* higher level
* identified by

## Researcher and Logistics


### observer

Definition:

Notes:

Attributes:

* name
* sex
* date of birth
* affiliation
* age

### research group

Definition:

Notes:

Attributes:

* name
* member

### institution

Definition:

Notes:

Attributes:

* name
* address

### research project

Definition:

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

* amount
* currency
* receive date
* source
* expiry date

## Demography and Life History


### individual animal

Definition:

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

* group name
* date of formation
* date of dissolution
* parent group

### census

Definition:

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

* start time
* end time
* participant
* class of behavior

### participant

Definition:

Notes:

Attributes:

* individual animal
* role
	* actor
	* recipient
	* mutual
* location

### behavior sample

Definition:

Notes:

Attributes:

* observer
* date
* group
* subject
* behavior protocol
* unit of behavior

### ethogram

Definition:

Notes:

Attributes:

* research group
* class of behavior

### class of behavior

Definition:

Notes:

Attributes:

* name
* parent

### behavior protocol

Definition:

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

* tree
* date of measurement
* measurement
	* DBH
	* height
	* crown diameter
	* etc.

### phenology monitoring data

Definition:

Notes:

Attributes:

* tree
* date of monitoring
* monitored by
* score
* amount

### meteorological sample

Definition:

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

* drug name
* amount
* units
* time administered
* processing event

### physical observation

Definition:

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

* biological sample
* amount
* quality
* storage condition
* date made

### storage condition

Definition:

Notes:

Attributes:

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

Notes:

Attributes:

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

Notes:

Attributes:

* biological sample
* amount used
* protocol used
* extractor
* date extracted
* quantification

### lab protocol

Definition:

Notes:

Attributes:

* protocol name
* protocol author
* protocol publication date
* description

### result

Definition:

Notes:

Attributes:

* result type

### genotype

Definition:

Notes:

Attributes:

* locus
* allele 1
* allele 2
* etc.

### hormone level

Definition:

Notes:

Attributes:

* value
* units
* etc.

