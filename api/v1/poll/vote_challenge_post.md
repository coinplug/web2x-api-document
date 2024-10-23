투표하기 위해 필요한 데이터(안건id, 선택지번호)를 전송하고, 응답값으로 참조 토큰을 받습니다.

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "status": "COMPLETE",
  "request_id": "004e728d-5859-486a-b187-7d3caaf62637",
  "results": {
    "transaction_hash": "0xba0965b862f2decacb5599fc758ce9f2982319cfe8d050c970df2a27385d2131",
    "transaction_gas_used": 162789,
    “transaction_fee”: "0.239949336000000000",
    "requested_at": "2024-07-16T23:22:51+09:00",
    "finished_at": "2024-07-17T08:22:56+09:00"
  },
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "004e728d-5859-486a-b187-7d3caaf62637",
    "status": "COMPLETE",
    "results": {
        "transaction_hash": "0xba0965b862f2decacb5599fc758ce9f2982319cfe8d050c970df2a27385d2131",
        "transaction_gas_used": 162789,
        “transaction_fee”: "0.239949336000000000",
        "requested_at": "2024-07-16T23:22:51+09:00",
        "finished_at": "2024-07-17T08:22:56+09:00"
    }
}
```
