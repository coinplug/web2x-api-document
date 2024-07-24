입장권 템플릿 배포\*를 위해 필요한 데이터(이름, 심볼)를 전송하고, 응답값으로 참조 토큰을 받습니다.

- 입장권 템플릿의 owner 는 wallet_id 필드의 주소로 지정됩니다.
- 입장권 템플릿의 default_data 는 빈문자열("") 로 지정됩니다.

\* 입장권 템플릿 배포: 입장권 발행을 위해 입장권 정보를 담아 템플릿을 배포 (블록체인 상 토큰 발행 정보를 담은 컨트랙트를 배포하는 단계, 배포 후 수정 불가)

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
# contract_id 필드는 배포된 NFT 컨트랙트의 식별자이며 컨트랙트를 사용하는 API에서 필요합니다.
{
  "request_id": "e63623c7-3082-4d1b-9756-6bfdd23bb325"
  "status": "COMPLETE",
  "results": {
    "contract": {
      "symbol": "YYFT",
      "network_chain_id": 12,
      "contract_id": "4f805512-e56d-41fe-b107-8929d5835f36",
      "name": "YYFT",
      "ids": [],
      "owner_address": "0x1214Ae02C495E96Fd102705FA3c00721fbD52BC9",
      "contract_address": "0xe62dcfefa9ec4304d1307b125725116ba9d06787",
      "is_burnable": true
    },
    "transaction_hash": "0x383d3b710c9ef94f25471f54db488e0687275f9abae75e3079b5179533ef86d3",
    "transaction_gas_used": 2210130,
    "requested_at": "2024-07-16T23:49:43+09:00",
    "finished_at": "2024-07-17T08:49:48+09:00"
  }
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
# contract_id 필드는 배포된 NFT 컨트랙트의 식별자이며 컨트랙트를 사용하는 API에서 필요합니다.
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "e63623c7-3082-4d1b-9756-6bfdd23bb325",
    "status": "COMPLETE",
    "results": {
        "contract": {
            "symbol": "YYFT",
            "network_chain_id": 12,
            "contract_id": "4f805512-e56d-41fe-b107-8929d5835f36",
            "name": "YYFT",
            "ids": [],
            "owner_address": "0x1214Ae02C495E96Fd102705FA3c00721fbD52BC9",
            "contract_address": "0xe62dcfefa9ec4304d1307b125725116ba9d06787",
            "is_burnable": true
        },
        "transaction_hash": "0x383d3b710c9ef94f25471f54db488e0687275f9abae75e3079b5179533ef86d3",
        "transaction_gas_used": 2210130,
        "requested_at": "2024-07-16T23:49:43+09:00",
        "finished_at": "2024-07-17T08:49:48+09:00"
    }
}
```

</details>
