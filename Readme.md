## General scheme.

![](https://github.com/otus-sre-lessons/homework3-n8n-calendar-comparison/blob/main/assets/scheme.png?raw=true)



## Data format.

```
{
    "year": 2022,
    "months":
    {
        "m01": "1,2,3,4,5,6,7,8,9,15,16,22,23,29,30",
        "m02": "5,6,12,13,19,20,22*,23,26,27",
        "m03": "5*,6,7+,8,12,13,19,20,26,27",
        "m04": "2,3,9,10,16,17,23,24,30",
        "m05": "1,2+,3+,7,8,9,10+,14,15,21,22,28,29",
        "m06": "4,5,11,12,13+,18,19,25,26",
        "m07": "2,3,9,10,16,17,23,24,30,31",
        "m08": "6,7,13,14,20,21,27,28",
        "m09": "3,4,10,11,17,18,24,25",
        "m10": "1,2,8,9,15,16,22,23,29,30",
        "m11": "3*,4,5,6,12,13,19,20,26,27",
        "m12": "3,4,10,11,17,18,24,25,31"
    },
    "statistics":
    {
        "workdays": 247,
        "holidays": 118,
        "hours40": 1973,
        "hours36": 1775.4,
        "hours24": 1182.6
    }
}
```


## Checking for matching data values.

By default, json-data and csv-data are matching.

![](https://github.com/otus-sre-lessons/homework3-n8n-calendar-comparison/blob/main/assets/scheme_for_matchig_data.png)

Example of a sent message:

![](https://github.com/otus-sre-lessons/homework3-n8n-calendar-comparison/blob/main/assets/tlg_msg_for_matching_data.png)


## Checking for mismatching data values.

Breaking the data in the json block a little.
Step by step...

![](https://github.com/otus-sre-lessons/homework3-n8n-calendar-comparison/blob/main/assets/breaking_data_01.png)

![](https://github.com/otus-sre-lessons/homework3-n8n-calendar-comparison/blob/main/assets/breaking_data_02.png)

![](https://github.com/otus-sre-lessons/homework3-n8n-calendar-comparison/blob/main/assets/breaking_data_03.png)

Runinig workflow again and checking result.

![](https://github.com/otus-sre-lessons/homework3-n8n-calendar-comparison/blob/main/assets/scheme_for_mismatchig_data.png)

Example of a sent message:

![](https://github.com/otus-sre-lessons/homework3-n8n-calendar-comparison/blob/main/assets/tlg_msg_for_mismatching_data.png)
