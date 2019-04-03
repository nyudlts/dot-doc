## `bookeye` workflow naming template
  * in the `bookeye` workflow:
    * no special naming conventions are used to denote front matter, numbered pages, or back matter
    * there is a `session master` that **MUST** be named using this template `<digi_id>_000001.tif`

### examples: ([template details](#template) below)
  * `nyu_aco123456_0000001.tif`  # this is the session master!
  * `nyu_aco123456_0000002.tif`  # this is the first image  of the item
  * `nyu_aco123456_0000003.tif`  # this is the second image of the item

### template
  * generic template:
    * `<digi_id>_<sequence number>.tif`
      * `digi_id`: the `digitization id` assigned to the `digital object`
      * `sequence number`: an integer padded with leading-zeros as needed,  
         e.g., `000007`, that indicates the order of the corresponding page in the item

  * EOC file:
    * `20160324-IQ260-EOC.csv`
    * `nyu_aco001871_eoc.csv`

#### specific templates
* **session target:**
  * <code><digi_id><b>_000001.tif</b></code>
* **EOC file:**
  * the following are valid EOC templates:
    * template: `<digitization station name>-EOC.csv`
    * template: `<digitization station name>_EOC.csv`
    * template: `<digitization station name>_eoc.csv`
    * template: `<digi_id>_eoc.csv`
