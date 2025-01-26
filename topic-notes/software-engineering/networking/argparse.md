```
import requests
import json
import argparse

parser = argparse.ArgumentParser(description="finds the stadiums")
parser.add_argument("team", metavar="team", type=str, help="enter your team")
args = parser.parse_args()

team = args.team

url = 'https://url/of/api' - + team
response = requests.get(url)
data = response.json()
print(data["teams"][0]["strStadium"])
```