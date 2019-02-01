# [overlay-name]-vendor-product-version-edition[-stig|cis-]-overlay

    Examples: acmecorp-policy-5.2-high-microsoft-iis-8.5-site-stig-overlay

InSpec profile overlay to validate the secure configuration of vendor product-version-edition against the [\<CIS'|DISA's\>](http://linktoguide) \<Benchmark|STIG|etc.\> Version [\<x.y.z\>] Release [\<x.y.z\>] tailored for [\<overlay-name>](http://linktooverlayguide).

## Getting Started  
It is intended and recommended that InSpec and this profile be run from a __"runner"__ host (such as a DevOps orchestration server, an administrative management system, or a developer's workstation/laptop) against the target remotely over __<transport_protocol>__.
    
__For the best security of the runner, always install on the runner the _latest version_ of InSpec and supporting Ruby language components.__ 

Latest versions and installation options are available at the [InSpec](http://inspec.io/) site.

## Required Configurations
    NOTE: This is for situations where you need to provide attribute configurations, 
    credentials, etc. to inspec (e.g., rsa archer instance, database, etc.) so 
    it knows what to target. Displaying in a table (like tomcat) seems nice 
    and provide instructions on where/how people can configure them.

    Also, provide links to how to create attribute files or tailor attributes 
    in inspec.yml as well as templates. Projects should provide inspec.yml 
    attributes configured to default values (i.e. controls should be written 
    to use these attributes).
The following attributes must be configured in order for the profile to run correctly. These attributes can be configured in inspec.yml file or in an attributes file. More information about InSpec attributes can be found [here](https://www.inspec.io/docs/reference/profiles/).
    
| Attribute      | Type                            | Required | Default        | Description               |
| :---           | :---                            | :---     | :---           | :---                      |
| attribute-name | array/numeric/string/etc.yes/no | yes/no   | default-value  | Description of attribute. |

## Running This Overlay

    inspec exec https://github.com/mitre/<project>/archive/master.tar.gz -t <transport-protocol>://<hostip> --user '<admin-account>' --password=<password> --reporter cli json:<filename>.json

Runs the overlay over <transport-protocol> to the host at IP address <hostip> as a user account with administrative privileges, reporting results to both the command line interface (cli) and to a machine-readable JSON file. 

    NOTE: Provide a usable example based on instructions above. 
    Example:
    inspec exec https://github.com/mitre/stig-microsoft-iis-8.5-site-baseline/archive/master.tar.gz -t winrm://$winhostip --user 'Administrator --password=Pa55w0rd --reporter cli json:my-iis-site.json

## Viewing the JSON Results

The JSON results output file can be loaded into __[heimdall-lite](https://mitre.github.io/heimdall-lite/)__ for a user-interactive, graphical view of the InSpec results. 

The JSON InSpec results file may also be loaded into a __full heimdall server__, allowing for additional functionality such as to store and compare multiple profile runs.

## Authors
* author_1
* author_2

## Special Thanks
* person_1
* person_2

## Contributing and Getting Help
To report a bug or feature request, please open an [issue](https://github.com/ejaronne/readmes/issues/new).

For other help, please send a message to [inspec@mitre.org](mailto:inspec@mitre.org).

To contribute, please review the [contribution guidelines](https://github.com/mitre/docs-mitre-inspec/blob/master/CONTRIBUTING.md)

## License 

This project is licensed under the terms of the Apache 2.0 license excepted as noted in [LICENSE.MD](https://github.com/mitre/project/blob/master/LICENSE.md). 

### NOTICE

© 2019 The MITRE Corporation.  

Approved for Public Release; Distribution Unlimited. Case Number 18-3678.  

### NOTICE
MITRE hereby grants express written permission to use, reproduce, distribute, modify, and otherwise leverage this software to the extent permitted by the licensed terms provided in the LICENSE.md file included with this project.

### NOTICE  

This software was produced for the U. S. Government under Contract Number HHSM-500-2012-00008I, and is subject to Federal Acquisition Regulation Clause 52.227-14, Rights in Data-General.  

No other use other than that granted to the U. S. Government, or to those acting on behalf of the U. S. Government under that Clause is authorized without the express written permission of The MITRE Corporation. 

For further information, please contact The MITRE Corporation, Contracts Management Office, 7515 Colshire Drive, McLean, VA  22102-7539, (703) 983-6000.  

### NOTICE

< DISA STIGs | CIS Benchmarks > are published by < DISA IASE | the Center for Internet Security (CIS) >, see: 
< https://iase.disa.mil/Pages/privacy_policy.aspx | https://www.cisecurity.org/ >.
