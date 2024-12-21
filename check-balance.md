## Query balance interface
Query user balance and price

## Interface call
### `POST` `/openapi/tron/energy/user/config`
**The following parameters with `*` are required, and those without `*` are optional**

Request Body

| Name                                   | Type   | Description    |
|----------------------------------------|--------|----------------|
| apiKey<span style="color:red">*</span> | String | apiKey applied by the user    |


Response Body
```JSON
{
  "code": 0,
  "msg": "success",
  "data": {
    "userInfo": {
      "balance": 2790.785, //Account balance
      "state": 1, //User status
      "username": "" //Account name
    },
    "payConfig": { //Price configuration
      "energy": {
        "canPay": 1,
        "limit": {
          "min": 32000,
          "max": 63028
        },
        "priceConfig": {
          "1440": 85.0,
        }
      },
      "bandwidth": {
        "canPay": 1,
        "limit": {
          "min": 32000,
          "max": 0
        },
        "priceConfig": null
      }
    }
  },
  "totalCount": 0
}
```

## Call example
```bash
curl --silent --location 'https://app-api.trxdefi.ai/openapi/tron/energy/user/config' \
--header 'Content-Type: application/json' \
--data '{
   "apiKey": "11111"
}'

```

## Postman Example

![user_config.png](https://raw.githubusercontent.com/robertwan2088/TRXDeFi/refs/heads/main/readme/img/user_config.png)

