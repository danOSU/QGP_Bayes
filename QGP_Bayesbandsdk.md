# BAND SDK v0.2 Community Policy Compatibility for QGP_Bayes

> This document summarizes the efforts of current and future BAND member packages to achieve compatibility with the BAND SDK community policies.  Additional details on the BAND SDK are available [here](https://raw.githubusercontent.com/bandframework/bandframework/main/resources/sdkpolicies/bandsdk.md) and should be considered when filling out this form. The most recent copy of this template exists [here](https://raw.githubusercontent.com/bandframework/bandframework/main/resources/sdkpolicies/template.md).
>
> This file should filled out and placed in the directory in the `bandframework` repository representing the software name appended by `bandsdk`.  For example, if you have a software `foo`, the compatibility file should be named `foobandsdk.md` and placed in the directory housing the software in the `bandframework` repository. No open source code can be included without this file.
>
> All code included in this repository will be open source.  If a piece of code does not contain a open-source LICENSE file as mentioned in the requirements below, then it will be automatically licensed as described in the LICENSE file in the root directory of the bandframework repository.
>
> Please provide information on your compatibility status for each mandatory policy and, if possible, also for recommended policies. If you are not compatible, state what is lacking and what are your plans on how to achieve compliance. For current BAND SDK packages: If you were not fully compatible at some point, please describe the steps you undertook to fulfill the policy. This information will be helpful for future BAND member packages.
>
> To suggest changes to these requirements or obtain more information, please contact [BAND](https://bandframework.github.io/team).

**Website:** https://github.com/danOSU/QGP_Bayes/
**Contact:** through github
**Icon:** None
**Description:**  Bayesian Parameter Estimation Tutorial for Heavy Ion Collisions

### Mandatory Policies

**BAND SDK**
| # | Policy                 |Support| Notes                   |
|---|-----------------------|-------|-------------------------|
| 1. | Support BAND community GNU Autoconf, CMake, or other build options |partially compliant| The code is in Python.It provides an environment.yml file to make a conda environment with relevent dependenicies. But it does not contain a setup/instalation file. Can be Python packaged;see below. [M1 details](#m1-details)|
| 2. | Have a README file in the top directory that states a specific set of testing procedures for a user to verify the software was installed and run correctly | fully compliant| The user will run all and reproduce the plots that are in the tutorial notebook as a test.|
| 3. | Provide a documented, reliable way to contact the development team |fully compliant| Development team can be contacted via github||
| 4. | Come with an open-source license |fully compliant| Use MIT license.|
| 5. | Provide a runtime API to return the current version number of the software |not compliant|No API has been designed. For now the code is a collection of python modules under one src folder|
| 6. | Provide a BAND team-accessible repository |fully compliant|https://github.com/danOSU/QGP_Bayes/|
| 7. | Must allow installing, building, and linking against an outside copy of all imported software that is externally developed and maintained |fully compliant| The code does not contain any other package's source code within. Note that Python packages are imported using the conventional `sys.path` system. Alternative instances of a package can be used, for example, by including them through an appropriate definition of the PYTHONPATH environment variable.|
| 8. | Have no hardwired print or IO statements that cannot be turned off |not compliant| There are print statements that can not be turned off|

M1 details <a id="m1-details"></a>: https://packaging.python.org/tutorials/packaging-projects/

### Recommended Policies

| # | Policy                 |Support| Notes                   |
|---|------------------------|-------|-------------------------|
|**R1.**| Have a public repository. |fully compliant| https://github.com/danOSU/QGP_Bayes/|
|**R2.**| Free all system resources acquired as soon as they are no longer needed. |fully compliant| Python has built-in garbage collection that frees memory when it becomes unreferenced. |
|**R3.**| Provide a mechanism to export ordered list of library dependencies. |not compliant|Proper instalation of dependencies has yet to be included|
|**R4.**| Document versions of packages that it works with or depends upon, preferably in machine-readable form.  |fully compliant| Conda environement.yml file is provided with relevent dependenicies and in machine-readable form|
|**R5.**| Have README, SUPPORT, LICENSE, and CHANGELOG files in top directory.  |partially compliant| README and LICENSE exist|
|**R6.**| Have sufficient documentation to support use and further development.  |partially compliant|  No documentation except for function definitions. This code was developed based on a previous code and for that documentation is available at  http://qcd.phy.duke.edu/hic-param-est/|
|**R7.**| Be buildable using 64-bit pointers; 32-bit is optional.|fully compliant| There is no explicit use of pointers in the code, as Python handles pointers internally and depends on the install of Python, which will generally be 64-bit on supported systems.|
|**R8.**| Do not assume a full MPI communicator; allow for user-provided MPI communicator |N/a| None. |
|**R9.**| Use a limited and well-defined name space (e.g., symbol, macro, library, include) |fully compliant| All the modules are unders Src directory. Functions are only accesible under src.module_name|
|**R10.**| Give best effort at portability to key architectures |None| None.|
|**R11.**| Install headers and libraries under `<prefix>/include` and `<prefix>/lib`, respectively |not compliant| No install setup. All modules are in Src directory|
|**R12.**| All BAND compatibility changes should be sustainable |None| None.|
|**R13.**| Respect system resources and settings made by other previously called packages |None| None.|
