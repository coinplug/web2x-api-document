NFT 토큰을 타체인에서 가져오기 위해 필요한 데이터를 전송하고, 응답값으로 참조 토큰을 받습니다.    
* 본 API 호출하기 위해서는 토큰에 대한 운영 권한을 WEB2X 플랫폼에서 관리하는 WEB2X-CCMP-LANE 컨트랙트에 위임해야 합니다. (NFT 위임 혹은 NFT 전체 위임 API 사용)
* WEB2X-CCMP-LANE 컨트랙트: WEB2X 플랫폼에서 운영하는 NFT 토큰 교환 기능용 컨트랙트입니다. WEB2X 플랫폼 측에서 각 체인 네트워크마다 1개씩 배포하여 운영합니다.

<p><br/></p>

<details/>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
    "request_id": "4f8e6089-a41f-430b-aab2-5d1f4bb66cc6",
    "status": "COMPLETE",
    "results": [
        {
            "type": "Burn",
            "request_id": "4f8e6089-a41f-430b-aab2-5d1f4bb66cc6",
            "status": "COMPLETE",
            "results": {
                "transaction_gas_used": 146268,
                "finished_at": "2024-12-04T17:15:54+09:00",
                "transaction_fee": "0.011701440000000000",
                "transaction_hash": "0x76209e95a6fd50b48fb387a739c58bbc3f546334c2c0f6b97727be385a6bc056",
                "requested_at": "2024-12-04T08:15:49+09:00"
            }
        },
        {
            "type": "Unlock",
            "request_id": "c8c67350-7ae7-440e-a99b-60add3b97fd6",
            "results": {
                "transaction_gas_used": 75005,
                "finished_at": "2024-12-04T08:16:10+09:00",
                "transaction_fee": "0.006000400000000000",
                "transaction_hash": "0xbb9c20e3ee72519670897dd9b0d8c84bcd3f151bd903e5afa38600a8a64c3eee",
                "requested_at": "2024-12-04T08:15:49+09:00"
            }
        }
    ]
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
{
  "code": "20000",
  "message": "SUCCESS",
  "request_id": "c8c67350-7ae7-440e-a99b-60add3b97fd6",
  "status": "COMPLETE",
  "results": [
    {
      "type": "Burn",
      "results": {
        "transaction_gas_used": 146268,
        "finished_at": "2024-12-04T17:15:54+09:00",
        "transaction_fee": "0.011701440000000000",
        "transaction_hash": "0x76209e95a6fd50b48fb387a739c58bbc3f546334c2c0f6b97727be385a6bc056",
        "requested_at": "2024-12-04T08:15:49+09:00"
      }
    },
    {
      "type": "Unlock",
      "request_id": "c8c67350-7ae7-440e-a99b-60add3b97fd6",
      "results": {
        "transaction_gas_used": 75005,
        "finished_at": "2024-12-04T17:16:10+09:00",
        "transaction_fee": "0.006000400000000000",
        "transaction_hash": "0xbb9c20e3ee72519670897dd9b0d8c84bcd3f151bd903e5afa38600a8a64c3eee",
        "requested_at": "2024-12-04T08:15:49+09:00"
      }
    }
  ]
}
```

</details>
