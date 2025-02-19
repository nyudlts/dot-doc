## `preservation` workflow naming template for `image sets`

An `image set` is a group of images typically generated by imaging a set of unbound documents, e.g., an archival folder.

### examples: ([template details](#template) below)
  * regular-sized documents (i.e., a document that can be photographed in one shot):
    * `fales_mss123_cuid1234_000001_m.tif`
    * `fales_mss123_cuid1234_000001_d.tif`
  * oversized documents (i.e., a document that requires multiple shots to capture):
    * e.g., oversized document requiring 4 `master` files
      * `fales_mss123_cuid1234_000003_01_m.tif`
      * `fales_mss123_cuid1234_000003_02_m.tif`
      * `fales_mss123_cuid1234_000003_03_m.tif`
      * `fales_mss123_cuid1234_000003_04_m.tif`
      * `fales_mss123_cuid1234_000003_d.tif`
  * session target:
    * `fales_mss123_cuid1234_target_m.tif`
  * EOC file:
    * `20160324-IQ260-EOC.csv`


### [Link to "Terms Used"](./README.md#terms-used)
### Additional `preservation` workflow terms:
  * **oversized documents**: a document that requires multiple `master` files  
    to capture. The `master` files are stitched together to create a single `dmaker` file  

  ### templates
  * general template: <code>&lt;digi_id&gt;<b>\_</b>&lt;sequence number&gt;<b>\_</b>&lt;role&gt;<b>.tif</b></code>
    * `digi_id`: the `digitization id` assigned to the `digital object`
    * `sequence number`: a **six digit** integer padded with leading-zeros, e.g., `000007`,  
    that indicates the order of the image in the `image set`
    * `role`: the role of the file, e.g., `master`, `dmaker`
      * use `_m` for `master` files
      * use `_d` for `dmaker` files

  * **oversized documents:**
      * an oversized document is one that requires more than one `master` image to fully capture 
      * `master` template: <code>&lt;digi_id&gt;<b>\_</b>&lt;sequence number&gt;<b>\_</b>&lt;master file number&gt;<b>\_m.tif</b></code>
        * `sequence number`: a **six digit** integer padded with leading-zeros, e.g., `000007`  
        * `master file number`: a **two digit** integer padded with leading zeros that indicates that this master file is part of an oversized document
      * `dmaker` template: <code>&lt;digi_id&gt;<b>\_</b>&lt;sequence number&gt;<b>\_d.tif</b></code>
        * `sequence number`: a **six digit** integer padded with leading-zeros, e.g., `000007`  
        * please note: the `dmaker` file is constructed by stitching the individual master files into a single large image,  
          therefore the `dmaker` template does not include a separate `file number` 

  * **session target:**
    * `master` template: <code>&lt;digi_id&gt;<b>\_target_m.tif</b></code>
    * `dmaker` template: **NOT APPLICABLE** (there are no session-target `dmaker` files)

  * **EOC file:**
    * the following are valid EOC templates:
      * template: <code>&lt;digitization station name&gt;<b>\-EOC.csv</b></code>
      * template: <code>&lt;digitization station name&gt;<b>_EOC.csv</b></code>
      * template: <code>&lt;digitization station name&gt;<b>_eoc.csv</b></code>
      * template: <code>&lt;digi_id&gt;<b>_eoc.csv</b></code>

### requirements:
* for every regular-sized document:
  * every `master` file **MUST** have a corresponding `dmaker` file
* for oversized documents
  * the multiple `master` files used to capture a single physical oversized document
    **MUST** be stitched together into one `dmaker` file

* all filenames must be numbered sequentially
    * e.g., 
      ```
      # GOOD
      fales_mss123_cuid1234_000001_m.tif
      fales_mss123_cuid1234_000001_d.tif
      fales_mss123_cuid1234_000002_m.tif
      fales_mss123_cuid1234_000002_d.tif
      fales_mss123_cuid1234_000003_01_m.tif
      fales_mss123_cuid1234_000003_02_m.tif
      fales_mss123_cuid1234_000003_03_m.tif
      fales_mss123_cuid1234_000003_04_m.tif
      fales_mss123_cuid1234_000003_d.tif    
      fales_mss123_cuid1234_000004_m.tif
      fales_mss123_cuid1234_000004_d.tif
      fales_mss123_cuid1234_000005_m.tif
      fales_mss123_cuid1234_000005_d.tif
      fales_mss123_cuid1234_000006_m.tif
      fales_mss123_cuid1234_000006_d.tif
                  

      # BAD 
      fales_mss123_cuid1234_000001_m.tif
      fales_mss123_cuid1234_000001_d.tif
      fales_mss123_cuid1234_000002_m.tif    # missing dmaker file
      fales_mss123_cuid1234_000003_01_m.tif
      fales_mss123_cuid1234_000003_02_m.tif
      fales_mss123_cuid1234_000003_03_m.tif
      fales_mss123_cuid1234_000003_04_m.tif
      fales_mss123_cuid1234_000003_d.tif
      fales_mss123_cuid1234_000004_d.tif    # missing master file
      fales_mss123_cuid1234_000006_m.tif    # missing image files for 000005
      fales_mss123_cuid1234_000006_d.tif
      
      ...
      ```

---
