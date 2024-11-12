# ESPNFantasyFootballAnalysis
`pip install espnfantasyfootball`

### Security Requirements
You will need to find your _league_id_ as well as the _swid_ and _espn_s2_ cookie parameters for your league. The league_id is found in the URL of your fantasy league:

<p align="center">
  <img width="832" alt="Screenshot 2023-06-07 at 11 52 16 AM" src="https://github.com/tbryan2/espnfantasyfootball/assets/29851231/2d40e807-644c-4423-bb70-5862c3fdd295">
</p>

To find the swid and espn_s2 cookie parameters, go to you any page on your fantasy league's website. Right click on the page and hit __Inspect Element__. Locate the _Storage_ tab in your browser's developer tools and find _Cookies_. Locate these two cookie parameters and copy them into a secrets.py file to be imported later.

## FantasyLeague
Create a FantasyLeague object by importing the package and instantiating the class:
```
import espnfantasyfootball as espn
import pandas as pd
import secrets

league = espn.FantasyLeague(league_id=730129, year=2022,
                            swid=secrets.swid, espn_s2=secrets.espn_s2)
```
