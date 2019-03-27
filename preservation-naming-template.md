## `preservation` workflow naming template:

### examples: ([template details](#template) below)
  * front matter:
    * `nyu_aco123456_fr01_m.tif`
    * `nyu_aco123456_fr01_d.tif`
  * numbered pages:
    * `nyu_aco123456_000123_m.tif`
    * `nyu_aco123456_000123_d.tif`
  * back matter:
    * `nyu_aco123456_bk97_m.tif`
    * `nyu_aco123456_bk97_d.tif`
  * inserts:
    * `nyu_aco123456_000456_01_m.tif`
    * `nyu_aco123456_000456_01_d.tif`
    * `nyu_aco123456_000456_02_m.tif`
    * `nyu_aco123456_000456_02_d.tif`
  * oversized:
    * `nyu_aco123456_000321_01_m.tif`
    * `nyu_aco123456_000321_02_m.tif`
    * `nyu_aco123456_000321_03_m.tif`
    * `nyu_aco123456_000321_04_m.tif`
    * `nyu_aco123456_000321_d.tif`
  * session target:
    * `nyu_aco123456_target_m.tif`
  * EOC file:
    * `20160324-IQ260-EOC.csv`
    * `nyu_aco001871_eoc.csv`

### terms:
* numbered pages: images of a pages that have a number printed on it
* front matter pages: images of pages that precede the numbered pages
* back matter pages: images of pages that follow the numbered pages
* insert pages: images of pages that do not have numbers on them that  
appear between numbered pages
* oversized pages: images of pages that require multiple `master` files  
to capture and are stitched together into a single `dmaker` file

### template
* generic template:
  * `<digi_id>_<sequence number>_<role>.tif`
    * `digi_id`: the `digitization id` assigned to the `digital object`
    * `sequence number`: an integer padded with leading-zeros as needed,  
    e.g., `000007`, that indicates the order of the corresponding page  
    in the item
    * `role`: the role of the file, e.g., `master`, `dmaker`
      * use `_m` for `master` files
      * use `_d` for `dmaker` files

#### specific templates
* **numbered pages:**
  * template: `<digi_id>_<page number>_<role>.tif`
    * `page number`: a **six digit** integer padded with leading zeros that  
    matches the page number in the item
* **front matter pages:**
  * template: `<digi_id>_fr<sequence number>_<role>.tif`
    * `sequence number`: a **two digit** integer padded with leading zeros
      * can use three digits when needed
* **back matter pages:**
  * template: `<digi_id>_bk<sequence number>_<role>.tif`
    * `sequence number`: a **two digit** integer padded with leading zeros
      * can use three digits when needed
* **inserts:**
  * template: `<digi_id>_<page number>_<sequence number>_<role>.tif`
    * `page number`: the **six digit** integer padded with leading zeros that  
    matches the last numbered page in the item
    * `sequence number`: a **two digit** integer padded with leading zeros  
    that indicates the sequence of the page in the "insert" section
      * can use three digits when needed
* **oversized pages:**
  * `dmaker` template: `<digi_id>_<page number>_d.tif`
    * `page number`: a **six digit** integer padded with leading zeros that  
    matches the page number in the item
  * `master` template: `<digi_id>_<page number>_<sequence number>_<role>.tif`
    * `sequence number`: a **two digit** integer padded with leading zeros  
    that indicates that this is part of an oversized page
* **session target:**
  * `dmaker` template: N/A
  * `master` template: `<digi_id>_target_m.tif`
* **EOC file:**
  * template: `<digitization station name>-EOC.csv`
  * template: `<digitization station name>_EOC.csv`
  * template: `<digitization station name>_eoc.csv`
  * template: `<digi_id>_eoc.csv`
