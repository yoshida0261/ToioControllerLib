# ToioControllerLib


# cheat sheet

# UUID

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



# ID Information / 読み取りセンサー

Todo

# Sensor Information / モーションセンサー

| index | type | description | value |
| --- | --- |--- |--- |
| 0 | Uint8 | Type of information | 0x01(detection) |
| 1 | Uint8 | Horizontal detection | 0x00(Horizontal)<br> 0x01(Not horizontal) |
| 2 | Uint8 | Collision detection | 0x00(Not collision)<br> 0x01(collision) |

# Button Information / ボタン

Todo

# Battery Information / バッテリー

| index | type | description | value |
| --- | --- |--- |--- |
| 0 | Uint8 | The remaining battery capacity | 0x00 - 0x64 (Get in 10 steps) |


# Motor Control / モーター

## Type of information

- mortor controll 0x01 
- motor control with time setting 0x02

### mortor controll 0x01 

| index | type | description | value |
| --- | --- |--- |--- |
| 0 | Uint8 | Type of information | 0x01|
| 1 | Uint8 | controll id | 0x01(left) |
| 2 | Uint8 | direction | 0x01(advance) <br> 0x02(fall back) |
| 3 | Uint8 | motor speed | 0x00-0xff |
| 4 | Uint8 | controll id | 0x02(right) |
| 5 | Uint8 | direction | 0x01(advance) <br> 0x02(fall back) |
| 6 | Uint8 | motor speed | 0x00-0xff |


### motor control with time setting 0x02


| index | type | description | value |
| --- | --- |--- |--- |
| 0 | Uint8 | Type of information | 0x02|
| 1 | Uint8 | Controll id | 0x01(left) |
| 2 | Uint8 | Direction | 0x01(advance) <br> 0x02(fall back) |
| 3 | Uint8 | Motor speed | 0x00-0xff |
| 4 | Uint8 | Controll id | 0x02(right) |
| 5 | Uint8 | Direction | 0x01(advance) <br> 0x02(fall back) |
| 6 | Uint8 | Motor speed | 0x00-0xff |
| 7 | Uint8 | Control time | 0x00-0xff (0x00 : No time limit)|

#### motor speed

see https://toio.github.io/toio-spec/docs/ble_motor



# Light Control / ランプ

Todo

# Sound Control / サウンド

Todo

# Configuration / 設定

Todo
