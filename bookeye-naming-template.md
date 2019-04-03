## `bookeye` workflow naming template
  * in the `bookeye` workflow:
    * no special naming conventions are used to denote front matter, numbered pages, or back matter
    * there is a `session master` that **MUST** be named using this template <code><digi_id><b>_000001.tif</b></code>

### examples: ([template details](#template) below)
  * `nyu_aco123456_0000001.tif`  # this is the session master!
  * `nyu_aco123456_0000002.tif`  # this is the first image  of the item
  * `nyu_aco123456_0000003.tif`  # this is the second image of the item

### template
  * generic template:
    * <code><digi_id><b>_</b><sequence number><b>.tif</b></code>
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
    * template: <code><digitization station name><b>-EOC.csv</b></code>
    * template: <code><digitization station name><code><b>_EOC.csv</b></code>
    * template: <code><digitization station name><code><b>_eoc.csv</b></code>
    * template: <code><digi_id><b>_eoc.csv</b></code>
