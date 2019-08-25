## `access` workflow naming template
  * in the `access` workflow, only `dmaker` files are generated.
    * no special naming conventions are used to differentiate front matter, numbered pages, and back matter

### examples: ([template details](#template) below)
  * `nyu_aco123456_0000001.tif`
  * `nyu_aco123456_0000002.tif`
  * `nyu_aco123456_0000003.tif`

### template
* generic template:
  * `<digi_id>_<sequence number>.tif`
    * `digi_id`: the `digitization id` assigned to the `digital object`
    * `sequence number`: an integer padded with leading-zeros as needed,  
    e.g., `000007`, that indicates the order of the corresponding page in the item  

### requirements:
* all filenames must be numbered sequentially
  * i.e., 
    ```
    # GOOD
    ...
    nyu_aco001143_000123.tif
    nyu_aco001143_000124.tif
    nyu_aco001143_000125.tif
    ...

    # BAD 
    ...
    nyu_aco001143_000723.tif
    nyu_aco001143_000725.tif  # missing file for 000724
    nyu_aco001143_000726.tif
    ...
    ```

