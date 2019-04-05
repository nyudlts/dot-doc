## `bookeye` workflow naming template
  * in the `bookeye` workflow:
    * no special naming conventions are used to differentiate the session target, front matter pages, numbered pages, and back matter pages
    * each digital object **MUST** have a `session target` that **MUST** be named using this template <code><digi_id><b>_000001.tif</b></code>

### examples: ([template details](#template) below)  
  * session target and item images
    ```
    nyu_aco123456_0000001.tif  # this is the session target!
    nyu_aco123456_0000002.tif  # this is the first image  of the item
    nyu_aco123456_0000003.tif  # this is the second image of the item
    ...
    ```
  * EOC file:
    * `20160324-IQ260-EOC.csv`
    * `nyu_aco123456_eoc.csv`


### template
* generic template:
  * `<digi_id>_<sequence number>.tif`
    * `digi_id`: the `digitization id` assigned to the `digital object`
    * `sequence number`: an integer padded with leading-zeros as needed,  
    e.g., `000007`, that indicates the order of the corresponding page in the item  

#### specific templates
* **session target:**
  * <code><digi_id><b>_000001.tif</b></code>

* **EOC file:**
  * the following are valid EOC templates:
    * template: <code>&lt;digitization station name&gt;<b>-EOC.csv</b></code>
    * template: <code>&lt;digitization station name&gt;<b>_EOC.csv</b></code>
    * template: <code>&lt;digitization station name&gt;<b>_eoc.csv</b></code>
    * template: <code><digi_id><b>_eoc.csv</b></code>

### requirements:
* all digital objects created with the `bookeye` workflow **MUST** include an EOC file.  
  (Without an EOC file, there is no way to differentiate between `access`-workflow   
   digital objects and a `bookeye`-workflow digital objects.)

* all filenames must be numbered sequentially
  * i.e., 
    ```
    # GOOD
    ...
    nyu_aco001143_000123.tif
    nyu_aco001143_000124.tif
    nyu_aco001143_000125.tif
    ...

    # BAD (missing 000724)
    ...
    nyu_aco001143_000723.tif
    nyu_aco001143_000725.tif
    nyu_aco001143_000726.tif
    ...
    ```

