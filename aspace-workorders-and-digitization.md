## ArchivesSpace Work Orders and Digitization

ArchivesSpace work orders contain information required to properly  
name digital object directories and files, and to associate the   
digital objects with their corresponding ArchivesSpace `archival objects`.  

**It is critical**, therefore, that the digitization identifier (`digi_id`) is properly    
formed using information in the corresponding work order row, and that the  
**digital object directory name** matches the `digi_id`.

The `digi_id` **must** end with either the `Ref ID` value or the  
`Component ID` value found in the ArchivesSpace work order row for the  
object being digitized.  This requirement allows DLTS to look up the  
ArchivesSpace Archival Object `URI` using the `digi_id`. 

**The project manager and digitization team should agree upon the  
`digi_id` structure before digitization begins.**

---

**Example 1:**  
Let's say that we're given the following ArchivesSpace work order:

| Resource ID | Ref ID                           | URI                                     | Container Indicator 1 | Container Indicator 2 | Container Indicator 3 | Title         | Component ID | Series         |
|-------------|----------------------------------|-----------------------------------------|-----------------------|-----------------------|-----------------------|---------------|--------------|----------------|
| XY.MC.099   | 731a6d52fd287ce04c86a4d82fd6b098 | /repositories/73/archival\_objects/4752 | 4                     | 32                    |                       | A Great Title | ref10_000001 | Awesome Things |


To simplify things, let's only show the columns that are used to create `digi_id`s.  

| Resource ID | Ref ID                           | Component ID |
|-------------|----------------------------------|--------------|
| XY.MC.099   | 731a6d52fd287ce04c86a4d82fd6b098 | ref10_000001 |


In this example, the project manager and digitization team agreed to  
use the `Resource ID` and the `Component ID` to form the `digi_id`\.  

Following the rules outlined [here](./README.md#characters-allowed-in-directory-names-and-file-names):  \
the `Resource ID` value `XY.MC.099` becomes `XY_MC_099` and  
the `Component ID` value `ref10_000001` can be used as is,   
resulting in the `digi_id`: **`XY_MC_099_ref10_000001`**

Because the digital object directory name **must** match the `digi_id`, we have:  
```
   XY_MC_099_ref10_000001/
                          XY_MC_099_ref10_000001_000001_m.tif
                          XY_MC_099_ref10_000001_000001_d.tif
                          XY_MC_099_ref10_000001_000002_m.tif
                          XY_MC_099_ref10_000001_000002_d.tif
                          ...
```
---

**Example 2.**  
Given the following ArchivesSpace work order,   
(only showing the columns used to create `digi_id`s):  

| Resource ID | Ref ID | Component ID |
|-------------|--------|--------------|
| BAR.937     | ref442 | 937.0123     |


In this example, the project manager and digitization team agreed to  
use the `Resource ID` and the `Ref ID` to form the `digi_id`\.  

Following the rules outlined [here](./README.md#characters-allowed-in-directory-names-and-file-names):  \
the `Resource ID` value `BAR.937` becomes `BAR_937` and  
the `Ref ID` value `ref442` can be used as is,  
resulting in the `digi_id`: **`BAR_937_ref442`**


Because the digital object directory name **must** match the `digi_id`, we have:  
```
   BAR_937_ref442/
                  BAR_937_ref442_000001_m.tif
                  BAR_937_ref442_000001_d.tif
                  BAR_937_ref442_000002_m.tif
                  BAR_937_ref442_000002_d.tif
                  ...
```

---

**Example 3.**  
Given the following ArchivesSpace work order,   
(only showing the columns used to create `digi_id`s):  

| Resource ID | Ref ID                           | Component ID |
|-------------|----------------------------------|--------------|
| QUUX.876    | ecc59b4631de477fb7f734fd80e208d1 | cuid2594     |


In this example, the project manager and digitization team decided to generate the  
`digi_id` using a "partner code", a "collection code", and the `Component ID` from the  
work order.  

The partner code is `foo`  
the collection code is `quux876`  
and the `Component ID` value is `cuid2594`\,  
resulting in the `digi_id`: **`foo_quux876_cuid2594`**

Because the digital object directory name **must** match the `digi_id`, we have:  
```
   foo_quux876_cuid2594/
                        foo_quux876_cuid2594_000001_m.tif
                        foo_quux876_cuid2594_000001_d.tif
                        foo_quux876_cuid2594_000002_m.tif
                        foo_quux876_cuid2594_000002_d.tif
                        ...
```

---

*end of examples*
