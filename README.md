# Channel metadata files for UCB and USGS Menlo Park EEW systems

This repository stores:

* Channel metadata files for UCB and USGS Menlo Park EEW systems.
* Lists of station channels currently undergoing Station Acceptance.
* A script to filter station channels from the channel metadata files.

## Vocabulary

**Primary Channel File (PCF)**: The channel metadata file that is
available at:

http://www.ncedc.org/ftp/outgoing/stephane/eew/

This file is deployed to the EEW development systems.

**Station Acceptance**: Process whereby station channels are confirmed
to produce reliable data.

**Integration Channel File**: Version of the PCF with Phase II station
channels removed.  This file is deployed to the EEW integration systems.

**Production/Testing Channel File**: Version of the PCF with Phase I and
Phase II station channels removed.  This file is deployed to the EEW
production and testing systems.

## Assumptions

* We start with a clean Primary Channel File.
* All processes are done through GitHub or the USGS repository (TBD)

We plan to take the following steps:

* Clean up the existing channel metadata files to make new Primary
  Channel Files.  These are the versions that are deployed to the
  EEW development systems.

* Maintain two filter lists for each site (UCB and USGS Menlo Park):

  * Station channels in Phase I of the station acceptance process
  * Station channels in Phase II of the station acceptance process

* Maintain a script that can use the filter lists to make Integration
  Channel Files and Production/Testing Channnel Files according to the
  following criteria:

  * Station channels on the Phase II list are removed from the
    Integration Channel File
  * Station channels on the Phase I and Phase II lists are removed
    from the Production/Testing Channel File

* Maintain all three versions of the channel metadata files (Primary
  Channel File, Integration Channel File, and Production/Testing
  Channel File) with version control on the repository site of choice.

* Give the REI coordinator the opportunity to review a channel metadata
  file before it is deployed to EEW systems.

* Each time a ticket is submitted to graduate stations to Phase I or II
  of Station Acceptance, the ticket submitter directs the EEW operator
  to the repository where the appropriate version of the channel
  metadata file is located.  The EEW operator distributes the
  appropriate version of the channel metadata file to the appropriate
  EEW systems.

We still need to address how easy it would be to maintain a separate NN
list or keep the same system for now (ask Stephane his opinion).

