갤러리 템플릿 배포를 위해 필요한 데이터(템플릿 이름 등)를 전송하고, 응답값으로 참조 토큰을 받습니다.

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
# contract_id 필드는 배포된 갤러리 템플릿의 식별자이며 템플릿을 사용하는 API에서 필요합니다. 
{
  "request_id": "d6721761-88eb-4c03-ab87-6a9dd3110793",
  "status": "COMPLETE",
  "results": {
    "contract": {
      "symbol": "W2G",
      "network_chain_id": 12,
      "contract_id": "c5ee0db0-4ce8-4219-befb-0b808afb41a9",
      "name": "WEB2X GALLERY",
      "ids": [],
      "owner_address": "0x1214Ae02C495E96Fd102705FA3c00721fbD52BC9",
      "contract_address": "0xe83687e545bbf90ce8b9507504460b8e85a737b7"
    },
    "transaction_hash": "0xa07dc6dae156eada4c7417cad2fde60e08323a2f12c3cc0215dc81ceb1bc4d23",
    "transaction_gas_used": 3083774,
    "transaction_fee": "0.239949336000000000",
    "requested_at": "2024-07-16T23:44:01+09:00",
    "finished_at": "2024-07-17T08:44:06+09:00"
  }
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
# contract_id 필드는 배포된 갤러리 템플릿의 식별자이며 템플릿을 사용하는 API에서 필요합니다. 
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "d6721761-88eb-4c03-ab87-6a9dd3110793",
    "status": "COMPLETE",
    "results": {
        "contract": {
            "symbol": "W2G",
            "network_chain_id": 12,
            "contract_id": "c5ee0db0-4ce8-4219-befb-0b808afb41a9",
            "name": "WEB2X GALLERY",
            "ids": [],
            "owner_address": "0x1214Ae02C495E96Fd102705FA3c00721fbD52BC9",
            "contract_address": "0xe83687e545bbf90ce8b9507504460b8e85a737b7"
        },
        "transaction_hash": "0xa07dc6dae156eada4c7417cad2fde60e08323a2f12c3cc0215dc81ceb1bc4d23",
        "transaction_gas_used": 3083774,
        "transaction_fee": "0.239949336000000000",
        "requested_at": "2024-07-16T23:44:01+09:00",
        "finished_at": "2024-07-17T08:44:06+09:00"
    }
}
```

</details>
