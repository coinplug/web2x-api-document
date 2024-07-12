지갑 공개키 변경을 위해 필요한 데이터(현재 공개키, 변경할 공개키)를 전송하고, 응답값으로 참조 토큰을 받습니다.

* old_public_key 필드는 key_usage 필드의 값에 따라 특정 지갑의 서명용 공개키나 관리용 공개키를 입력할 수 있습니다. 
* new_public_key 필드에는 지갑의 기존 서명키 종류(auth_type)와 동일한 형태의 공개키를 입력해야합니다. 
* (주의) 해당 챌린지는 반드시 관리용 개인키로 서명해야합니다.
<p><br/></p>


<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

  ```plaintext
  {
      “request_id”: “21c6c1c4-ca95-4144-9bc3-0d44456d3243”,
      “status”: “SUCCESS”,
      “reason”: “”,
      “results”: {
            “transaction_hash”: “0xbd0c8192a39a70525e4b243f67d31c9656bb…”
      }
  }
  ```
</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

  ```plaintext
  {
      “code”: “20000”,
      “message”: “SUCCESS”,
      “request_id”: “21c6c1c4-ca95-4144-9bc3-0d44456d3243”,
      “results”: {
            “transaction_hash”: “0xbd0c8192a39a70525e4b243f67d31c9656bb…”,
            “requested_at”: “2024-04-19T02:16:44.53415005Z”,
            “finished_at”: “2024-04-19T02:16:44.53415005Z”
      }
  }
  ```
</details>
