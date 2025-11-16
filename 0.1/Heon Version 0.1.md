# Human Editable Object Notation (Heon) Version 0.1 (Doc  WIP)

### DataTypes:

#### Primatives:

| Type             |                       Internal Data Type                       |                                   Example Text Value |                                                                                                                                                                                 Notes |
| :--------------- | :------------------------------------------------------------: | ---------------------------------------------------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Number           |                    IEE754 Double (64-bits)                     |                                           1.0f , 1.0 |                                                                                                                                                                                       |
| Unsigned Integer |                       uint64_t (64 bit)                        |                                                1234u |                                                                                                                                                                                       |
| Integer          |                        int64_t (64 bit)                        |                                                1234i |                                                                                                                                                                                       |
| Boolean          |   Any Value greate or Equal to one bit implmentation defined   |           T , F , true , false , True, , TRUE ,FALSE |                                                                                                                                                                        case Insensive |
| String           | Standard Null Sequence Character Byte - Encode defined by read |                         "This is a String 12345@STr" |                                                                                                                                                                                       |
| Multine String   |             Standard Null Sequence Character Byte              |                         """( adfasdfasd adfasdf )""" | Effectively same as String expect multiline expect re-emit at multline, usefull for defined inline code/ or scripts, and line formated text the should re-emited in readable form etc |
| Comment          |                             String                             | // Single Line Comment , /_ Multline line Comment _/ |                                                                                                                                      Optionally Attached to each Primate or Composite |
| Null             |                              None                              |                                         NULL ,null , |                                       Used it repesent Mising values - can be use explict for clearity - but is the value return for all null properties on index of Arrays / Objects |

#### Composites:

| Type   |          Internal Data Type          |                                            Example Text Value | Notes |
| :----- | :----------------------------------: | ------------------------------------------------------------: | ----: |
| Array  |         List of Heon Values          |             [1.0, "string", 1245i, """ Some Formated Text"""] |       |
| Object | Map of Heon Values - Key-Value Pairs | { KEY1_NAME : "String", KEY2_TEST : 123i , KEY3_NAME : 10.0f} |       |

## Values Details:

### Terminators:

Comma or newlines are expectable value terminators

#### Number

#### Integer:

##### Signed:

##### Unsigned:

#### Strings:

##### Single-line:

##### Multi-line:

### Composites Details:

#### Array:


#### Object:




### HEON - Example:

```
// Root Object must also ways be Defined
{
	// This is full 64bit  ID Type
ID : 123u
// String Type - Newline or Comma are expectable Termators
Type : "Name ", "Array" :  [ 1,2,"3",1234i
//
T ]


"#12432  13412  3@12 2" : FALSE, // Wrapped Key are allow space and UniCodeCharacters.

SubObject :
{
	KEY1 :  "key1Value",
	// Trail Commas are Expectable.
	KEY2 :  "key2 Value",
}

TEST : [ {TESt : "TEST"},
1234#, "ADDFa", 1e-1243 , 566 ,67.0]

// Value can be on a new line - space
InlineMarkdownText :
"""#1221324(

	### Inline Text
	##  Uses
		-  Formated Text
		-  Scripts
		- Any other Markdown / texture format
		- Long String can be Wrapped to new lin




)1221324"""SomeUnqinueKey


```
