NFT 위임을 위해 필요한 데이터(위임할 토큰 id, 위임받을 주소 id 등)을 전송하고, 응답값으로 참조 토큰을 받습니다.

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "request_id": "ac7f1ec3-ae32-4cfd-9767-d10495f1ce9a"
  "status": "COMPLETE",
  "results": {
    "transaction_hash": "0xf174631f476cfb63f49f945c70e8d1db0fce39e009fe226f41b3bbdf172a5cd5",
    "transaction_gas_used": 118012,
    "requested_at": "2024-07-16T23:31:29+09:00",
    "finished_at": "2024-07-17T08:31:32+09:00"
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
  "request_id": "ac7f1ec3-ae32-4cfd-9767-d10495f1ce9a",
  "status": "COMPLETE",
  "results": {
    "transaction_hash": "0xf174631f476cfb63f49f945c70e8d1db0fce39e009fe226f41b3bbdf172a5cd5",
    "transaction_gas_used": 118012,
    "requested_at": "2024-07-16T23:31:29+09:00",
    "finished_at": "2024-07-17T08:31:33+09:00"
  }
}
```

</details>
