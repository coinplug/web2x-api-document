지갑 생성을 위해 필요한 데이터(지갑 이름, 사용할 네트워크 등)를 전송하고, 응답값으로 참조 토큰을 받습니다.

- auth_type 필드는 생성할 지갑의 서명 키 종류를 입력합니다.
- sig_public_key 필드는 서명용 키로써, 지갑에서 발생시킬 트랜잭션(챌린지)을 서명할 때 사용할 키의 공개키입니다.
- mng_public_key 필드는 관리용 키로써, 지갑의 서명키를 변경할때 사용하는 공개키입니다. (EoA키만 등록 가능)
<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
# wallet_id 필드는 생성된 지갑의 식별자이며 지갑을 사용하는 API에서 필요합니다.
{
  "request_id": "5fc9682d-7b21-448e-9c62-286b266e7e9b"
  "status": "COMPLETE",
  "results": {
    "wallet": {
      "wallet_id": "31b8b3e2-9ebb-41a8-a7d5-9dda28e249d5",
      "wallet_name": "hong-gil-dong",
      "wallet_address": "0x300209c94eb01e9a27b053a41586de71225377be",
      "network_chain_id": 12,
      "auth_type": "eoakey",
      "sig_public_key": "0x44b59a2101ef56ae6f618602255f8b147568332c53262b5f02f359c87709649e478929d74a73ca2007d9f0e55106f39ad2507859ccc15413cb48e83fd57b0950",
      "mng_public_key": "0xc2962fbe6af1540896ccd7ba816a52ebc1d7d4fa1df2b1745e27b257b0023f0a1d5ff0ca8fd6378e5bf5a50597f23dbea8773775f452178793f534a731578606",
      "created_at": "2024-07-16T07:30:24+09:00"
    },
    "transaction_hash": "0x871721b6e08645a40dc3ce2a625bafa039cf5ed64c65124c71cbbbc2c05aa02d",
    "transaction_gas_used": 2347335,
    "requested_at": "2024-07-16T07:30:24+09:00"
    "finished_at": "2024-07-16T16:30:26+09:00",
  },
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
# wallet_id 필드는 생성된 지갑의 식별자이며 지갑을 사용하는 API에서 필요합니다.
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "5fc9682d-7b21-448e-9c62-286b266e7e9b",
    "status": "COMPLETE",
    "results": {
        "wallet": {
            "wallet_id": "31b8b3e2-9ebb-41a8-a7d5-9dda28e249d5",
            "wallet_name": "dev-test-0716",
            "wallet_address": "0x300209c94eb01e9a27b053a41586de71225377be",
            "network_chain_id": 12,
            "auth_type": "eoakey",
            "sig_public_key": "0x44b59a2101ef56ae6f618602255f8b147568332c53262b5f02f359c87709649e478929d74a73ca2007d9f0e55106f39ad2507859ccc15413cb48e83fd57b0950",
            "mng_public_key": "0xc2962fbe6af1540896ccd7ba816a52ebc1d7d4fa1df2b1745e27b257b0023f0a1d5ff0ca8fd6378e5bf5a50597f23dbea8773775f452178793f534a731578606",
            "created_at": "2024-07-16T07:30:24+09:00"
        },
        "transaction_hash": "0x871721b6e08645a40dc3ce2a625bafa039cf5ed64c65124c71cbbbc2c05aa02d",
        "transaction_gas_used": 2347335,
        "requested_at": "2024-07-16T07:30:24+09:00"
        "finished_at": "2024-07-16T16:30:27+09:00",
    }
}
```

</details>
