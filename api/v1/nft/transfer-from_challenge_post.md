NFT 대리전송을 위해 필요한 데이터(전송할 토큰 id, 토큰오너의 지갑 id, 수신자 지갑 id 등)을 전송하고, 응답값으로 참조 토큰을 받습니다.
- 대리전송을 진행할 지갑(wallet_id)는 전송할 토큰에 대해서 NFT 위임 API를 통해 전송권한을 위임한 상태여야 합니다.
<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

  ```plaintext
  {
    "request_id": "5a52468e-c98b-4ead-b02d-7c1b1b81a055",
    "status": "COMPLETE",
    "results": {
      "transaction_hash": "0xa5f0c449d7de3e81af7c9892e3bb5c37a629f152cdf2ec439490464177f1b062",
      "transaction_gas_used": 141605,
      "requested_at": "2024-07-16T23:34:20+09:00",
      "finished_at": "2024-07-17T08:34:24+09:00"
    }
  }
  ```
</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

  ```plaintext
  {
      "code": "20000",
      "message": "SUCCESS",
      "request_id": "5a52468e-c98b-4ead-b02d-7c1b1b81a055",
      "status": "COMPLETE",
      "results": {
          "transaction_hash": "0xa5f0c449d7de3e81af7c9892e3bb5c37a629f152cdf2ec439490464177f1b062",
          "transaction_gas_used": 141605,
          "requested_at": "2024-07-16T23:34:20+09:00",
          "finished_at": "2024-07-17T08:34:24+09:00"
      }
  }
  ```
</details>