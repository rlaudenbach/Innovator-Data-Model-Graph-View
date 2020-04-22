## Adhoc Workflow Voters v1
### Purpose
- Alows Administrators to graphically view the data model of an ItemType with all its Relationships, related Items Types and Item Property links.
- This solution is targeted for Aras Innovator Administrators only.

### Pre-requisites
Aras Innovator Release: 12SP5


### Implementation Details
- Two new Actions are introduced on Item Type **Item Type**
- Each starts a different Graph View  based on a different Query Definition
	- Graph View: **Innovator Data Model Down** will resolve relationships to other Item Types recursively. And it will also resolve all item Property to their target Item Types.
	- Graph View: **Innovator Data Model Surround** (360°) will resolve relationships to other Item Types one level down and one level up (where used).  And it will also resolve all item Property to their target Item Types and item Properties pointing to this Item Type with their source Item Types.

- From the Graph View the displayed ItemTypes, Relationships, and Item Properties can be opened using right click action **Open Item**.
- If on an ItemType block, another right click action **Open Graph View** allows to start this GraphView again starting with the selected ItemType.


### Improvements
- Add resolution of LifeCycles and Workflows to show on ItemTypes.

### Installation Steps

1. Back up your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**.
    * _Note: You must log in as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
    * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\Innovator Data Model Graph View\Import\imports.mf` file in the Manifest File field.
6. Select **Innovator Data Model Graph View** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top-left corner.
9. Close the Aras Package Import tool.

### Usage
- Log on to Aras as "admin"
- On TOC go to **Administration/Item Types**
- Search for **Part**
- Select **Part** row and right click and start action **Show Related Item Types Data Model**
- Related Graph View will open in new tab. Close Graph View when done.
- On Item Types search, search for **Affected Item**
- Select **Affected Item** row and right click and start action **Show Surrounding Item Types Data Model**
- Related Graph View will open in new tab. Close Graph View when done.

## Credits


## License
This project is published under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.)
