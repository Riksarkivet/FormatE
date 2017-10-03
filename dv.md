# Digital Video
| identifier | value
| --------- | -----
| generally | DV25
# overview
## audio coding
| DV                              | encoding        | channel | sampling | bitdepth | bitrate | locked | comment
| ------------------------------- | --------------- | ------- | -------- | -------- | ------- | ------ | -------
| basic                           | [LPCM](lpcm.md) | 2       | 48 kHz   | 16-bit   | 768 kibit/s per channel, 1.5 Mibit/s stereo | no  | Possible to lock audio using "1394" I/O. JVC Pro DV records audio locked at 48 kHz.
| basic                           | [LPCM](pcm.md)  | 2       | 44.1 kHz | 16-bit   | 706 kibit/s per channel, 1.4 Mibit/s stereo | no  | Accepts 44.1 kHz using "1394" I/O. Possible to lock audio using "1394" I/O.
| basic                           | [PCM](pcm.md)   | 4       | 32 kHz   | 12-bit   | 384 kibit/s per channel, 1.5 Mibit/s per 4 channels | no  | Possible to lock audio using "1394" I/O. JVC Pro DV records audio locked at 32 kHz.
| [D-7](dv/dvcpro.md) 25          | ?               | 2       | 48 kHz   | 16-bit   | ? | yes |
| [D-7](dv/dvcpro.md) 25          | ?               | 1       | 32 kHz   | 12-bit   | ? | yes | Analog spund track.
| [D-7](dv/dvcpro.md) 25          | ?               | 1       | 44.1 kHz | 16-bit   | ? | yes | Analog spund track.
| [D-7](dv/dvcpro.md) 50          | ?               | ?       | ?        | ?        | ? | ?   |
| [D-7](dv/dvcpro.md) 100/HD      | ?               | ?       | ?        | ?         | ? | ?   |
| [D-7](dv/dvcpro.md) Progressive | [PCM](pcm.md)   | 4       | 48 kHz   | 16-bit   | ? | ?   |
| [D-9](dv/s-9.md)                | [PCM](pcm.md)   | 4       | 48 kHz   | 16-bit   | ? | ?   |
| [D-9](dv/s-9.md) HD             | [PCM](pcm.md)   | 8       | 48 kHz   | 16-bit   | ? | ?   |
| Digital8                        | ?               | 2       | 48 kHz   | 16-bit   | ? | yes | Possible to lock audio using "1394" I/O.
| Digital8                        | ?               | 2       | 44.1 kHz   | 16-bit   | ? | yes | Accepts 44.1 kHz using "1394" I/O. Possible to lock audio using "1394" I/O.
| Digital8                        | ?               | 4       | 32 kHz   | 12-bit   | ? | yes | Possible to lock audio using "1394" I/O.
| DV CAM                          | ?               | 2       | 48 kHz   | 16-bit   | ? | yes | Possible that some VTR (Video Tape Recorder) allows unlocked recording using "1394" I/O.
| DV CAM                          | ?               | 2       | 44.1 kHz   | 16-bit   | ? | yes | Accepts 44.1 kHz using "1394" I/O. 
| DV CAM                          | ?               | 4       | 32 kHz   | 12-bit   | ? | yes |

## video coding
| DV    | [interlaced](interlaced.md) | filter                                                       | compression   | Mbit/s | subsampling           | subsampling          | bit depth  | bit depth |
| ----- | --------------------------- | ----------------------------------------------------------- | ------------- | ------ | ----------------------| -------------------- | ---------- | --------- |
|       |                             |                                                             |               |        | *NTSC (60hz 720x480)* | *PAL (50Hz 720x576)* | *chroma*   | *luma*    |
| basic | yes                         | [intra-frame](intra-frame.md), [inter-field](inter-frame.md) | [DCT](dct.md) | 25     | 4:1:1                 | 4:2:0                | 8-bit      | 8-bit     |
| [D-7](dv/dvcpro.md) 25 | yes        | [intra-frame](intra-frame.md), [inter-field](inter-frame.md) | [DCT](dct.md) | 25     | 4:1:1                 | 4:1:1                | 8-bit      | 8-bit     |
| [D-7](dv/dvcpro.md) 50 | yes        | ?                                                           | ?             | 50     | 4:2:2                 | 4:2:2                | ?          | ?         |
| [D-7](dv/dvcpro.md) 100/HD | yes    | ?                                                           | ?             | 40-100 | 4:2:2                 | 4:2:2                | ?          | ?         |
| [D-7](dv/dvcpro.md) Progressive | yes/no | ?                                                      | ?             | 25-50  | 4:2:0?                | 4:2:0?               | ?          | ?         |
| [D-9](dv/s-9.md) | yes              | ?                                                           | ?             | 50     | 4:2:2                 | 4:2:2                | ?          | ?         |
| [D-9](dv/s-9.md) HD | ?             | ?                                                           | ?             | 100    | ?                     | ?                    | ?          | ?         |
| Digital8 | ?                        | [intra-frame](intra-frame.md), [inter-field](inter-frame.md) | [DCT](dct.md) | 25     | 4:1:1                 | 4:2:0                | 8-bit      | 8-bit     |
| DV CAM | ?                          | [intra-frame](intra-frame.md), [inter-field](inter-frame.md) | [DCT](dct.md) | 25     | 4:1:1                 | 4:2:0                | 8-bit      | 8-bit     |

# container format

# specification
Relevant specifications are 1-2, 4-5?[1]

| source | published | reference | summary
| ------ | --------- | --------- | -
| IEC    | 20010619  | IEC 61834-1:1998 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 1: General specifications (v. 1) | Specifies the content, format and recording method of the data blocks forming the helical records on the tape. Describes the common specifications for cassettes, modulation method, magnetization and basic system data, for helical-scan digital video cassette recording system using 6,35 mm (1/4 inch) magnetic tape. Defines the electrical and mechanical characteristics of equipment which will provide for the interchangeability of recorded cassettes. This consolidated version consists of the first edition (1998) and its amendment 1 (2001). Therefore, no need to order amendment in addition to this publication. (125 pages)
| IEC    | 19980825  | IEC 61834-2 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 2: SD format for 525-60 and 625-50 systems (v. 1.0) | Specifies the content, format and recording method of the data blocks forming the helical records on the tape containing audio, video, and system data. It describes the specifications for the 525-line system with a frame frequency of 29,97 Hz and 625-line system with a frame frequency of 25,00 Hz. One video channel and two independent audio channels are recorded in the digital format. (249 pages)
| IEC    | 19991104  | IEC 61834-3 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 3: HD format for 1125-60 and 1250-50 systems (v. 1.0) | Establishes basic principles applicable to the next generation of digital video cassette recording systems for consumer use for the interest of both users and manufacturers. Specifies the content, format and recording method of the data blocks forming the helical records on the tape containing audio, video, and system data. Describes the specifications for the 1125-line system with a frame frequency of 30,00 Hz and the 1250-line system with a frame frequency of 25,00 Hz. (125 pages)s
| IEC    | 19980717  | IEC 61834-4 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 4: Pack header table and contents (v. 1.0) | Specifies the pack headers and the contents of packs which are applicable to the whole recording system of helical-scan digital video cassette using 6,35 mm magnetic tape. (189 pages)
| IEC    | 19980812  | IEC 61834-5 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 5: The character information system (v. 1.0) | Specifies the character information systems which is applicable to the whole recording system for helical-scan digital video cassettes using 6,35 mm magnetic tape. Provides the method of recording characters in many languages and provides easy operation for users. (99 pages)
| IEC    | 20000822  | IEC 61834-6 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 6: SDL format (v. 1.0) | Describes the format extension, using higher compression to increase recording time and reduce running costs for the digital video cassette recording system. (89 pages)
| IEC    | 20010309  | IEC 61834-7 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 7: EDTV2 format (v. 1.0) | Is an extension to the SD specification. Covers features for the recording and reproduction of EDTV2 signals. (25 pages)
| IEC    | 20010627  | 61834-8 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 8: PALplus format for the 625-50 system (v. 1.0) | Is an extension of the SD specification (SD mode) and covers the features necessary to enable a DVCR to record and reproduce PALplus signals. (25 pages)
| IEC    | 20010322  | IEC 61834-9 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 9: DVB format (v. 1.0) | Specifies the content, format and recording method for the data blocks forming the helical records on tape containing audio, video and system data. Describes the specifications for the recording of single DVB programmes. The DVB data is delivered to the digital video cassette recorder via a digital interface or by a built-in tuner (IRD). The DVB data consist of an MPEG2 transport stream containing one or more programmes. (81 pages)
| IEC    | 20010222  | IEC 61834-10 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 10: DTV format (v. 1.0) | Specifies the content, format and recording method for the data blocks forming the helical records on tape containing audio, video and system data. Describes the specifications for the recording of single DTV programmes. The contents of the corrigendum of June 2001 have been included in this copy. (81 pages)
| IEC    | 20080213  | IEC 61834-11 -- Recording - Helical-scan digital video cassette recording system using 6,35 mm magnetic tape for consumer use (525-60, 625-50, 1125-60 and 1250-50 systems) - Part 11: HDV format for 1080i and 720p systems (v. 1.0) | It specifies the content, format, and recording method of data blocks containing video, audio, and system data on the helical scan digital video cassettes using 6,35 mm tape as defined in IEC 61834-1 for recording MPEG-2 streaming HD signals. The main specifications shall be as defined in IEC 61834-9 and IEC 61834-10. Other information, such as details about MPEG-2 stream descriptors, trick play data, system data, etc., are defined in Clause 7. (108 pages)
# source
[1] Cf `Admin J. Wilt, the DV, "DVCAM & DVCPRO Formats,  Standards Documents", http://adamwilt.com/DV-tech.html#Standards (20170227).` and ` Library of Congress, "Sustainability of Digital Formats: Planning for Library of Congress Collections" § Format Description Categories, Digital Video Encoding (DV, DVCAM, DVCPRO), https://digitalpreservation.gov/formats/fdd/fdd000183.shtml#specs (20170227).`
