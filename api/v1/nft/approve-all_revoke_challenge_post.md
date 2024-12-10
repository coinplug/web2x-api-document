NFT 전체 위임 해제를 위해 필요한 데이터를 전송하고, 응답값으로 참조 토큰을 받습니다. 

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "request_id": "d383c84e-bf5c-43e8-b0d7-2e23500d141b",
  "status": "COMPLETE",
  "results": {
    "transaction_gas_used": 115623,
    "finished_at": "2024-12-04T17:24:31+09:00",
    "transaction_fee": "0.009249840000000000",
    "transaction_hash": "0xed65b024b4d7703f148363c77ad209c803dd14cf6513cf3d8a41699dea0b5a52",
    "requested_at": "2024-12-04T08:24:26+09:00"
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
    "request_id": "d383c84e-bf5c-43e8-b0d7-2e23500d141b",
    "status": "COMPLETE",
    "results": {
        "transaction_gas_used": 115623,
        "finished_at": "2024-12-04T17:24:31+09:00",
        "transaction_fee": "0.009249840000000000",
        "transaction_hash": "0xed65b024b4d7703f148363c77ad209c803dd14cf6513cf3d8a41699dea0b5a52",
        "requested_at": "2024-12-04T08:24:26+09:00"
    }
}
```

</details>
