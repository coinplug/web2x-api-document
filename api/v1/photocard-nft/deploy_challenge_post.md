디지털 포토카드 템플릿 배포*를 위해 필요한 데이터(이름, 심볼)을 전송하고, 응답값으로 참조 토큰을 받습니다.
- 디지털 포토카드 템플릿의 owner 는 wallet_id 필드의 주소로 지정됩니다.
- 디지털 포토카드 템플릿의 default_data 는 빈문자열("") 로 지정됩니다.

\* 디지털 포토카드 템플릿 배포: 디지털 포토카드 발행을 위해 포토카드의 정보를 담아 템플릿을 배포 (블록체인 상 토큰 발행 정보를 담은 컨트랙트를 배포하는 단계, 배포 후 수정 불가)
<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

  ```plaintext
  # contract_id 필드는 배포된 NFT 컨트랙트의 식별자이며 컨트랙트를 사용하는 API에서 필요합니다. 
  {
      “request_id”: “21c6c1c4-ca95-4144-9bc3-0d44456d3243”,
      “status”: “SUCCESS”,
      “reason”: “”,
      “results”: {
            "contract": {
                “contract_id”: “93462407-7410-44f3-bbb4-648f1d732fa0”,
                "network_chain_id": 11,
                "contract_address": "0x379A77AD8c89b5d1366e77D1f3a168706A9e287e",
                "owner_address": "0x579A77AD8c89b5d1366e77D1f3a168706A9e287e",
                "name": "WEB2X NFT",
                "symbol": "W2NFT",
                "is_burnable": true,
                “ids” : [1, 2, 3, 4]
            },
            “transaction_hash”: “0xbd0c8192a39a70525e4b243f67d31c9656bb…”
      }
  }
  ```
</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

  ```plaintext
  # contract_id 필드는 배포된 NFT 컨트랙트의 식별자이며 컨트랙트를 사용하는 API에서 필요합니다. 
  {
      “code”: “20000”,
      “message”: “SUCCESS”,
      “request_id”: “21c6c1c4-ca95-4144-9bc3-0d44456d3243”,
      “results”: {
            "contract": {
                “contract_id”: “93462407-7410-44f3-bbb4-648f1d732fa0”,
                "network_chain_id": 11,
                "contract_address": "0x379A77AD8c89b5d1366e77D1f3a168706A9e287e",
                "owner_address": "0x579A77AD8c89b5d1366e77D1f3a168706A9e287e",
                "name": "WEB2X NFT",
                "symbol": "W2NFT",
                "is_burnable": true,
                “ids” : [1, 2, 3, 4]
            },
            “transaction_hash”: “0xbd0c8192a39a70525e4b243f67d31c9656bb…”
            “requested_at”: “2024-04-19T02:16:44.53415005Z”,
            “finished_at”: “2024-04-19T02:16:44.53415005Z”
      }
  }          
  ```
</details>
