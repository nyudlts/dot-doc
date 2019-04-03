## `access` workflow naming template
  * in the `access` workflow, only `dmaker` files are generated.
    * no special naming conventions are used to denote front matter, numbered pages, or back matter

### examples: ([template details](#template) below)
  * `nyu_aco123456_0000001.tif`
  * `nyu_aco123456_0000002.tif`
  * `nyu_aco123456_0000003.tif`

### template
* generic template:
  * `<digi_id>_<sequence number>.tif`
    * `digi_id`: the `digitization id` assigned to the `digital object`
    * `sequence number`: an integer padded with leading-zeros as needed,  
    e.g., `000007`, that indicates the order of the corresponding page  
    in the item

* all filenames must be numbered sequentially, with no breaks sequence numbers
  * e.g., 
  ```
  # OK
  ...
  nyu_aco000123.tif
  nyu_aco000124.tif
  nyu_aco000125.tif
  ...

  # BAD (missing 000724)
  ...
  nyu_aco000723.tif
  nyu_aco000725.tif
  nyu_aco000726.tif
  ...
  ```

