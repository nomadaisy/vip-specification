# Coding Styles


## Text Files

This section applies to all text files in the repository (XML, HTML,
Markdown, etc).

* The file encoding should be UTF-8.

* Line endings should be LF (as opposed to CRLF).  Git should handle this
  automatically for you via the project [`.gitattributes`](.gitattributes) file.

* Trailing white space should be removed from the end of lines.

* Spaces should be used instead of tabs.  See the file-type specific
  section for how many spaces should be used for indentations.


## XSD Styles

### Indentation

* Two-space indents should be used (e.g. in place of tabs).


### Naming Styles
+ Attributes should be camelCased - The first letter of the second and subsequent words are capitalized.
+ Elements should be TitleCased (PascalCased) - The first letter of every word is capitalized.
+ Enumerations should be spinal-case - all lower case with spaces replaced with hyphens.


### IDs

* A primary key ID should be an attribute with type "xs:ID" and name "id".
  For example,

    ```xml
    <xs:attribute name="id" type="xs:ID" use="required" />
    ````
  Note that this departs from the style used by [VSSC 1622.2][vssc_1622],
  where the name is "object_id".

* A reference to a primary key should have type "xs:IDREF".  The name
  of the element or attribute should normally end with the name of the type
  of the object being referenced, followed by "ID" (and made TitleCased or
  camelCased as appropriate).  For example,

    ```xml
    <xs:element name="ElectoralDistrictID" type="xs:IDREF" />
    ````


### Attributes

Attributes should appear in the following order:

1. name
2. type
3. minOccurs
4. maxOccurs

Any attributes not listed above should appear after those listed.  Also,
a single space should separate the final attribute from the closing "`/>`".
For example--

```xml
<xs:attribute name="id" type="xs:ID" use="required" />
```


## CSV Styles
To be determined


[vssc_1622]: http://grouper.ieee.org/groups/1622/groups/2/index.html