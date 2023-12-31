# MeasurementReport Calculator
online calculate: https://dustinchen26.github.io/RSRP_RSRQ_SINR

## Spec
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
// QXDM log
1980/02/03 18:45:39.265	[0xB821]	UL_DCCH / MeasurementReport
                        resultsSSB-Cell 
                        {
                          rsrp 98,
                          rsrq 66,
                          sinr 93
                        }

// Enter
Input the QXDM [0xB821] UL_DCCH / MeasurementReport (rsrp/rsrq/sinr), and press the Calculate button to get the actual value
nr-rsrp: 98
nr-rsrq: 66
nr-sinr: 93

Calculate
actual value RSRP = -58 dBm
actual value RSRQ = -10.5 dB
actual value SINR = 23.5 dB

// rantcp-20230923-181708.pcap
resultsSSB-Cell
    rsrp: -59dBm <= SS-RSRP < -58dBm (98)
    rsrq: -10.5dB <= SS-RSRQ < -10.0dB (66)
    sinr: 23.0dB <= SS-SINR < 23.5dB (93)

```