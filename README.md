# Innovator Data Model Graph View - Installation


## History

Release          | Notes                        | Supported Aras Versions
-----------------|------------------------------|-------------------
[v1](add link)   | Initial Release              | 11SP15, 12SP0, 12Sp5, 12SP6, 12SP8

*add link to version location in repository on each row


## Important!
**Always back up your code tree and database before applying an import package or code tree patch!**


## Pre-requisites

1. Aras Innovator installed (supported version)
2. Aras Package Import tool 
3. AML tool like nash or AML-Studio
4. Import packages of this solution


## Install Steps

### Import Packages
Packages are located in folder "Import" of this solution

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Select relevant database and enter your login credentials for "root" and click **Login**

#### Import Step 1
4. Enter the package name in the TargetRelease field.
5. Enter the path to the `Import\imports.mf` file into the Manifest File field.
6. Select all packages in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

#### Import if used with Innovator 11SP15
Patches for it to run on 11SP15 are located in foldert "Import/Innovator Data Model Graph View - patch for 11SP15 (Methods)" of this soluton

Open Aras Package Import tool again and login as "root"

10. Enter the path to the 'Import\Innovator Data Model Graph View - patch for 11SP15 (Methods)\imports.mf' file into the Manifest File field.
11. Select all packages in the Available for Import field.
12. Select Type = **Merge** and Mode = **Thorough Mode**.
13. Click **Import** in the top left corner.
14. Close the Aras Package Import tool.

### Post Import Steps
none 

### Deploy Code Tree Changes
none


## Installation Validation (quick steps)
1. log on as "admin" 
2. Go to TOC "Administration/Item Types"  --> search for name = "ItemType"
3. Pick an ItemType (i.e. Part) --> right click and start action "Show Related ItemTypes Data Model"


## Contributing
For more information on contributing to this Presales Solution, send an email to the owner at "Technical Enablement"


## License
Aras Presales Solutions are published under the MIT license. See the [LICENSE.md file](./LICENSE.md) for license rights and limitations.
