# BAND SDK Community Policy Compatibility for \<JETSCAPE Bayesian Analysis\>


> This document summarizes the efforts of current and future BAND member packages to achieve compatibility with the BAND SDK community policies. Additional details on the BAND SDK are available [here](https://github.com/bandframework/privateband/blob/team/Resources/bandsdk.md) and should be considered when filling out this form.
>
> Please provide information on your compatibility status for each mandatory policy and, if possible, also for recommended policies.
If you are not compatible, state what is lacking and what are your plans on how to achieve compliance.
For current BAND SDK packages: If you were not fully compatible at some point, please describe the steps you undertook to fulfill the policy. This information will be helpful for future BAND member packages.
>
> To suggest changes to these requirements or obtain more information, please contact [BAND's Design & Oversight Committee](https://github.com/bandframework/privateband/blob/team/Resources/DesignandOversight.md)



**Website:** \<https://github.com/j-f-paquet/emulator-validation.git\>

### Mandatory Policies

**BAND SDK**
| # | Policy                 |Support| Notes                   |
|---|-----------------------|-------|-------------------------|
| 1. | Support BAND community GNU Autoconf, CMake, or other build options |None| The code is in Python. But it does not contain a setup file to install relevent dependencies. Can be Python packaged;see below. [M1 details](#m1-details)|
| 2. | Provide a comprehensive test suite for correctness of installation verification |None| No tests are provided at this time.| 
| 3. | Provide a documented, reliable way to contact the development team |None| No documentation except for function definitions. Can use Sphenix for documentation; see below. [M3 details](#m3-details)||
| 4. | Come with an open-source license |None| Can use 2-clause BSD license.|
| 5. | Provide a runtime API to return the current version number of the software |None|No API has been designed. For now the code is a collections of python modules under src folder|
| 6. | Provide a BAND team-accessible repository |Full|https://github.com/j-f-paquet/emulator-validation.git|
| 7. | Must allow installing, building, and linking against an outside copy of all imported software that is externally developed and maintained |Full| Dreks code does not contain any other package's source code within. Note that Python packages are imported using the conventional `sys.path` system. Alternative instances of a package can be used, for example, by including them through an appropriate definition of the PYTHONPATH environment variable.|
| 8. |  Have no hardwired print or IO statements that cannot be turned off |None| There are print sttements that can not be turned off|

M1 details <a id="m1-details"></a>: https://packaging.python.org/tutorials/packaging-projects/
M3 details <a id="m3-details"></a>: https://www.sphinx-doc.org/en/master/

### Recommended Policies

| # | Policy                 |Support| Notes                   |
|---|------------------------|-------|-------------------------|
|**R1.**| Have a public repository. |Full| https://github.com/j-f-paquet/emulator-validation.git|
|**R2.**| Free all system resources acquired as soon as they are no longer needed. |Full| Python has built-in garbage collection that frees memory when it becomes unreferenced. |
|**R3.**| Provide a mechanism to export ordered list of library dependencies. |None|Proper instalation of dependencies has yet to be included|
|**R4.**| Document versions of packages that it works with or depends upon, preferably in machine-readable form.  |None| None. What is here meant by machine-readable form? |
|**R5.**| Have README, SUPPORT, LICENSE, and CHANGELOG files in top directory.  |None| None of these exists|
|**R6.**| Have sufficient documentation to support use and further development.  |None| Need documentation |
|**R7.**| Be buildable using 64-bit pointers; 32-bit is optional.|Full| There is no explicit use of pointers in surmise, as Python handles pointers internally and depends on the install of Python, which will generally be 64-bit on supported systems.|
|**R8.**| Do not assume a full MPI communicator; allow for user-provided MPI communicator |N/a| None. |
|**R9.**| Use a limited and well-defined name space (e.g., symbol, macro, library, include) |Full| All the modules are unders Src directory. Functions are only accesible under src.module_name|
|**R10.**| Give best effort at portability to key architectures |None| None.|
|**R11.**| Install headers and libraries under `<prefix>/include` and `<prefix>/lib`, respectively |None| No install setup. All modules are in Src directory|
|**R12.**| All BAND compatibility changes should be sustainable |None| None.|
|**R13.**| Respect system resources and settings made by other previously called packages |None| None.|