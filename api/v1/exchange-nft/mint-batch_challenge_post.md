교환권 대량발행을 위해 필요한 데이터를 전송하고, 응답값으로 참조 토큰을 받습니다.

- 발행된 교환권의 token_id는 최초 발행 시 0이며, 발행요청 시 마다 순차적으로 1씩 증가하는 값으로 지정됩니다. 
- (주의) 블록체인에 올라가는 data 필드들의 크기에 따라 네트워크 수수료가 부가되며, 크기가 클 경우 수수료가 더 많이 발생할 수 있습니다.
<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
# token_ids 필드는 발행된 NFT 토큰의 식별자이며 NFT 토큰을 사용하는 API에서 필요합니다.
{
  "request_id": "c5f76b60-34f5-476b-ad9e-b15f29bff67b",
  "status": "COMPLETE",
  "results": {
    "token_ids": [
      14,
      13
    ],
    "transaction_hash": "0xd7a3c99b746cf54ef61167f6304ac2fde785596df1519aa90a810e6316171207",
    "transaction_gas_used": 384141,
    "requested_at": "2024-07-16T23:15:42+09:00",
    "finished_at": "2024-07-17T08:15:46+09:00"
  }
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
# token_ids 필드는 발행된 NFT 토큰의 식별자이며 NFT 토큰을 사용하는 API에서 필요합니다.
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "c5f76b60-34f5-476b-ad9e-b15f29bff67b",
    "status": "COMPLETE",
    "results": {
        "token_ids": [
            14,
            13
        ],
        "transaction_hash": "0xd7a3c99b746cf54ef61167f6304ac2fde785596df1519aa90a810e6316171207",
        "transaction_gas_used": 384141,
        "requested_at": "2024-07-16T23:15:42+09:00",
        "finished_at": "2024-07-17T08:15:46+09:00"
    }
}
```

</details>
