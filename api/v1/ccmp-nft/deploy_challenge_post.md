Wrapped NFT 배포를 위해 필요한 데이터를 전송하고, 응답값으로 참조 토큰을 받습니다.   
Wrapped NFT 를 배포할 체인 네트워크의 지갑으로 요청해야 합니다.
<br />
* Wrapped 컨트랙트: NFT를 내보낼 대상 체인네트워크에서 NFT 토큰을 관리하기 위한 NFT 컨트랙트입니다.

<p><br/></p>

<details/>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "request_id": "fcfb0390-9f64-4ba9-8c53-b748de1c4819",
  "status": "COMPLETE",
  "results": {
    "transaction_gas_used": 470643,
    "finished_at": "2024-12-04T17:05:47+09:00",
    "contract": {
      "symbol": "WCCMPNFT3",
      "network_chain_id": 11,
      "contract_id": "d6c2df09-51b2-4978-a296-41a5dde43bbb",
      "name": "Wrapped CCMP NFT3",
      "ids": [],
      "owner_address": "0x50e9Bdae45DBfc4D7f999F54a3742aE47F79a3D4",
      "contract_address": "0x4e0c3b10ac568735aba2e092003810b678c2f10e",
      "is_burnable": false
    },
    "transaction_fee": "0.037651440000000000",
    "transaction_hash": "0x6825a1308d64b1ed36b842113acc9ab9d1164dd320e37e9be53df7d94f472b91",
    "requested_at": "2024-12-04T08:05:44+09:00"
  }
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "fcfb0390-9f64-4ba9-8c53-b748de1c4819",
    "status": "COMPLETE",
    "results": {
        "transaction_gas_used": 470643,
        "finished_at": "2024-12-04T17:05:48+09:00",
        "contract": {
            "symbol": "WCCMPNFT3",
            "network_chain_id": 11,
            "contract_id": "d6c2df09-51b2-4978-a296-41a5dde43bbb",
            "name": "Wrapped CCMP NFT3",
            "ids": [],
            "owner_address": "0x50e9Bdae45DBfc4D7f999F54a3742aE47F79a3D4",
            "contract_address": "0x4e0c3b10ac568735aba2e092003810b678c2f10e",
            "is_burnable": false
        },
        "transaction_fee": "0.037651440000000000",
        "transaction_hash": "0x6825a1308d64b1ed36b842113acc9ab9d1164dd320e37e9be53df7d94f472b91",
        "requested_at": "2024-12-04T08:05:44+09:00"
    }
}
```

</details>
