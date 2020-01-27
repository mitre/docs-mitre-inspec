# vendor-product-version-edition[-stig|cis]-baseline

    Examples: microsoft-iis-8.5-site-stig-baseline (specific version)
              apache-tomcat-7-cis-baseline (7.x)
              rsa-archer-6-baseline (6.x)
              microsoft-azure-cis-foundations-baseline

InSpec Profile to validate the secure configuration of vendor product-version-edition, against the [<DISA/CIS/vendor>](http://linktosite)'s **<CIS Benchmark|DISA STIG, etc.> version <x.y.z>**.

## Getting Started  
It is intended and recommended that InSpec run this profile from a __"runner"__ host (such as a DevOps orchestration server, an administrative management system, or a developer's workstation/laptop) against the target remotely over __<transport_protocol>__.

__For the best security of the runner, always install on the runner the _latest version_ of InSpec and supporting Ruby language components.__ 

Latest versions and installation options are available at the [InSpec](http://inspec.io/) site.

Git is required to download the latest InSpec profiles using the instructions below. Git can be downloaded from the [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) site. 

__START-OPTIONAL-ATTRIBUTES-TEXT__<br/>
The following attributes must be configured in an attributes file for the profile to run correctly. More information about InSpec attributes can be found in the [InSpec Profile Documentation](https://www.inspec.io/docs/reference/profiles/).

```
# Attribute description
attribute_name: 'value'
```
__END-OPTIONAL-ATTRIBUTES-TEXT__

## Running This Profile
When the __"runner"__ host uses this profile overlay for the first time, follow these steps: 

```
mkdir profiles
cd profiles
git clone https://<baseline_repo>.git
cd vendor-product-version-edition[-stig|cis-]-baseline
bundle install
cd ..
inspec exec vendor-product-version-edition[-stig|cis-]-baseline --attrs=<path_to_your_attributes_file/name_of_your_attributes_file.yml> [-t <transport_protocol>://<hostname>:<port> --user=<username> --password=<password>] --reporter=cli json:<path_to_your_output_file/name_of_your_output_file.json>
```
For every successive run, follow these steps to always have the latest version of this profile:

```
cd profiles/<baseline_repo>
git pull
cd ..
inspec exec vendor-product-version-edition[-stig|cis-]-baseline --attrs=<path_to_your_attributes_file/name_of_your_attributes_file.yml> [-t <transport_protocol>://<hostname>:<port> --user=<username> --password=<password>] --reporter=cli json:<path_to_your_output_file/name_of_your_output_file.json>
```

## Viewing the JSON Results

The JSON results output file can be loaded into __[heimdall-lite](https://mitre.github.io/heimdall-lite/)__ for a user-interactive, graphical view of the InSpec results. 

The JSON InSpec results file may also be loaded into a __full heimdall server__, allowing for additional functionality such as to store and compare multiple profile runs.

## Contributing and Getting Help
To report a bug or feature request, please open an [issue](https://<baseline_repo>/issues/new).

## Authors
* author_1
* author_2

## Special Thanks
* person_1
* person_2

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
