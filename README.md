# MLProcess - Air Quality Prediction

This repository contains information about Air Quality Prediction using Machine Learning approach.

## Dataset Information

- Dataset downloaded from: [here](https://www.kaggle.com/datasets/senadu34/air-quality-index-in-jakarta-2010-2021/data)
- Dataset description: \
This dataset contains the Air Quality Index (AQI) or Indeks Standar Pencemaran Udara (ISPU) measured from 5 air quality monitoring stations (SPKU) in DKI Jakarta from January 2021 to December 2021.

- Data Definition:

| **Variable** | **Type** | **Description**                                                                                                                                                               |
|--------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tanggal`    | string   | The date when the AQI measurement was recorded.                                                                                                                               |
| `stasiun`    | string   | The name or identifier of the monitoring station where the measurement was taken.                                                                                             |
| `pm25`       | integer  | The concentration of particulate matter with a diameter of 2.5 micrometers or less (PM2.5), measured in micrograms per cubic meter (µg/m³).                                   |
| `pm10`       | integer  | The concentration of particulate matter with a diameter of 10 micrometers or less (PM10), measured in micrograms per cubic meter (µg/m³).                                     |
| `so2`        | integer  | The concentration of sulfur dioxide (SO2), measured in parts per million (ppm).                                                                                               |
| `co`         | integer  | The concentration of carbon monoxide (CO), measured in parts per million (ppm).                                                                                               |
| `o3`         | integer  | The concentration of ozone (O3), measured in parts per million (ppm).                                                                                                         |
| `no2`        | integer  | The concentration of nitrogen dioxide (NO2), measured in parts per million (ppm).                                                                                             |
| `max`        | integer  | The maximum value recorded among the pollutants for that particular date and station. This value represents the highest concentration among PM25, PM10, SO2, CO, O3, and NO2. |
| `critical`   | string   | The pollutant that had the highest concentration for that date and station.                                                                                                   |
| `category`   | string   | The air quality category based on the 'max' value that describes the air quality level.                                                                                       |


## Flow Chart

(will be updated soon)

## Predict API (FastAPI)
### Endpoint

`POST` `/predict`

### Description

This API endpoint accepts pollutant values as input and returns the predicted air quality. 

### Request

**Not all variables used in the prediction process**. Below are the example.

```json
{
  "stasiun": "DKI1 (Bunderan HI)",
  "pm10": 38,
  "pm25": 53,
  "so2": 29,
  "co": 6,
  "o3": 31,
  "no2": 13
}
```

### Response

```json
{
  "category": 'TIDAK BAIK'
}
```

## Deploy Model in Local
### Prerequisites
- Make sure Python and PIP installed in your system (this project use Python 3.12.3 and PIP 24.0)
- Install the required packages from requirements.txt (you may use virtual environment for this)
```bash
pip install -r requirements.txt
```

### Running FastAPI App in Local
(will be updated soon)

**Last Update:** 24-06-2025
**Created By:** indraps30