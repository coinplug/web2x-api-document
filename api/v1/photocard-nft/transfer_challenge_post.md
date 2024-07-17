디지털 포토카드 전송을 위해 필요한 데이터(전송할 디지털 포토카드 id, 전송자 지갑 id, 수신자 지갑 id 등)을 전송하고, 응답값으로 참조 토큰을 받습니다.
<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

  ```plaintext
  {
    "status": "COMPLETE",
    "request_id": "004e728d-5859-486a-b187-7d3caaf62637",
    "results": {
      "transaction_hash": "0xba0965b862f2decacb5599fc758ce9f2982319cfe8d050c970df2a27385d2131",
      "transaction_gas_used": 162789,
      "requested_at": "2024-07-16T23:22:51+09:00",
      "finished_at": "2024-07-17T08:22:56+09:00"
    },
  }
  ```
</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

  ```plaintext
  {
      "code": "20000",
      "message": "SUCCESS",
      "request_id": "004e728d-5859-486a-b187-7d3caaf62637",
      "status": "COMPLETE",
      "results": {
          "transaction_hash": "0xba0965b862f2decacb5599fc758ce9f2982319cfe8d050c970df2a27385d2131",
          "transaction_gas_used": 162789,
          "requested_at": "2024-07-16T23:22:51+09:00",
          "finished_at": "2024-07-17T08:22:56+09:00"
      }
  }
  ```
</details>