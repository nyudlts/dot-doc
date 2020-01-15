## `born-digital` workflow naming template

### examples: ([template details](#template) below)

  * born-digital (`original`) file examples:
    * `AD_MC_025_ref72_000001_o.tif`
    * `AD_MC_025_ref118_000001_o.tif`
  * `dmaker` file examples:
    * `AD_MC_025_ref72_000001_d.tif`
    * `AD_MC_025_ref118_000001_d.tif`


### [Link to "Terms Used"](./README.md#terms-used)
### template
* generic template:
  * `<digi_id>_<sequence number>_<role>.tif`
    * `digi_id`: the `digitization id` assigned to the `digital object`,  
    or original identifier provided by the depositor.
    * `sequence number`: an integer padded with leading-zeros as needed,  
    e.g., `000007`, that indicates the order of the corresponding image in the item  
    * `role`: the role of the file, e.g., `original`, `dmaker`
      * use `_o` for `original` files
      * use `_d` for `dmaker` files

### requirements:
* all filenames must be numbered sequentially
  * i.e., 
    ```
    # GOOD
    AD_MC_025_ref72_000001_d.tif
    AD_MC_025_ref72_000001_o.tif
    AD_MC_025_ref72_000002_d.tif
    AD_MC_025_ref72_000002_o.tif
    AD_MC_025_ref72_000003_d.tif
    AD_MC_025_ref72_000003_o.tif
    ...

    # BAD 
    AD_MC_025_ref72_000001_d.tif
    AD_MC_025_ref72_000001_o.tif 
    AD_MC_025_ref72_000002_o.tif # missing dmaker for 000002
    AD_MC_025_ref72_000003_d.tif
    AD_MC_025_ref72_000003_o.tif
    ...
    ```
