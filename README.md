<table align="center"><tr><td align="center" width="9999">
<img src="sharetide-logo.png" align="center" width="150" alt="Project icon">

# ShareTide

_OpenTide `TLP:CLEAR` Content Sharing_

</td></tr></table>

## Overview

ShareTide is the repository for open source, `TLP:CLEAR`, OpenTide objects that can be shared across the public OpenTide community. It is meant as an information exchange across Detection Engineering team worlwide and avoid work duplication for teams consuming similar Cyber Threat Intelligence.

### Consumption

You can import any file from this repository in your own OpenTide repo and let the automation rebuild your schemas to integrate the new objects. We recommend that you import these objects in a PR/MR to allow the pipeline to validate them, which will be important when ShareTide objects start referecing one another (for example TVM chaining, or cross-object relation).

In such cases, we recommend either importing objects one by one to allow the schema to build in-between imports to respect their dependencies. 
 
### Contributing

You are welcome to open a PR and propose new OpenTide object to share to the community.

### Licensing

All objects shared in this repository are licensed under [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.en). 

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg


**Guidelines**
- Ensure that all information contained in the object is public information.
- Before being ready for a review, your PR must pass the Schema Validation pipeline.
- Use the latest template/schema available 
