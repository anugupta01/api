# COVID19-India API

A volunteer-driven, crowd-sourced database for COVID-19 stats & patient tracing in India.

[Source Code on Github](https://github.com/covid19india/api)

## API Documentation
Detailed documentation regarding the API end-points [can be found here](documentation/)


### JSON Endpoints

| Status        | Data                                                                         | URL                                                      |
| ------------- | ---------------------------------------------------------------------------- | -------------------------------------------------------- |
| :green_heart: | Patient Level : Raw Data Partition 1 (Till Apr 19)                           | https://api.covid19india.org/raw_data1.json              |
| :green_heart: | Patient Level : Raw Data Partition 2 (From Apr 20 to Apr 26)                 | https://api.covid19india.org/raw_data2.json              |
| :green_heart: | Patient Level : Raw Data Partition 3 (From Apr 27 to May 09)                 | https://api.covid19india.org/raw_data3.json              |
| :green_heart: | Patient Level : Raw Data Partition 4 (From May 10 to May 23)                 | https://api.covid19india.org/raw_data4.json              |
| :green_heart: | Patient Level : Raw Data Partition 5 (From May 24 to Jun 04)                 | https://api.covid19india.org/raw_data5.json              |
| :green_heart: | Patient Level : Raw Data Partition 6 (From Jun 05 to Jun 19)                 | https://api.covid19india.org/raw_data6.json              |
| :green_heart: | Patient Level : Raw Data Partition 7 (From Jun 20 to Jun 30)                 | https://api.covid19india.org/raw_data7.json              |
| :green_heart: | Patient Level : Raw Data Partition 8 (From Jul 01 to Jul 07)                 | https://api.covid19india.org/raw_data8.json              |
| :green_heart: | Patient Level : Raw Data Partition 9 (From Jul 08 to Jul 13)                 | https://api.covid19india.org/raw_data9.json              |
| :green_heart: | Patient Level : Raw Data Partition 10 (From Jul 14th onwards)                | https://api.covid19india.org/raw_data10.json             |
| :green_heart: | National Level :Time series, State-wise stats and Test counts                | https://api.covid19india.org/data.json                   |
| :green_heart: | State Level : has district-wise info                                         | https://api.covid19india.org/state_district_wise.json    |
| :green_heart: | State Level : Daily changes                                                  | https://api.covid19india.org/states_daily.json           |
| :green_heart: | State Level : Testing data                                                   | https://api.covid19india.org/state_test_data.json        |
| :green_heart: | National/State/District Level : Latest cumulative/daily counts               | https://api.covid19india.org/v4/data.json                |
| :green_heart: | National/State/District Level : Specific date cummulative/daily counts       | https://api.covid19india.org/v4/data-YYYY-MM-DD.json     |
| :green_heart: | National/State/District Level : Historical date-wise cumulative/daily counts | https://api.covid19india.org/v4/data-all.json            |
| :green_heart: | National/State Level: Timeseries _(different structure)_                     | https://api.covid19india.org/v4/timeseries.json          |
| :end:         | District Level : Daily changes                                               | https://api.covid19india.org/districts_daily.json        |
| :end:         | Raw Data (Partition 1 + Partition 2. Frozen after Apr 26th)                  | https://api.covid19india.org/raw_data.json               |
| :end:         | Deaths and Recoveries (Frozen after Apr 26th)                                | https://api.covid19india.org/deaths_recoveries.json      |
| :end:         | Travel history (No more updated)                                             | https://api.covid19india.org/travel_history.json         |

### CSV

Sometimes, having files in a spreadsheet format is more useful for analysts and scientists. We have provided the files as downloadable csv files at the following location.

| Data                 | URL                                                                    |
| -------------------- | ---------------------------------------------------------------------- |
| Google sheets in CSV | [https://api.covid19india.org/csv/](https://api.covid19india.org/csv/) |

> :rocket: Quick example : Apply the formula `=IMPORTDATA("https://api.covid19india.org/csv/latest/state_wise.csv")` in A1 cell of a Google Sheets to get the state data for analysis :)

## How this works

- Data in this repository is generated from Google Sheets (https://api.covid19india.org/csv)
- Volunteers collect data from trusted sources and update the sheet
- We use Github Actions to periodically fetch the data from the sheet to the repo
- Static json and csv files into the gh-pages repository
- gh-pages serve the json files just like a website

## License
This repository contains both the code that routinely fetches the data from Google Sheet and convert it into JSON files in the required format and the data itself (in the gh-pages branch). So, the content of this repository is licensed in two ways : Code and Data

License for Code (Consider this as everything in the `master` branch) : MIT License (Detailed in LICENSE_CODE.txt)  
License for Data (Consider this as everything in the `gh-ages` branch) : CC-BY-SA-4.0 License (Detailed in LICENSE_DATA.txt)

## Citation
You can cite us in your work in the following format  
```
@misc{covid19indiaorg2020tracker,
  author = {COVID-19 India Org Data Operations Group},
  title = {{Dataset for tracking COVID-19 spread in India}},
  howpublished = {Accessed on yyyy-mm-dd from \url{https://api.covid19india.org/}},
  year = 2020
}
```

## Contributing
- Contributions to new data formats and making the data fetch process mroe efficient are welcome. 
- Please create a GH issue and discuss your idea before working on the same.
- Report issues regarding [covid19india.org](https://www.covid19india.org) website in the [react-site repository](https://github.com/covid19india/covid19india-react/issues)
- DO NOT change anything in `gh-pages` branch directly as they get replaced automatically every 10 minutes.


## Quick Links

- [Telegram Group](https://telegra.ph/CoVID-19--India-Ops-03-24)
- [Sources Considered](https://telegra.ph/Covid-19-Sources-03-19)


-----


## Team Projects Using This API

- [COVID-19 INDIA TRACKER](https://www.covid19india.org/) (Main Dashboard)
- [covid19india.org Ops Telegram Channel](https://t.me/covid19indiaorg) (News and Announcements from covid19india.org Team)
- [covid19india.org Instant Updates](https://t.me/covid19indiaorg_updates) (Instant Updates of new cases added - from covid19india.org Team)

.............................................
