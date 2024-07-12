디지털 포토카드 발행을 위해 필요한 데이터(이름, 등급, 컬렉션넘버 등)을 전송하고, 응답값으로 참조 토큰을 받습니다. 
- 발행된 디지털 포토카드의 token_id는 최초 발행 시 0이며, 발행 시 마다 순차적으로 1씩 증가하는 값으로 지정됩니다. 
- (주의) 블록체인에 올라가는 data 필드들의 크기에 따라 네트워크 수수료가 부가되며, 크기가 클 경우 수수료가 더 많이 발생할 수 있습니다.
<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

  ```plaintext
  # token_id 필드는 발행된 NFT 토큰의 식별자이며 NFT 토큰을 사용하는 API에서 필요합니다. 
  {
      “request_id”: “21c6c1c4-ca95-4144-9bc3-0d44456d3243”,
      “status”: “SUCCESS”,
      “reason”: “”,
      “results”: {
            “token_id”: 1,
            “transaction_hash”: “0xbd0c8192a39a70525e4b243f67d31c9656bb…”
      }
  }
  ```
</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

  ```plaintext
  # token_id 필드는 발행된 NFT 토큰의 식별자이며 NFT 토큰을 사용하는 API에서 필요합니다. 
  {
      “code”: “20000”,
      “message”: “SUCCESS”,
      “request_id”: “21c6c1c4-ca95-4144-9bc3-0d44456d3243”,
      “results”: {
            “token_id”: 1,
            “transaction_hash”: “0xbd0c8192a39a70525e4b243f67d31c9656bb…”,
            “requested_at”: “2024-04-19T02:16:44.53415005Z”,
            “finished_at”: “2024-04-19T02:16:44.53415005Z”
      }
  }
  ```
</details>
