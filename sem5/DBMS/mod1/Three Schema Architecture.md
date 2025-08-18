
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.17 - 23.23pm.drawing",
	"width": 1134,
	"aspectRatio": 1.4921052631578948
}
```
# Goal for the 3 schema architecture
## Seperates user application from physical storage
Composed of: 
### 1) Internal Level - Describes physical storage structure
- Uses physical data model
- Specifies:
	- File structures
	- Indexing/access paths
	- Record Layouts
- Also known as internal schema
### Conceptual Level - Describes structure of the database
- Uses representational data model
- Independent of physical storage
- Captures
	- Entities, relationships
	- Data types, operations
	- Integrety constraints
- Also known as conceptual schema
### External level - Defines User specific views of data
- Multiple external schemas possible
- Hides irrelavant details
- Each view is tailored for user group
- Known as external schema
## Data Independence
Nature whereby one can change the structure of the database without having to change its implementation or data
### Physical Data Independence
- Change in internal schema does not affect conceptual schema
- for eg:
	- Using new types of storage device
	- Modifying the file structure
	- switching data structures
	- Changing the access methods
### Logical Data Independence
- change in conceptual schema doesn't affect external schema
- for eg:
	- Adding/ modifying/deleting a new attribute, entity or relationship
	- merging 2 records
	- divide a record