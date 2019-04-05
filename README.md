## Digital Object Naming Requirements
This repository specifies the file and naming requirements used by
New York University's Digital Library Technology Services department
to validate digital objects produced by different digitization workflows.


## Digital Object Types (`DOT`s)
* `book`: the `DOT` created when digitizing a bound volume
* `image set` : the `DOT` created when digitizing an unbound `item`,  
   e.g., a folder of documents 

## Digital Object Types (`DOT`s) and Digitization Workflows

| DOT       | workflow<br>name | master<br>files | dmaker<br>files | session<br>target | EOC<br>file | README.txt<br>file | naming<br>template                        |
|-----------|:----------------:|:---------------:|:---------------:|:-----------------:|:-----------:|:------------------:|-------------------------------------------|
| book      | `preservation`   | REQUIRED        | REQUIRED        | REQUIRED          | REQUIRED    | optional           | [link](./preservation-naming-template.md) |
| book      | `access`         | ---             | REQUIRED        | ---               | ---         | optional           | [link](./access-naming-template.md)       |
| book      | `bookeye`        | ---             | REQUIRED        | ---               | REQUIRED    | optional           | [link](./bookeye-naming-template.md)      |
| image set | `preservation`   | REQUIRED        | REQUIRED        | optional          | optional    | optional           | [link](./preservation-naming-template.md) |


### Terms Used
* `item`: a (physical) object being digitized
* `digital object`: the digitized version of an `item`
* `digital object type (DOT)`: a name assigned to a class of `digital objects`,  
e.g., `book`,`image set`
* `digitization`: the process of creating a `digital object` from an `item`
* `digitization identifier (digi_id)`: the string used to name the `digital object`
* `digitization station`: the set of equipment used to digitize an `item`
* `environment of creation file (eoc)`: a file that contains information about  
the `digitization station`
* `digitization workflow:**  
the workflow used to digitize the item, e.g., `preservation`, `access`, `bookeye`
* `master file`: a file used for long-term storage/preservation of the `digital object`.  
  In imaging projects, the `master file` includes a calibration target alongside  
  the content being imaged.  
* `session-target file`: a file containing the image of a calibration target
* `derivative-maker file (dmaker)`: a file used to generate access files. In  
imaging projects, the `dmaker file` contains a cropped version of the `master file`  
in which the calibration target has been excluded.
* `digital object type variant`: the name for the combination of a `DOT` and  
a `digitization workflow`. For example, a book item can be digitized using various  
`digitization workflows`, e.g., the `preservation` workflow, the `access` workflow,  
the `bookeye` workflow, all of which result in a different set of files in the `digital object`.

### Template Notation
* naming templates are used throughout this documentation
* a template is a string that indicates how something should be named
* angle brackets `<...>` indicate a REQUIRED value
* square brackets `[]` indicate an OPTIONAL value
* a vertical bar `|` indicates alternate values
* any characters outside of brackets must be present as written

### Characters Allowed in Directory Names and File Names:
* The **ONLY** characters allowed in directory names and file names are:  
  * `A-Za-z0-9_`   
    i.e.,   
    capital letters `A` through `Z`  
    lowercase letters `a` through `z`  
    digits `0` through `9`  
    underscore `_`  
* The dot/period '.' character is **ONLY** allowed as a delimiter between  
  a filename stem and the filename extension.
  ```
  e.g., nyu_aco123456_fr01_d.tif
        where nyu_aco123456_fr01_d is the filename "stem"
        and   tif                  is the filename "extension"
  ```
  
* examples:
  ```
  # GOOD
  /Volumes/Drive_001/this/is/a/valid/path/nyu_aco123456/nyu_aco123456_fr01_d.tif
  ```
  
  ```
  # BAD
  /Volumes/My $uper C00l Drive!/(version 1)/nyu_aco123456/nyu_aco123456_fr01_d.tif  
  ```

### Directory Naming Requirements
* **new digital objects**
  * the first time a `digital object` is created, all files for the   
  `digital object` **MUST** be stored in a directory named `<digi_id>`,  
  e.g., `nyu_aco123456/`
* **patches**
  * if some files in the original `digital object` need to be replaced,  
  the replacement files **MUST** be stored in a directory named `<digi_id>_patch`,  
  e.g., `nyu_aco123456_patch/`
* **redos**
  * if the original `digital object` needs to be replaced completely, the files  
  for the `replacement digital object` **MUST** be stored in a directory named  
  `<digi_id>_redo`, e.g., `nyu_aco123456_redo/`
* **additions**
  * if there are files that should be added to the original `digital object`,   
  e.g., searchable PDF files, `.srt` files, the files **MUST** be stored in a  
  directory named `<digi_id>_add`, e.g., `nyu_aco123456_add/`


---
