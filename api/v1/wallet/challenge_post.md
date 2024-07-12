지갑 생성을 위해 필요한 데이터(지갑 이름, 사용할 네트워크 등)를 전송하고, 응답값으로 참조 토큰을 받습니다.

* auth_type 필드는 생성할 지갑의 서명 키 종류를 입력합니다. 
* sig_public_key 필드는 서명용 키로써, 지갑에서 발생시킬 트랜잭션(챌린지)을 서명할 때 사용할 키의 공개키입니다. 
* mng_public_key 필드는 관리용 키로써, 지갑의 서명키를 변경할때 사용하는 공개키입니다. (EoA키만 등록 가능)
<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

  ```plaintext
  # wallet_id 필드는 생성된 지갑의 식별자이며 지갑을 사용하는 API에서 필요합니다. 
  {
      "request_id": "21c6c1c4-ca95-4144-9bc3-0d44456d3243",
      "status": "SUCCESS",
      "reason": "",
      "results": {
            "wallet": {
                "wallet_id": "12c6c1c4-ca95-4144-9bc3-0d44456d3243",
                "wallet_name": "홍길동지갑1",
                "address": "0x11",
                "network_chain_id": 11,
                "auth_type": "eoa",
                "sig_public_key": "0x13…",
                "mng_public_key": "0x14…",
                "created_at": "2024-04-19T02:16:44.53415005Z"
            },
            "transaction_hash": "0xbd0c8192a39a70525e4b243f67d31c9656bb…"
      }
  }
  ```
</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

  ```plaintext
  # wallet_id 필드는 생성된 지갑의 식별자이며 지갑을 사용하는 API에서 필요합니다. 
  {
      "code": "20000",
      "message": "SUCCESS",
      "request_id": "21c6c1c4-ca95-4144-9bc3-0d44456d3243",
      "results": {
            "wallet": {
                "wallet_id": "12c6c1c4-ca95-4144-9bc3-0d44456d3243",
                "wallet_name": "홍길동지갑1",
                "address": "0x11",
                "network_chain_id": 11,
                "auth_type": "eoa",
                "sig_public_key": "0x13…",
                "mng_public_key": "0x14…",
                "created_at": "2024-04-19T02:16:44.53415005Z"
            },
            "transaction_hash": "0xbd0c8192a39a70525e4b243f67d31c9656bb…"
            "requested_at": "2024-04-19T02:16:44.53415005Z",
            "finished_at": "2024-04-19T02:16:44.53415005Z" 
      }
  }
  ```
</details>
