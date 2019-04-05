## DOCUMENT STATUS: WORK-IN-PROGRESS

## Digital Object Type Documentation
This repository contains files describing the digital object types supported   
by New York University's Digital Library Technology Services department.

## Digital Object Types (`DOT`s)
* `book`: the `DOT` created when digitizing a bound volume
* `image set` : the `DOT` created when digitizing an unbound `item`,  
   e.g., a folder of documents 

## Digital Object Types (`DOT`s) and Digitization Workflows
### `book` Digitization Workflows

| workflow<br>name | master<br>files | dmaker<br>files | session<br>target | EOC<br>file | naming<br>template                        |
|------------------|:---------------:|:---------------:|:-----------------:|:-----------:|:-----------------------------------------:|
| `preservation`   | REQUIRED        | REQUIRED        | REQUIRED          | REQUIRED    | [link](./preservation-naming-template.md) |
| `access`         | ---             | REQUIRED        | ---               | ---         | [link](./access-naming-template.md)       |
| `bookeye`        | ---             | REQUIRED        | ---               | REQUIRED    | [link](./bookeye-naming-template.md)      |


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
* `digitization process/method/technique/workflow(?)`**[need a term here!]:**  
the workflow used to digitize the item, e.g., `preservation`, `access`, `bookeye-4`
* `master file`: a file used for long-term storage/preservation of the `digital object`.  
  In imaging projects, the `master file` includes a calibration target alongside  
  the content being imaged.  
* `session-target file`: a file containing the image of a calibration target
* `derivative-maker file (dmaker)`: a file used to generate access files. In  
imaging projects, the `dmaker file` contains a cropped version of the `master file`  
in which the calibration target has been excluded.
* `digital object type variant`: the name for the combination of a `DOT` and  
a `digitization process/method/technique/workflow`.  For example, a book item  
can be digitized using various `digitization workflows`, e.g., the `preservation`  
workflow, the `access` workflow, the `bookeye-4` workflow, all of which result  
in a different set of files in the `digital object`.

### Template Notation
* naming templates are used throughout this documentation
* a template is a string that indicates how something should be named
* angle brackets `<...>` indicate a REQUIRED value
* square brackets `[]` indicate an OPTIONAL value
* a vertical bar `|` indicates alternate values
* any characters outside of brackets must be present as written

### Directory Naming
* **new digital objects**
  * the first time a `digital object` is created, all files for the   
  `digital object` MUST be stored in a directory named `<digi_id>`,  
  e.g., `nyu_aco123456/`
* **patches**
  * if some files in the original `digital object` need to be replaced,  
  the replacement files MUST be stored in a directory named `<digi_id>_patch`,  
  e.g., `nyu_aco123456_patch/`
* **redos**
  * if the original `digital object` needs to be replaced completely, the files  
  for the `replacement digital object` MUST be stored in a directory named  
  `<digi_id>_redo`, e.g., `nyu_aco123456_redo/`
* **additions**
  * if there are files that should be added to the original `digital object`,   
  e.g., searchable PDF files, `.srt` files, the files MUST be stored in a  
  directory named `<digi_id>_add`, e.g., `nyu_aco123456_add/`
---
