# Dataframe: `hw2:fed_funds_futures` - 30-Day Fed Funds Futures

Daily open, high, low, close, and volume for every listed 30-Day Fed Funds futures contract, pulled from the Databento GLBX.MDP3 (CME Globex) dataset with the ohlcv-1d schema and the parent symbol ZQ.FUT. Each row is one contract on one trading date. The symbol column includes calendar spreads (e.g. ZQU6-ZQZ6) as well as outright monthly contracts (e.g. ZQU6); keep only the outrights with fedwatch.filter_outright_contracts. A contract settles at 100 minus the average daily effective fed funds rate over its month, so 100 - close is the market's forecast of that average.


## DataFrame Glimpse

```
Rows: 11653
Columns: 7
$ date   <datetime[ns]> 2026-10-25 00:00:00
$ symbol          <str> 'ZQG7-ZQJ7'
$ open            <f64> 15.5
$ high            <f64> 16.0
$ low             <f64> 15.5
$ close           <f64> 16.0
$ volume          <u64> 333


```

## Dataframe Manifest

| Dataframe Name                 | 30-Day Fed Funds Futures                                                          |
|--------------------------------|--------------------------------------------------------------------------------------|
| Dataframe ID                   | [fed_funds_futures](../dataframes/hw2/fed_funds_futures.md)                                       |
| Sources                        | CME Group                                          |
| Providers                      | Databento                                        |
| Provider Links                 | https://databento.com/                                   |
| Tags                           | Monetary Policy, Futures, Fed Funds                                             |
| Access Types                   |                                       |
| How is data pulled?            | Databento API via Python                                                   |
| Data available up to (min)     | 2026-10-25 00:00:00                                                             |
| Data available up to (max)     | 2026-10-25 00:00:00                                                             |
| Dataframe Path                 | C:\Users\czale\Desktop\UChicago\I. Classes\1. First Quarter\FINM 32800_Data Pipelines for QR\hw0\Homeworks\hw2-alexcruzj\_data\fed_funds_futures.parquet                                             |


**Linked Charts:**


- [hw2:fedwatch_latest_forecast](../../charts/hw2.fedwatch_latest_forecast.md)



## Pipeline Manifest

| Pipeline Name                   | HW 2: The Yield Curve and the Policy Path                       |
|---------------------------------|--------------------------------------------------------|
| Pipeline ID                     | [hw2](../../../index.md)              |
| Maintainer                      | Jeremiah Bejarano               |
| Contributors                    | Jeremiah Bejarano |
| Repository                     | https://github.com/hw-finm-32800/hw2                  |
| Pipeline Web Page               | <a href="file://C:/Users/czale/Desktop/UChicago/I. Classes/1. First Quarter/FINM 32800_Data Pipelines for QR/hw0/Homeworks/hw2-alexcruzj/docs/index.html">Pipeline Web Page      |
| Date of Last Code Update        | 2026-10-27 01:07:57           |
| OS Compatibility                | Windows, Linux, macOS |
| Linked Dataframes               |  [hw2:crsp_treasury_consolidated](../../dataframes/hw2/crsp_treasury_consolidated.md)<br>  [hw2:fed_yield_curve](../../dataframes/hw2/fed_yield_curve.md)<br>  [hw2:fed_funds_futures](../../dataframes/hw2/fed_funds_futures.md)<br>  |


**Build Commands:**
```
doit

```

