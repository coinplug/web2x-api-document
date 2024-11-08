문서 등록을 위해 필요한 데이터(문서 내용 해시값)를 전송하고, 응답값으로 참조 토큰을 받습니다.

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
# token_id 필드는 등록된 문서(토큰)의 식별자이며 문서를 사용하는 API에서 필요합니다. 
{
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

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
# token_id 필드는 등록된 문서(토큰)의 식별자이며 문서를 사용하는 API에서 필요합니다. 
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
