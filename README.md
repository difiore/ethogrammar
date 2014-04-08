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

Material record that is stored physically or digitally. 

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

Hierarchical classification of individuals.

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

Individual taking the recordings. 

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

Output of a project or specific study. 

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

Grants that used to fund the project. 

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

Animal observed for data collection.

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

Cluster of individuals that maintain social (affiliative and agonistic) interactions in space and time. 

Notes:

Social interactions between individuals in the group cannot be exclusively agonistic. 

Attributes:

* group name
* date of formation
* date of dissolution
* parent group

### census

Definition:

Number of individuals in a specific area observed for estimation of population or group size. 

Notes:

Attributes:

* date recorded
* time recorded
* group
* taker
* composition
* method
	* transect
	* plot
	* etc
* type
	* group
	* subgroup

### physical state observation

Definition:

Assessment of physical traits of an individual.

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

Definition: An instance of behavior as specified in the ethogram.

Notes:

Attributes:

* start time
* end time
* participant
* class of behavior

### participant

Definition:

Non-focal animal involved in a social interaction with the focal animal. 

COMMENT: Since all behavior samples do not necessarily involve a focal animal (because a behavior sample can have 
multiple individuals or even a particular behavior as its subject, according to the “sampling rule”), maybe this
definition should be revised? An alternative definition could be:

Any animal involved in a social interaction with the sample's subject.

Notes:

Attributes:

* individual animal
* role
	Definition:
	The part that an individual plays in a social interaction.

	* actor
	* recipient
	* mutual
* location

### behavior sample

Definition: A record of a subject’s behavior, or linked records of behavior made over a specific time span.

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

Detailed description of typical behaviors observed in a species or in the study group.

Notes:

Attributes:

* research group
* class of behavior

### class of behavior

Definition: A group of several related types of behavior.

Notes:

Attributes:

* name
Definition: Denotative of a specific behavior.

* parent

### behavior protocol

Definition: The set of detailed instructions specifying how behavioral data for a particular research project are 
collected.

Notes:

Attributes:

<!-- individual and group should both be prefixed by "focal" -->

* sampling rule
Definition: Determines the subject of a behavior sample, whether an individual or a set of individuals, or a specific 
behavior of interest.
	* focal individual
	* focal group
	* behavior
	* ad libitium
	
* scheduling rule
Definition: The temporal span over which the subjects’ behavior is sampled. Instantaneous samples represent a snapshot 
in time with negligible duration, whereas continuous samples have a duration.
	* instantaneous
	* continuous
	
* interval
Definition: Time between two consecutive instantaneous samples.

* targeted duration
A predetermined length of time over which the study subject(s) is/are to be observed, if possible.

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
	* leaves
	* fruits
	* seeds
	* nutritional

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
* recording instrument
	* name
	* model
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

Evidence of behavioral activity that was not observed by the researcher. 

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

Amount and concentration of drug used to sedate an animal. 

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

Biological material from an animal that can be collected by the researcher. 

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

Treatment of a biological sample for analysis. 

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

DNA isolation from a biological sample.

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

Detailed instructions on how to proceed for the analysis of biological samples.

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

