## ArchivesSpace Work Orders and Digitization

ArchivesSpace work orders contain information required to properly  
name digital object directories and files.  This name is the digitization  
identifier, or `digi_id`.  

DLTS uses the `digi_id` to look up the ArchivesSpace archival object URI  
which is required to load persistent URLs for the digital objects into  
ArchivesSpace.

**It is critical**, therefore, that `digi_id` is generated from the  
information in the ArchivesSpace work order, and that the   
**digital object directory name** matches the `digi_id`.


## Generating the `digi_id`
For digitization projects with ArchivesSpace work orders, the `digi_id`  
is formed by combining a string of characters (the `prefix`), with either  
the work order `Ref ID` or `Component ID` values.  

The `prefix` can be any string of characters that conforms to the rules  
outlined [here](./README.md#characters-allowed-in-directory-names-and-file-names),  but is usually either a normalized version of the `Resource ID`\,  
or a combination of partner and collection codes from the DLTS repository.  

**The `digi_id` must end with either the `Ref ID` or the `Component ID`  
value from the ArchivesSpace work order.**

This means that the `digi_id` must conform to one of the following templates:  
* `<prefix>_<Ref ID>`  
* `<prefix>_<Component ID>`  


**The project manager and digitization team should agree upon the  
`digi_id` structure before digitization begins.**

#### Examples:  
The following examples show `digi_id`s generated using various `prefixes`.  

---

**Example 1:  `digi_id` = `<Normalized Resource ID>_<Component ID>`**  


| Resource ID | Ref ID                           | Component ID |
|-------------|----------------------------------|--------------|
| XY.MC.099   | 731a6d52fd287ce04c86a4d82fd6b098 | ref10_000001 |

`prefix` = `XY_MC_099` (`Resource ID` normalized per [these rules](./README.md#characters-allowed-in-directory-names-and-file-names).)  
`Component ID` = `ref10_000001`  

`digi_id`: **`XY_MC_099_ref10_000001`**

*required directory structure:*
```
   XY_MC_099_ref10_000001/
                          XY_MC_099_ref10_000001_000001_m.tif
                          XY_MC_099_ref10_000001_000001_d.tif
                          XY_MC_099_ref10_000001_000002_m.tif
                          XY_MC_099_ref10_000001_000002_d.tif
                          ...
```
---

**Example 2:  `digi_id` = `<Resource ID>_<Ref ID>`**  

| Resource ID | Ref ID | Component ID |
|-------------|--------|--------------|
| BAR.937     | ref442 | 937.0123     |

`prefix` = `BAR_937` (`Resource ID` normalized per [these rules](./README.md#characters-allowed-in-directory-names-and-file-names).)  
`Ref ID` = `ref442`   

`digi_id`: **`BAR_937_ref442`**

*required directory structure:*
```
   BAR_937_ref442/
                  BAR_937_ref442_000001_m.tif
                  BAR_937_ref442_000001_d.tif
                  BAR_937_ref442_000002_m.tif
                  BAR_937_ref442_000002_d.tif
                  ...
```

---

**Example 3:  `digi_id` = `<partner code>_<collection code>_<Component ID>`**  

| Resource ID | Ref ID                           | Component ID |
|-------------|----------------------------------|--------------|
| QUUX.876    | ecc59b4631de477fb7f734fd80e208d1 | cuid2594     |


partner code: `foo`  
collection code: `quux876`  

`prefix` = `foo_quux876`  
`Component ID` value: `cuid2594`  

`digi_id`: **`foo_quux876_cuid2594`**

*required directory structure:*
```
   foo_quux876_cuid2594/
                        foo_quux876_cuid2594_000001_m.tif
                        foo_quux876_cuid2594_000001_d.tif
                        foo_quux876_cuid2594_000002_m.tif
                        foo_quux876_cuid2594_000002_d.tif
                        ...
```

---

**Example 4:  `digi_id` = `<agreed-upon string>_<Component ID>`**  

| Resource ID     | Ref ID  | Component ID |
|-----------------|---------|--------------|
| MSS.LaScala.001 | ref3412 | cuid50       |


The agreed-upon string: `vxt_MSSLaScala001`  
`Component ID` value  : `cuid50`  

`digi_id` = **`vxt_MSSLaScala001_cuid50`**


*required directory structure:*
```
   vxt_MSSLaScala001_cuid50/
                           vxt_MSSLaScala001_cuid50_000001_m.tif
                           vxt_MSSLaScala001_cuid50_000001_d.tif
                           vxt_MSSLaScala001_cuid50_000002_m.tif
                           vxt_MSSLaScala001_cuid50_000002_d.tif
                           ...
```

---

*end of examples*
