# Learning-LR-WPAN
Larning IEEE 802.15.4 specification.

* MLME：MAC Sublayer Management Entity
* MCPS：MAC Common Part Sublayer
* PD　：PHY Data
* PLME：Physical Layer Management Entity
* SAP ：Service Access Point

### MAC Layer
The MAC sublayer provides two services.   
* MLME-SAP
* MCPS-SAP

https://postfiles.pstatic.net/MjAxNjExMThfMjc0/MDAxNDc5NDU0MzY0OTU0.S3nK6WZxtjCXZ0XHfbKYBvsf2DNnm1onGV4JdyG28Ogg.6E0W1iHGGbt1vCTvmK_eIT7s0vFzK9cJL3vVFsuGcu8g.JPEG.jjz0426/%EC%BA%A1%EC%B2%98.JPG?type=w966


#### MLME-SAP
|Name               |Request|Indication|Response|Confirm|Frame|
|-------------------|-------|----------|--------|-------|-----|
|MLME-ASSOCIATE     |O      |O♦        |O♦      |O      |Cmd(Association) <br> Data <br> Ack|
|MLME-DISASSOCIATE  |O      |O         |        |O      |Cmd(Deassociation notification) <br> Ack|
|MLME-BEACON-NOTIFY |       |O         |        |       |Beacon|
|MLME-GET           |O      |          |        |O      |- (For get PIB)|
|MLME-GTS           |O*     |O*        |        |O*     |Cmd(GTS) <br> Beacon <br> Ack|
|MLME-ORPHAN        |       |O♦        |O♦      |       |Cmd(Coordinator realignment) <br> Ack|
|MLME-RESET         |O      |          |        |O      |-|
|MLME-RX-ENABLE     |O      |          |        |O*     |-|
|MLME-SCAN          |O      |          |        |O      |Cmd(Beacon) <br> Cmd(Orphan notification) <br> Cmd(Coordinator realignment) <br> Beacon|
|MLME-COMM-STATUS   |       |O         |        |       |-|
|MLME-SET           |O      |          |        |O      |- (For get PIB)|
|MLME-START         |O♦     |          |        |O♦     |Beacon|
|MLME-SYNC          |O*     |          |        |       |-|
|MLME-SYNC-LOSS     |       |O         |        |       |-|
|MLME-POLL          |O      |          |        |O      |Cmd(Data)|

♦:optional for an RFD.   
*:optional for both device types (i.e., RFD and FFD).


#### MCPS-SAP
|Name       |Request|Indication|Confirm|Frame|
|-----------|---|---|---|---|
|MCPS-DATA  |○|○|○  |Data|
|MCPS-PURGE |○♦|○♦|-|-|

♦:optional for an RFD.   
*:optional for both device types (i.e., RFD and FFD).

### Phy Layer

#### PLME-SAP

|Name               |Request|Confirm|
|-------------------|-------|-------|
|PLME-CCA           |○|○|
|PLME-ED            |○|○|
|PLME-GET           |○|○|
|PLME-SET-TRX-STATE |○|○|
|PLME-SET           |○|○|


#### PD-SAP

|Name    |Request|Confirm|Infication|
|--------|-------|-------|----------|
|PD-DATA |○|○|○|
