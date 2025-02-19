## Preservation Media Lab A/V naming template

### Current Template:
```
A/V File Naming Template (no "Content-Split", with "version" option): 

The naming template at the time of this writing is:

    <pc>_<ci>_<aoi>[<sis>][_<fs>][_<tv>]_<fr>.<fe>

where:
    pc  = partner code
    ci  = collection identifier
    aoi = archival object ID
    sis = source item sequence identifier, e.g., first tape of a set        [optional]
    fs  = file sequence, e.g., 000001 -> tape side A, 000002 -> tape side B [optional]
    tv  = take/version indicating different attempts at digitizing an asset [optional]
    fr  = file role, e.g., master, derivative maker (mezzanine)
    fe  = file extension


|--------------------------------------+-----------+----------+----------+---------+--------+------|
|                                      |           | source   |          |         |        |      |
|                                      |           | item     |          |         |        |      |
| file name                            | archival  | sequence | file     | take/   | file   | file |
|                                      | object    | id       | sequence | version | role   | ext  |
|--------------------------------------+-----------+----------+----------+---------+--------+------|
| tamwag_TAM-709_cuid168A_000001_d.wav | cuid168   | A        | 1        | n/a     | dmaker | wav  |
| tamwag_TAM-709_cuid168A_000001_m.wav | "         | "        | "        | "       | master | "    |
|                                      |           |          |          |         |        |      |
| tamwag_TAM-709_cuid168A_000002_d.wav | "         | "        | 2        | "       | dmaker | "    |
| tamwag_TAM-709_cuid168A_000002_m.wav | "         | "        | "        | "       | master | "    |
|                                      |           |          |          |         |        |      |
| tamwag_TAM-709_cuid168B_000001_d.wav | "         | B        | 1        | "       | dmaker | "    |
| tamwag_TAM-709_cuid168B_000001_m.wav | "         | "        | "        | "       | master | "    |
|                                      |           |          |          |         |        |      |
| tamwag_TAM-709_cuid168B_000002_d.wav | "         | "        | 2        | "       | dmaker | "    |
| tamwag_TAM-709_cuid168B_000002_m.wav | "         | "        | "        | "       | master | "    |
|                                      |           |          |          |         |        |      |
| fales_mss547_cuid41188_v1_m.mov      | cuid41188 | n/a      | n/a      | take 1  | master | mov  |
| fales_mss547_cuid41188_v1_d.mov      | "         | "        | "        | "       | dmaker | "    |
|                                      |           |          |          |         |        |      |
| fales_mss547_cuid41188_v2_m.mov      | "         | n/a      | n/a      | take 2  | master | mov  |
| fales_mss547_cuid41188_v2_d.mov      | "         | "        | "        | "       | dmaker | "    |
|--------------------------------------+-----------+----------+----------+---------+--------+------|
* the "take/version" field is used to differentiate digitization passes of the same source asset.
  v1 denotes the first  attempt at digitizing the asset
  v2 denotes the second attempt at digitizing the asset
  ...
```

##
### Legacy Template:
```
"Content-Split" File Naming Template: 

* JHOVE used to fail .wav files that were larger than 4 GB. [1]
  (https://wiki.dpconline.org/images/4/46/WAV_Assessment_v1.0.pdf)

  This file-size upper limit required content to be split
  so that the .wav files would pass JHOVE validation.

  Therefore, a "content split" indicator is present in the naming template.

Template:
<partner code>_<collection identifier>_<archival object ID>_<tape side>_<content split>_<file role>.<file extension>


Example: fales/mss326:

|-------------------------+----------+--------+-------+--------+------|
| file name               | archival |  tape  |content|  file  | file |
|                         |  object  |  side  | split |  role  | ext  |
|-------------------------+----------+--------+-------+--------+------|
| 326_0003_000001_A_d.wav | 326_0003 |   1    |   A   | dmaker | wav  |
| 326_0003_000001_A_m.wav |    "     |   "    |   "   | master |  "   |
|                         |          |        |       |        |      |
| 326_0003_000001_B_d.wav |    "     |   "    |   B   | dmaker |  "   |
| 326_0003_000001_B_m.wav |    "     |   "    |   "   | master |  "   |
|                         |          |        |       |        |      |
| 326_0003_000002_A_d.wav |    "     |   2    |   A   | dmaker |  "   |
| 326_0003_000002_A_m.wav |    "     |   "    |   "   | master |  "   |
|                         |          |        |       |        |      |
| 326_0003_000002_B_d.wav |    "     |   "    |   B   | dmaker |  "   |
| 326_0003_000002_B_m.wav |    "     |   "    |   "   | master |  "   |
|-------------------------+----------+--------+-------+--------+------|

[1] The JHOVE WAV validation module now accepts files larger than 4GB,   
    so the content does not need to be split. Therefore, the  
    "Content-Split" naming template is no longer used.
```
