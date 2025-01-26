Skeleton

`
```
import requests import get
import json
import argparse

# Nice way to notify user you have an APIError
class APIError(Exception):
    """Describes an error triggered by a failing API call."""

    def __init__(self, message: str, code: int = 500):
        """Creates a new APIError instance."""
        self.message = message
        self.code = code

	
def fetch_data(country_name: str) -> dict:
    """Returns a dict of country data from the API."""
	# This is what gets the information:
    response = get(f"https://restcountries.com/v3.1/name/{country_name}")
    
	# Checking for response codes:
    if response.status_code == 404:
        raise APIError("Unable to locate matching country.", code=404)
    if response.status_code == 500:
        raise APIError("Unable to connect to server.", code=500)
    if response.status_code != 200:
        raise APIError(
            f"Unexpected error occured. Status code: {response.status_code}", code=response.status_code)

	# This shows you the info in json format
    info = response.json()
    
    # If you want to see the json of the information you got from the link in a nicer format:
    # print(json.dumps(info, indent=4))

	# Checking for multiple matches:
    if len(info) > 1:
        print("Countries found:")
        for idx, country in enumerate(info):
            print(f"{idx}: {country["name"]["official"]}")
        selected_country = input(
            "Please choose which number you want to select: ")

        if not selected_country.isnumeric():
            raise ValueError(
                "Please enter the number corresponding the country given above.")

        selected_country = int(selected_country)

        name = info[selected_country]["name"]["official"]
        flag = info[selected_country]["flag"]
        languages = info[selected_country]["languages"]
    else:
        name = info[0]["name"]["official"]
        flag = info[0]["flag"]
        languages = info[0]["languages"]
    return {
        "name": {
            "official": name
        },
        "flag": flag,
        "languages": languages
    }

```
`