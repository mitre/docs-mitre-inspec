# vendor-product-version-edition[-stig|cis]-baseline

    Examples: microsoft-iis-8.5-site-stig-baseline (specific version)
              apache-tomcat-7-cis-baseline (7.x)
              rsa-archer-6-baseline (6.x)

InSpec Profile to validate the secure configuration of vendor product-version-edition, against the [<DISA/CIS/vendor>](http://linktosite)'s **<CIS Benchmark|DISA STIG, etc.> version <x.y.z>**.

## Getting Started  
It is intended and recommended that InSpec run this profile from a __"runner"__ host (such as a DevOps orchestration server, an administrative management system, or a developer's workstation/laptop) against the target remotely over __<transport_protocol>__.

    Note to be removed: Changed it from "component" to "the target" because we talk about "Ruby language components" below. 
    
__For the best security of the runner, always install on the runner the _latest version_ of InSpec and supporting Ruby language components.__ 

Latest versions and installation options are available at the [InSpec](http://inspec.io/) site.

    NOTE: This is for situations where the user needs to provide attribute configurations, 
    credentials, etc. to inspec (e.g., rsa archer instance, database, etc.) so 
    it knows what to target. 
    
The following attributes must be configured in an attributes file for the profile to run correctly. More information about InSpec attributes can be found in the [InSpec Profile Documentation](https://www.inspec.io/docs/reference/profiles/).

```
# Description of attribute
attribute-name: default-value

# Username for MSSQL DB Server
user: null

# Password for MSSQL DB Server
password: null

# Hostname of MSSQL DB Server
host: null

# Instance name of MSSQL DB Server
instance: null

# Port number of MSSQL DB Server
port: 49789

# Name of the specific database being evaluated within the MSSQL DB Server
db_name: 'master'
```
The following environment variables must also be set in order for the profile to run correctly. 

Windows
```
$ setx VARIABLE_NAME=value
```

UNIX/Linux/MacOS
```
$ export VARIABLE_NAME=value
```

## Running This Profile

    inspec exec https://github.com/mitre/<project>.git --attrs=<path_to_your_attributes_file/name_of_your_attributes_file.yml> --target=<transport-protocol>://<hostip> --user=<admin-account> --password=<password> --reporter cli json:<filename>.json 

Runs this profile over __<transport_protocol>__ to the host at IP address __hostip__ as a privileged user account (i.e., an account with administrative privileges), reporting results to both the command line interface (cli) and to a machine-readable JSON file. 

    NOTE: Provide a usable example based on instructions above. 
    Example:
    inspec exec https://github.com/mitre/stig-microsoft-iis-8.5-site-baseline.git --attrs=<path_to_your_attributes_file/name_of_your_attributes_file.yml> --target=winrm://$winhostip --user=Administrator --password=Pa55w0rd --reporter cli json:my-iis-site.json 

## Viewing the JSON Results

The JSON results output file can be loaded into __[heimdall-lite](https://mitre.github.io/heimdall-lite/)__ for a user-interactive, graphical view of the InSpec results. 

The JSON InSpec results file may also be loaded into a __full heimdall server__, allowing for additional functionality such as to store and compare multiple profile runs.

## Contributing and Getting Help
To report a bug or feature request, please open an issue at https://github.com/mitre/ <project> /issues/new .

For other help, please send a message to [inspec@mitre.org](mailto:inspec@mitre.org).

To contribute, please review the [contribution guidelines](https://github.com/mitre/docs-mitre-inspec/blob/master/CONTRIBUTING.md).

## Authors
* author_1
* author_2

## Special Thanks 
     NOTE: This is for people that have made significant contributions to development/testing of the profile
* person_1
* person_2
 
## Additional References (OPTIONAL SECTION)
* reference_1
* reference_2

## License
This is licensed under the Apache 2.0 license excepted as noted in [LICENSE.MD](https://github.com/mitre/project/blob/master/LICENSE.md). 

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
