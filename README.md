# ML_FINAL
data_train/{stn}.json ->
```
"{stnid} {date} {time(like "00:00")} {tot} {weekday} {working(0 or 1)} {holiday(0 or 1)} {rain} {temp} {moist} {sbi}"
```

data_datelist_test.txt -> date list for test, separated by breakline
data_datelist_train.txt -> date list for train, separated by breakline
data_dayfeature -> some features related to day, include "weekday", "working", "holiday"
data_stn_test_set.txt -> station for test
data_stn_tot.json -> station totoal bike mumber
```
{
  "statoin id": number
}
```
data_weather.json -> date weather data
```
{
  "date":
  {
    "hour("1" to "24")":
    {
      "temp": "(str)",
      "rain": "(str)",
      "moist": "(str)",
      "wind": "(str)"
    }
  }
}
```

