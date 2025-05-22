# ADJ v2 specification

General Info

```json
{
    "ports": {str:int},
    "addresses": {str:str},
    "units":{str:str},
    "message_ids": {str:int}
}
```

Boards list

```json
{
    str:str
}
```

Board

```json
{
    "board_id":uint16,
    "board_ip":str,
    "measurements":[str],
    "packets":[str]
}
```

Measurements file

```json
[{
        "id":str,
        "name":str,
        "type":str <uint8|uint16|uint32|uint64|int8|int16|int32|int64|float32|float64>,
        "podUnits":str <general_info/units>,
        "displayUnits":str <general_info/units>,
        "enumValues":[str],
        "above": {
            "safe": float64
            "warning": float64
        },
        "below": {
            "safe": float64
            "warning": float64
        },
        "out_of_range": [float64, float64]
}]
```

Packets file

```json
[{
        "id":uint16,
        "type":str,
        "name":str,
        "variables":[str]
}]
```
