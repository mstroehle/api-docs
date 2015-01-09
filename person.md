# Person

Contains information on entities that have some association to works of art in the collection.

## Get people

`GET /person` will get all people affiliated with the museums.

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

#### Examples

> http://api.harvardartmuseums.org/person?q=culture:Dutch 
> Finds all of the people with that are Dutch.    

#### Response

```json
{
    "info": {
        "totalrecordsperquery": 10,
        "totalrecords": 600,
        "pages": 60,
        "page": 1
    },
    "records": [
        {
            "dateend": 0,
            "alphasort": "Kaap, Gérald Van Der",
            "displaydate": "born 1959",
            "deathplace": null,
            "objectcount": 1,
            "id": 18135,
            "lastupdate": "2015-01-09T04:07:45-0500",
            "datebegin": 1959,
            "birthplace": "Enschede, Netherlands",
            "personid": 18135,
            "gender": "male",
            "culture": "Dutch",
            "displayname": "Gérald Van Der Kaap"
        },
        {
            "dateend": 1633,
            "alphasort": "Vinckboons, David",
            "displaydate": "1576 - 1632-1633",
            "deathplace": "Amsterdam",
            "objectcount": 9,
            "id": 18301,
            "lastupdate": "2015-01-09T04:07:45-0500",
            "datebegin": 1576,
            "birthplace": "Mechelen",
            "personid": 18301,
            "gender": null,
            "culture": "Dutch",
            "displayname": "David Vinckboons"
        }
    ]
}
```

## Get person

`GET /person/PERSON_ID` will get detailed info about a specific person.

#### Examples

> http://api.harvardartmuseums.org/person/28241  
> Returns the full record for Rembrandt.

#### Response

```json
{
    "personid": 28241,
    "displayname": "Rembrandt Harmensz van Rijn",
    "datebegin": 1606,
    "dateend": 1669,
    "displaydate": "1606 - 1669",
    "culture": "Dutch",
    "gender": null,
    "birthplace": "Leiden",
    "deathplace": "Amsterdam",
    "alphasort": "Rembrandt Harmensz van Rijn",
    "objectcount": 691,
    "id": 28241,
    "lastupdate": "2015-01-09T04:08:25-0500",
    "ulan_id": "500011051",
    "viaf_id": "64013650",
    "wikipedia_id": "4254144"
}
```