# Welcome to Quaff

Quaff is utility to import data from Canvas LMS, into Q Gradebook (Aequitas).
The prevents teachers from having to double enter data.  

## Overview of how Quaff Works

The Quaff can be run from the command line for testing.  
In productions, it is run as a scheduled task.
Most configuration is via the config file.
There are also command line switches.

### Workflow
Quaff looks for a CVS extract exported from Canvas.  
It copies this file to a local working directory.
The local copy is filtered and parsed to include current semester data.

Quaff checks to make sure that course gradebooks have been set up.
If not, it sends a reminder notification to the teacher and school.
(Data for courses w/o gradebooks is not processed further.)

Quaff attempts to match assignments in Canvas and Q by name.
If a Canvas assignment doesn't exist in Q Gradebook, the missing assigment is created.
It then adds/updates assignment score.

At the end, the extract file is compressed and archived.

### Outputs
The utility updates Q Gradebook data.
It compresses and archives the vendor's CSV extract

#### Data CRU[D] - Create, Read, and Updates Only [No Delete]
A Gradebook record must already exist, before the utility will import course data.

Q Gradebook records are never deleted, added, or updated.
Q assignment records are added but are never deleted or updated.
Scores may be added or updated, but never deleted.

#### Archiving

stub...

#### Logging

stub...
Configurable in XML
PS Course

## Technical Details

### Setup

#### Prerequisites
- Service account
- Server
  - OS Version
  - .NET Framework
- SFTP
- Canvas
  - Checkbox
  - Course IDs
- Q
  - Gradebook
  - Teacher Emails
  - 


#### 

### Development
Stuff used:
- C#
- .NET Framework 4.6.x
- EF6
- Logging (TBD)
- NUnit ver ???
- Moq
- Compression ...?

