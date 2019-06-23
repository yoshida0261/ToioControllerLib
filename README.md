# ToioControllerLib



# Characteristic

| Characteristic | UUID | Properties |
| --- | --- |--- |
| ID Information| 10B20101-5B3B-4571-9508-CF3EFCD7BBAE | Read, Notify | 
| Sensor Information | 10B20106-5B3B-4571-9508-CF3EFCD7BBAE | Read, Notify | 
| Button Information | 10B20107-5B3B-4571-9508-CF3EFCD7BBAE| Read, Notify | 
| Battery Information | 10B20108-5B3B-4571-9508-CF3EFCD7BBAE | Read, Notify | 
| Motor Control | 10B20102-5B3B-4571-9508-CF3EFCD7BBAE | 	Write without response | 
| Light Control | 10B20103-5B3B-4571-9508-CF3EFCD7BBAE | Write | 
| Sound Control | 10B20104-5B3B-4571-9508-CF3EFCD7BBAE | Write| 
| Configuration | 10B201FF-5B3B-4571-9508-CF3EFCD7BBAE | Write, Read, Notify| 



# ID Information / 読み取りセンサー (Read, Notify)

Todo

# Sensor Information / モーションセンサー (Read, Notify)

| index | type | description | value |
| --- | --- |--- |--- |
| 0 | Uint8 | Type of information | 0x01(detection) |
| 1 | Uint8 | Horizontal detection | 0x00(水平)<br> 0x01(水平ではない) |
| 2 | Uint8 | Collision detection | 0x00(衝突なし)<br> 0x01(衝突あり) |

# Button Information / ボタン (Read, Notify)

Todo

# Battery Information / バッテリー(Read, Notify)

| index | type | description | value |
| --- | --- |--- |--- |
| 0 | Uint8 | The remaining battery capacity | 0x00 - 0x64  |


# Motor Control / モーター (Write without response )

## Type of information

- モーター制御 0x01 
- 時間指定付きモーター制御 0x02

### モーター制御 0x01 

| index | type | description | value |
| --- | --- |--- |--- |
| 0 | Uint8 | Type of information | 0x01|
| 1 | Uint8 | Controll id | 0x01(左) |
| 2 | Uint8 | Direction | 0x01(前進) or <br> 0x02(後退) |
| 3 | Uint8 | Motor speed | 0x00-0xff |
| 4 | Uint8 | Controll id | 0x02(右) |
| 5 | Uint8 | Direction | 0x01(前進) or <br> 0x02(後退) |
| 6 | Uint8 | Motor speed | 0x00-0xff |


### 時間指定付きモーター制御 0x02


| index | type | description | value |
| --- | --- |--- |--- |
| 0 | Uint8 | Type of information | 0x02|
| 1 | Uint8 | Controll id | 0x01(左) |
| 2 | Uint8 | Direction | 0x01(前進) or <br> 0x02(後退) |
| 3 | Uint8 | Motor speed | 0x00-0xff |
| 4 | Uint8 | Controll id | 0x02(右) |
| 5 | Uint8 | Direction | 0x01(前進) or <br> 0x02(後退) |
| 6 | Uint8 | Motor speed | 0x00-0xff |
| 7 | Uint8 | Control time | 0x00-0xff (0x00 : 永続)|

#### motor speed

see https://toio.github.io/toio-spec/docs/ble_motor



# Light Control / ランプ (Write)

Todo

# Sound Control / サウンド (Write)

Todo

# Configuration / 設定 ( Write, Read, Notify)

Todo
