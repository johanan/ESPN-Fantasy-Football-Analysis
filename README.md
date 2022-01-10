# ESPN Fantasy Football Analysis
This has some data science methods to investigate the Fantasy Football league I am in. You can modify some settings for your own league. 

I would not have been able to get this far without reading Steven Morse's [posts](https://stmorse.github.io/journal/espn-fantasy-python.html). I highly recommend you start there.

## Getting Started
We need to setup the environment to get everything to work.

### Cookies and .env
First you will need some cookies from ESPN. Log into your league and then inspect the cookies that are set. You will need to pull out two values `swid, espn_s2` and set in the `.env` file.

Next, get your `league_id`. When you first log into your league it should be query parameter `leagueId`. Grab that and put it into the `.env` as `league_id`.

Finally, set the current year to whatever year you want to run the analysis on.

Example `.env`:

```shell
current_year=2021
league_id=YOUR_LEAGUE_ID
swid={GUID_HERE_INCLUDE_THE BRACKETS}
espn_s2=SUPER_LONG_VALUE HERE
```

### Python
Create the virtual env, activate it, and install everything.

```shell
python3 -m venv env
source ./env/bin/activate
python3 -m pip install -r ./requirements.txt
```