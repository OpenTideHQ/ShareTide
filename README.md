<table align="center"><tr><td align="center" width="9999">
<img src="sharetide-logo.png" align="center" width="150" alt="Project icon">

# ShareTide

_OpenTide `TLP:CLEAR` Content Sharing_

</td></tr></table>

## Overview

ShareTide is the repository for open source, `TLP:CLEAR`, OpenTide objects that can be shared across the public OpenTide community. It is meant as an information exchange across Detection Engineering team worlwide and avoid work duplication for teams consuming similar Cyber Threat Intelligence.

### Consumption

You can import any file from this repository in your own OpenTide repo and let the automation rebuild your schemas to integrate the new objects. We recommend that you import these objects in a PR/MR to allow the pipeline to validate them, which will be important when ShareTide objects start referecing one another (for example TVM chaining, or cross-object relation).

**Resolving chaining dependencies**

When you're interested in importing several TVMs at once, if they contain chaining relations to objects not yet in your OpenTide instance, they will not be valid from a validation standpoint. We recommend commenting out chaining relations for those new files, importing them all at once (committing them to your default branch) to pass validation and update your local object index and schemas, and then uncommenting the chaining relations which will have become available. 

**Resolving cross-object relation**

When you're importing related objects (typically threats and related detection objects in one go), because they are not yet indexed, the UUIDs will not be valid to be referenced. We recommend starting from the top (e.g., threat vectors), importing those objects first, letting the object index and schema rebuild, then only move on to the next layer (Detection Objectives, finally Detection Rules).
 
### Contributing

You are welcome to open a PR and propose new OpenTide objects to share to the community, and to engage in issues or discussions.

**Guidelines**
- Ensure that all information contained in the object is public information.
- Before being ready for a review, your PR must pass the Schema Validation pipeline.
- Use the latest template/schema available 

### Licensing

All objects shared in this repository are licensed under [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.en). 

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
