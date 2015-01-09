# Exhibition

Contains information on past exhibitions as documentation of an object’s exhibition history and current and/or upcoming exhibitions.

## Get exhibitions

`GET /exhibition` will get all exhibitions affiliated with the museums collections.

Include one or more of the following parameters to filter the items.

| Parameter | Value |
| :--------- | :----- |
| apikey | YOUR API KEY required |
| q | FIELD:VALUE |
| size | 0-9+ |
| page | 0-9+ |
| sort | FIELD NAME or "random" or "random:[SEED NUMBER]" |
| sortorder | asc or desc |
| fields | comma separated list of data fields you want in the output |
| facet | FIELD NAME or comma separated list of fields |
| hasimage | 0 or 1 |
| facet | FIELD NAME or comma separated list of fields |
| venue | “HAM” |
| exact_title | EXACT URL ENCODED TITLE |
| before | YYYY-MM-DD or “begindate:YYYY-MM-DD” or “enddate:YYYY-MM-DD” or “temporalorder:1234” |
| after | YYYY-MM-DD or “begindate:YYYY-MM-DD” or “enddate:YYYY-MM-DD” or “temporalorder:1234” |

#### Examples

> http://api.harvardartmuseums.org/exhibition?venue=HAM  
> Returns all records for exhibitions that take place at a Harvard Art Museums venue. 

#### Response

```json
{
    "info": {
        "totalrecordsperquery": 10,
        "totalrecords": 462,
        "pages": 47,
        "page": 1
    },
    "records": [
        {
            "id": 225,
            "lastupdate": "2015-01-09T04:09:29-0500",
            "title": "Colors of the Caucasus",
            "temporalorder": 2740,
            "exhibitionid": 225,
            "primaryimageurl": null,
            "color": null,
            "description": null,
            "venues": [
                {
                    "ishamvenue": 1,
                    "venueid": 10615,
                    "name": "Harvard University Art Museums",
                    "zipcode": "02138",
                    "state": "MA",
                    "address1": "32 Quincy Street",
                    "address2": null,
                    "begindate": "1990-06-16",
                    "enddate": "1990-09-09",
                    "fullname": "Harvard University Art Museums",
                    "city": "Cambridge",
                    "country": null
                }
            ],
            "begindate": "1990-06-16",
            "enddate": "1990-09-09",
            "shortdescription": null
        },
        {
            "id": 249,
            "lastupdate": "2015-01-09T04:09:29-0500",
            "title": "David Smith: \"This work is my identity\"",
            "temporalorder": 2993,
            "exhibitionid": 249,
            "primaryimageurl": "http://nrs.harvard.edu/urn-3:huam:GS04997_dynmc",
            "color": null,
            "description": null,
            "venues": [
                {
                    "ishamvenue": 1,
                    "venueid": 10615,
                    "name": "Harvard University Art Museums",
                    "zipcode": "02138",
                    "state": "MA",
                    "address1": "32 Quincy Street",
                    "address2": null,
                    "begindate": "1995-06-03",
                    "enddate": "1996-05-05",
                    "fullname": "Harvard University Art Museums",
                    "city": "Cambridge",
                    "country": null
                }
            ],
            "begindate": "1995-06-03",
            "enddate": "1996-05-05",
            "shortdescription": null
        }
    ]
}
```

## Get exhibition

`GET /exhibition/EXHIBITION_ID` will get detailed info about a specific exhibition.

#### Examples

> http://api.harvardartmuseums.org/exhibition/4236  
> Returns the full record for the exhibition “In Harmony: The Norma Jean Calderwood Collection of Islamic Art”.

#### Response

```json
{
    "exhibitionid": 4236,
    "title": "In Harmony: The Norma Jean Calderwood Collection of Islamic Art",
    "begindate": "2013-01-31",
    "enddate": "2013-06-01",
    "description": "This special exhibition showcases some 150 works from the Norma Jean Calderwood Collection of Islamic Art. Largely unpublished and little known, the collection includes important objects from the Persian cultural sphere, such as luxury glazed ceramics of the early Islamic era, illustrated manuscripts of medieval epic poems, and lacquerware of the early modern era. Among the manuscripts are folios of the Shahnama, by Firdawsi, and the Khamsa, by Nizami. The accompanying catalogue, published by the Harvard Art Museums and distributed by Yale University Press, offers illustrated entries and nine essays written by distinguished scholars and conservation scientists from a broad range of specialties. Curated by Mary McWilliams, Norma Jean Calderwood Curator of Islamic and Later Indian Art, Division of Asian and Mediterranean Art, Harvard Art Museums.\r\nIn Harmony marks the first time the museums are using an augmented reality app called Layar in the galleries. The free app, available for iPhone, iPad, or Android devices, gives visitors access to audio, video, and web links for several objects on display. \r\n\r\nSpecial docent-led tours of the exhibition will be offered on Wednesdays, February 13–May 29, 2013. These tours start in the Sackler Museum lobby at 2pm, last approximately an hour, and are included with admission. Special notice: The docent tour of In Harmony on Wednesday, May 1, has been canceled.\r\nIn conjunction with Harvard's Arts First celebration, special talks by undergraduate students on selected artworks in the exhibition will be given on Saturday, April 27, 2013, 11am to noon and 1pm to 2pm. Please note that attendance for these talks is limited and included with admission.\r\nThis exhibition and its accompanying catalogue have been made possible through the generous support of the late Stanford Calderwood.",
    "shortdescription": "A brilliant display of some 150 objects from the Persian cultural sphere, including fine ceramics, illustrated manuscripts, drawings, and lacquerware.",
    "primaryimageurl": "http://nrs.harvard.edu/urn-3:HUAM:61350_dynmc",
    "color": "#DF7845",
    "temporalorder": 4378,
    "id": 4236,
    "lastupdate": "2015-01-09T04:09:30-0500",
    "media": [
        {
            "thumbnailimageurl": null,
            "fileurl": "http://vimeo.com/58571319",
            "publiccaption": "Recreation of a Medieval Ceramic Sweetmeat Dish from Kashan, Iran",
            "filetype": "Video File",
            "copyright": null,
            "renditionnumber": "VID0012"
        }
    ],
    "publications": [
        {
            "title": "In Harmony: The Norma Jean Calderwood Collection of Islamic Art",
            "primaryimageurl": null,
            "description": "<P>Mary McWilliams, with essays by Jessica Chloros and Katherine Eremin, Walter B. Denny, Penley Knipe, Oya Pancaroğlu, David J. Roxburgh, Sunil Sharma, Anthony B. Sigel, and Marianna Shreve Simpson<BR>ISBN 978-1-891771-62-0<BR>Available January 2013<BR>304 pages, 9 1/4 x 12 in.<BR>341 color illustrations<BR>Hardcover, $75.00<BR>With slipcase<BR>Published by the Harvard Art Museums<BR>Distributed by Yale University Press</P>\r\n<P>Winner, American Institute of Graphic Arts (AIGA) Best of New England (BoNE) 2013 Award</P>\r\n<P>A major philanthropist from the Boston area, Norma Jean Calderwood assembled an extensive collection of Islamic art, ranging from austere and powerful epigraphic ceramics of the 9th and 10th centuries to the introspective realism of late-19th-century portraiture. With more than ﬁfty pieces of ceramics, the collection represents every signiﬁcant period and technique in Persian pottery. It has particular strength in illustrations of the greatest epic poem in the Persian language, the Shahnama (Book of Kings) by Abu’l-Qasim Firdawsi, and also includes beautiful examples of album painting, drawing, and calligraphy.</P>\r\n<P>Nine essays by diverse experts explore issues of conservation as well as the cultural and historical signiﬁcance of various objects in this largely unpublished collection. Topics include the inﬂuence of calligraphic line and physical gesture on Safavid drawings; ﬁgurative imagery on Iranian ceramics; and what cobalt pigment reveals about an object’s origins.</P>\r\n<P>Mary McWilliams is Norma Jean Calderwood Curator of Islamic and Later Indian Art, Harvard Art Museums; Jessica Chloros is Assistant Objects Conservator, Isabella Stewart Gardner Museum; Walter B. Denny is Professor of Art History, University of Massachusetts, Amherst; Katherine Eremin is Patricia Cornwell Conservation Scientist, Straus Center for Conservation and Technical Studies, Harvard Art Museums; Penley Knipe is Philip and Lynn Straus Conservator of Works of Art on Paper, Straus Center for Conservation and Technical Studies, Harvard Art Museums; Oya Pancaroğlu is Associate Professor of History, Boğaziçi University; David J. Roxburgh is Prince Alwaleed Bin Talal Professor of Islamic Art History, Harvard University; Sunil Sharma is Associate Professor of Persianate and Comparative Literature, Boston University; Anthony B. Sigel is Conservator of Objects and Sculpture, Straus Center for Conservation and Technical Studies, Harvard Art Museums; and Marianna Shreve Simpson is an independent scholar.</P>",
            "publicationplace": "Cambridge, MA",
            "publicationyear": 2013,
            "format": "Exhibition Catalogue",
            "publicationid": 19939,
            "shortdescription": "<P>Mary McWilliams, with essays by Jessica Chloros and Katherine Eremin, Walter B. Denny, Penley Knipe, Oya Pancaroğlu, David J. Roxburgh, Sunil Sharma, Anthony B. Sigel, and Marianna Shreve Simpson</P>\r\n<P>Hardcover, $75.00</P>",
            "publicationdate": "2013"
        }
    ],
    "venues": [
        {
            "ishamvenue": 1,
            "zipcode": "02138",
            "name": "Arthur M. Sackler Museum",
            "venueid": 55780,
            "state": "MA",
            "address1": "485 Broadway",
            "address2": null,
            "enddate": "2013-06-01",
            "begindate": "2013-01-31",
            "fullname": "Harvard Art Museums",
            "country": "USA",
            "city": "Cambridge"
        }
    ]
}
```