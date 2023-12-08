## Preservation Media Lab A/V naming template

### Current Template:
```
A/V File Naming Template (no "Content-Split"): 

The naming template at the time of this writing is:
<partner code>_<collection identifier>_<archival object ID><source item sequence identifier>_<file sequence, e.g., side A>_<file role>.<file extension>

|--------------------------------------+----------+----------+----------+--------+------|
|                                      |          |  source  |          |        |      |
|                                      |          |   item   |          |        |      |
| file name                            | archival | sequence |   file   |  file  | file |
|                                      |  object  |    id    | sequence |  role  | ext  |
|--------------------------------------+----------+----------+----------+--------+------|
| tamwag_TAM-709_cuid168A_000001_d.wav | cuid168  |    A     |    1     | dmaker | wav  |
| tamwag_TAM-709_cuid168A_000001_m.wav |    "     |    "     |    "     | master |  "   |
|                                      |          |          |          |        |      |
| tamwag_TAM-709_cuid168A_000002_d.wav |    "     |    "     |    2     | dmaker |  "   |
| tamwag_TAM-709_cuid168A_000002_m.wav |    "     |    "     |    "     | master |  "   |
|                                      |          |          |          |        |      |
| tamwag_TAM-709_cuid168B_000001_d.wav |    "     |    B     |    1     | dmaker |  "   |
| tamwag_TAM-709_cuid168B_000001_m.wav |    "     |    "     |    "     | master |  "   |
|                                      |          |          |          |        |      |
| tamwag_TAM-709_cuid168B_000002_d.wav |    "     |    "     |    2     | dmaker |  "   |
| tamwag_TAM-709_cuid168B_000002_m.wav |    "     |    "     |    "     | master |  "   |
|--------------------------------------+----------+----------+----------+--------+------|
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