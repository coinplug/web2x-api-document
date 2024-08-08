NFT 발행을 위해 필요한 데이터(토큰 데이터, 수신자 지갑 id 등)을 전송하고, 응답값으로 참조 토큰을 받습니다.

- 발행된 NFT의 token_id는 최초 발행 시 0이며, 발행 시 마다 순차적으로 1씩 증가하는 값으로 지정됩니다.
- token_data 필드를 입력하지 않으면 템플릿의 default_data 필드 값으로 자동 지정됩니다.
- (주의) 블록체인에 올라가는 data 필드들의 크기에 따라 네트워크 수수료가 부가되며, 크기가 클 경우 수수료가 더 많이 발생할 수 있습니다.
<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
# token_id 필드는 발행된 NFT 토큰의 식별자이며 NFT 토큰을 사용하는 API에서 필요합니다.
{
  "request_id": "87e1afbe-9944-4733-a55b-07043cf7db42",
  "status": "COMPLETE",
  "results": {
    "token_id": 12,
    "transaction_hash": "0x78f4d7063397dd71639a7877876af7f161518679cb8f9df5ac75b1e3e37dac62",
    "transaction_gas_used": 243122,
    "transaction_fee": "0.239949336000000000",
    "requested_at": "2024-07-16T23:11:20+09:00",
    "finished_at": "2024-07-17T08:11:24+09:00"
  },
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
# token_id 필드는 발행된 NFT 토큰의 식별자이며 NFT 토큰을 사용하는 API에서 필요합니다.
{
  "code": "20000",
  "message": "SUCCESS",
  "request_id": "87e1afbe-9944-4733-a55b-07043cf7db42",
  "status": "COMPLETE",
  "results": {
    "token_id": 12,
    "transaction_hash": "0x78f4d7063397dd71639a7877876af7f161518679cb8f9df5ac75b1e3e37dac62",
    "transaction_gas_used": 243122,
    "transaction_fee": "0.239949336000000000",
    "requested_at": "2024-07-16T23:11:20+09:00",
    "finished_at": "2024-07-17T08:11:25+09:00"
  }
}
```

</details>
