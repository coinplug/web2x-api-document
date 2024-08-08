시즌권 템플릿 배포\*를 위해 필요한 데이터(이름, 심볼)을 전송하고, 응답값으로 참조 토큰을 받습니다. 

- 시즌권 템플릿의 owner 는 wallet_id 필드의 주소로 지정됩니다.
- 시즌권 템플릿의 default_data 는 빈문자열("") 로 지정됩니다.

\* 시즌권 템플릿 배포: 시즌권 발행을 위해 시즌권 정보를 담아 템플릿을 배포 (블록체인 상 토큰 발행 정보를 담은 컨트랙트를 배포하는 단계, 배포 후 수정 불가)

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
# contract_id 필드는 배포된 NFT 컨트랙트(템플릿)의 식별자이며 컨트랙트를 사용하는 API에서 필요합니다.
{
  "request_id": "52e657ee-cc9b-4b7f-b5e7-2e05477ecbaa",
  "status": "COMPLETE",
  "results": {
    "contract": {
      "symbol": "SEASON",
      "network_chain_id": 12,
      "contract_id": "b658c99f-3e44-46c9-8a29-71caa9711e65",
      "name": "EXCHANGE",
      "ids": [],
      "owner_address": "0x1214Ae02C495E96Fd102705FA3c00721fbD52BC9",
      "contract_address": "0x3bfd79fe7a70f24d0ed5e38c1f7e10da76896cdb",
      "is_burnable": true
    },
    "transaction_hash": "0x7442ed2bbf599c9ad8391ca08330ade641308c07d6445e498f38479364ae6610",
    "transaction_gas_used": 2241774,
    "requested_at": "2024-07-16T23:51:48+09:00",
    "finished_at": "2024-07-17T08:51:50+09:00"
  }
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
# contract_id 필드는 배포된 NFT 컨트랙트(템플릿)의 식별자이며 컨트랙트를 사용하는 API에서 필요합니다.
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "52e657ee-cc9b-4b7f-b5e7-2e05477ecbaa",
    "status": "COMPLETE",
    "results": {
        "contract": {
            "symbol": "SEASON",
            "network_chain_id": 12,
            "contract_id": "b658c99f-3e44-46c9-8a29-71caa9711e65",
            "name": "EXCHANGE",
            "ids": [],
            "owner_address": "0x1214Ae02C495E96Fd102705FA3c00721fbD52BC9",
            "contract_address": "0x3bfd79fe7a70f24d0ed5e38c1f7e10da76896cdb",
            "is_burnable": true
        },
        "transaction_hash": "0x7442ed2bbf599c9ad8391ca08330ade641308c07d6445e498f38479364ae6610",
        "transaction_gas_used": 2241774,
        "requested_at": "2024-07-16T23:51:48+09:00",
        "finished_at": "2024-07-17T08:51:50+09:00"
    }
}
```

</details>
