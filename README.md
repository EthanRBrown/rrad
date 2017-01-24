# Real, Random Address Data (RRAD)

This is a list of real, random addresses that geocode successfully (tested on Google's Geocoding API service).
The address data comes from the [OpenAddresses](https://openaddresses.io/) project, and all the addresses are in the public domain.  The
addresses are deliberately not linked to people or businesses; the only gaurantee is that they are real addresses that
geocode successfully.

The addresses were pulled from OpenAddress where the "Required attribute" field was present and not "Yes".  See "Attribution" below for a list of sources (also included in each data file).

## Usage

The data is packaged into randomly-ordered files of varying sizes:

| Filename                      | Address Count   | Size    |
| ----------------------------- | ---------------:| -------:|
| addresses-us-all.json         | 3,220           | 969k    |
| addresses-us-all.min.json     | 3,220           | 493k    |
| addresses-us-1000.json        | 1,000           | 304k    |
| addresses-us-1000.min.json    | 1,000           | 155k    |
| addresses-us-500.json         |   500           | 154k    |
| addresses-us-500.min.json     |   500           |  79k    |
| addresses-us-250.json         |   250           |  79k    |
| addresses-us-250.min.json     |   250           |  41k    |
| addresses-us-100.json         |   100           |  34k    |
| addresses-us-100.min.json     |   100           |  18k    |

Each package is an object with two properites, `addresses` and `attribution`.  `addresses` is an array of addresses, each of with
with the form:

    {
        "address1": "203 East Gwinnett Street",
        "address2": "",
        "city": "Savannah",
        "state": "GA",
        "postalCode": "31401",
        "coordinates": {
            "lat": 32.06637,
            "lng": -81.093895
        }
    },

For example, to get a random address:

    const addresses = require('./rrad/addresses-us-all.min.json').addresses
    const randomAddress = addresses[Math.floor(Math.random() * addresses.length)]

You may also install this package via npm, though it is a large package since it contains all the data sets.  Usage:

    npm install --save-dev rrad

Or

    yarn add -D rrad

Then, to get a random address:

    const rrad = require('rrad')
    const randomAddress = rrad.addresses[Math.floor(Math.random() * rrad.addresses.length)] 

## Attribution

All data collected from the [OpenAddresses](https://openaddresses.io/) project, and is in the public domain.  Original sources:

* City of Haddam (CT)
* Ciy of Hartford (CT)
* City of Lyme (CT)
* City of Manchester (CT)
* City of Watertown (CT)
* City of Avon (CT)
* Town of Fairfield (CT)
* City of Groton (CT)
* Office of Geographic Information (MassGIS), Commonwealth of Massachusetts, MassIT (MA)
* VT Enhanced 911 Board, VCGI (VT)
* City of Huntsville (AL)
* City of Montgomery (AL)
* Shelby County (AL)
* Talladega County (AL)
* City of Fayetteville (AR)
* Arkansas Geographic Information Office (AR)
* City of Washington (DC)
* Bay County (FL)
* Brevard County (FL)
* Charlotte County (FL)
* Citrus County (FL)
* Clay County (FL)
* Highlands County, FL (FL)
* Hillsborough County (FL)
* City of Savannah (GA)
* Gordon County (GA)
* Muscogee County (GA)
* Sumter County (GA)
* Metro Louisville,  LOJIC partners (KY)
* Anne Arundel County (MD)
* City of Baltimore (MD)
* Frederick County (MD)
* Oklahoma and Logan Counties - Association of Central Oklahoma Governments (OK)
* Kern, Cleveland, Canadian, Logan Counties (OK)
* City of Nashville (TN)
* Cooke,Fannin,Grayson Counties - Texoma Council of Governments (TX)
* Municipality of Anchorage (AK)
* Copyright © 2015 Kenai Peninsula Borough (AK)
* Matanuska-Susitna Borough (AK)
* City of Glendale (AZ)
* City of Mesa (AZ)
* Alameda County (CA)
* Amador County (CA)
* City of Berkeley (CA)
* Butte County (CA)
* City of Bakersfield (CA)
* City of Carson (CA)
* City of Cupertino (CA)
* City of Hayward and Fairview. Licensed for Public Use (CA)
* City of Mountain View (CA)
* City of Orange (CA)
* Contra Costa County (CA)
* El Dorando County (CA)
* Fresno County (CA)
* Humboldt County (CA)
* Kern County (CA)
* Kings County (CA)
* Lake County (CA)
* Lassen County (CA)
* Los Angeles County (CA)
* Madera County (CA)
* Marin County (CA)
* Merced County (CA)
* Mono County (CA)
* Monterey County (CA)
* Napa County (CA)
* County of Nevada, California (CA)
* Orange County (CA)
* City of Palo Alto (CA)
* County of Placer (CA)
* Secramento County (CA)
* San Bernardino County (CA)
* San Diego Geographic Information Source - JPA (CA)
* San Joaquin County (CA)
* San Luis Obispo County (CA)
* San Mateo County (CA)
* Santa Barbara County (CA)
* Santa Clara County (CA)
* Santa Cruz County (CA)
* Shasta County (CA)
* Solano County (CA)
* Sonoma County (CA)
* Stanislaus County (CA)
* Tuolumne County (CA)
* Yolo County (CA)
* Yuba County (CA)
* Arapahoe County (CO)
* Archuleta County (CO)
* City of Arvada (CO)
* City of Aurora (CO)
* City of Boulder (CO)
* City of Fort Collins (CO)
* City of Greeley (CO)
* City of Loveland (CO)
* City of Westminster (CO)
* Gilpin County (CO)
* Gunnison County (CO)
* Jefferson County (CO)
* Larimer County (CO)
* Mesa County (CO)
* Pitkin County (CO)
* Pubelo County (CO)
* San Miguel County (CO)
* City of Honolulu (HI)
