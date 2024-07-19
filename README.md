# allora-worker

# Bước 1
Chạy lệnh 

```
cd
rm -rf alloraworker.sh
wget https://raw.githubusercontent.com/wibucrypto2201/allora-worker/main/alloraworker.sh && chmod +x alloraworker.sh && ./alloraworker.sh
```
# Bước 2

Check status

```
  curl --location 'http://localhost:6000/api/v1/functions/execute' \
--header 'Content-Type: application/json' \
--data '{
    "function_id": "bafybeigpiwl3o73zvvl6dxdqu7zqcub5mhg65jiky2xqb4rdhfmikswzqm",
    "method": "allora-inference-function.wasm",
    "parameters": null,
    "topic": "1",
    "config": {
        "env_vars": [
            {
                "name": "BLS_REQUEST_PATH",
                "value": "/api"
            },
            {
                "name": "ALLORA_ARG_PARAMS",
                "value": "ETH"
            }
        ],
        "number_of_nodes": -1,
        "timeout": 2
    }
}'
```
