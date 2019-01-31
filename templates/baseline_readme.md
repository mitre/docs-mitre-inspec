# vendor-product-version-edition[-stig|cis]-baseline

    Examples: microsoft-iis-8.5-site-stig-baseline (specific version)
              apache-tomcat-7-cis-baseline (7.x)
              rsa-archer-6-baseline (6.x)


InSpec Profile to validate the secure configuration of vendor product-version-edition, against the [<DISA/CIS/vendor>](http://linktosite)'s **<CIS Benchmark|DISA STIG, etc.> version <x.y.z>**.

    Note to be removed: Moving forward, maybe we should just base our profiles, 
    etc. on the version of the benchmark, stig, etc. since that is how 
    people will use it? I am not sure they care what our versions are 
    plus they don't change a ton after the fact. Or, if we really feel 
    the need to have our own versioning scheme maybe we can have 
    something like <benchmark|stig version>_<semver>. 

## Getting Started  
It is intended and recommended that InSpec run this profile from a __"runner"__ host (such as a DevOps orchestration server, an administrative management system, or a developer's workstation/laptop) against the target remotely over __<transport_protocol>__.

    Note to be removed: Changed it from "component" to "the target" because we talk about "Ruby language components" below. 
    
__For the best security of the runner, always install on the runner the _latest version_ of InSpec and supporting Ruby language components.__ 

Latest versions and installation options are available at the [InSpec](http://inspec.io/) site.

## Running This Profile

    inspec exec https://github.com/mitre/<project>/archive/master.tar.gz -t <transport-protocol>://<hostip> --user '<admin-account>' --password=<password> --reporter cli json:<filename>.json

Runs this profile over <transport-protocol> to the host at IP address <hostip> as a privileged user account (i.e., an account with administrative privileges), reporting results to both the command line interface (cli) and to a machine-readable JSON file. 

    NOTE: Provide a usable example based on instructions above. 
    Example:
    inspec exec https://github.com/mitre/stig-microsoft-iis-8.5-site-baseline/archive/master.tar.gz -t winrm://$winhostip --user 'Administrator --password=Pa55w0rd --reporter cli json:my-iis-site.json

## Viewing the JSON Results

The JSON results output file can be loaded into __[heimdall-lite](https://mitre.github.io/heimdall-lite/)__ for a user-interactive, graphical view of the InSpec results. 

The JSON InSpec results file may also be loaded into a __full heimdall server__, allowing for additional functionality such as to store and compare multiple profile runs.

## Contributing and Getting Help
To report a bug or feature request, please open an [issue](https://github.com/ejaronne/readmes/issues/new).

For other help, please send a message to [inspec@mitre.org](mailto:inspec@mitre.org).

To contribute, please review the [contribution guidelines](https://github.com/mitre/docs-mitre-inspec/blob/master/CONTRIBUTING.md).

## Authors
* author_1
* author_2

## Special Thanks
* person_1
* person_2
 
## Additional References
* reference_1
* reference_2

## License
This is licensed under the [Apache 2.0](https://github.com/mitre/project/blob/master/LICENSE.md) license. 

### NOTICE

© 2019 The MITRE Corporation.

Approved for Public Release; Distribution Unlimited. Case Number 18-3678.  

### NOTICE
MITRE hereby grants express written permission to use, reproduce, distribute, modify, and otherwise leverage this software to the extent permitted by the licensed terms provided in the LICENSE.md file included with this project.

### NOTICE  

This software was produced for the U. S. Government under Contract Number HHSM-500-2012-00008I, and is subject to Federal Acquisition Regulation Clause 52.227-14, Rights in Data-General.  

No other use other than that granted to the U. S. Government, or to those acting on behalf of the U. S. Government under that Clause is authorized without the express written permission of The MITRE Corporation.

For further information, please contact The MITRE Corporation, Contracts Management Office, 7515 Colshire Drive, McLean, VA  22102-7539, (703) 983-6000.
