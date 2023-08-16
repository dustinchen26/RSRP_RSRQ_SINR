# MeasurementReport Calculator
online calculate: https://dustinchen26.github.io/RSRP_RSRQ_SINR

## Description
```
● NR MeasurementReport
Ref: ETSI TS 138 331 V16.1.0 (2020-07)
> input RSRP-Range ::= INTEGER(0..127), the actual value is (IE value – 156) dBm. except for the IE value 127, in which case the actual value is infinity. 
> input RSRQ-Range ::= INTEGER(0..127), the actual value is (IE value – 87) / 2 dB.
> input SINR-Range ::= INTEGER(0..127), the actual value is (IE value – 46) / 2 dB.

● LTE MeasurementReport
Ref: ETSI TS 136 331 V15.3.0 (2018-10)
> input RSRP-Range ::= INTEGER(0..97), For RSRP: RSRP based threshold for event evaluation. The actual value is field value – 140 dBm.
> input RSRQ-Range ::= INTEGER(0..34), For RSRQ: RSRQ based threshold for event evaluation. The actual value is (field value – 40)/2 dB.
> input RS-SINR-Range-r13 ::= INTEGER(0..127), For RS-SINR: RS-SINR based threshold for event evaluation. The actual value is (field value -46)/2 dB.
```
## Example
```
nr-rsrp: 113
nr-rsrq: 66
nr-sinr: 93

Calculate
actual value RSRP = -43 dBm
actual value RSRQ = -10.5 dB
actual value SINR = 23.5 dB
```