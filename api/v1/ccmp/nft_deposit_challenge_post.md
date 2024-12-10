NFT 토큰을 타체인으로 내보내기 위해 필요한 데이터를 전송하고, 응답값으로 참조 토큰을 받습니다.    
<br />
* 본 API 호출하기 위해서는 토큰에 대한 운영 권한을 WEB2X 플랫폼에서 관리하는 WEB2X-CCMP-LANE 컨트랙트에 위임해야합니다. (NFT 위임 혹은 NFT 전체 위임 API 사용)
* WEB2X-CCMP-LANE 컨트랙트: WEB2X 플랫폼에서 운영하는 NFT 토큰 교환 기능용 컨트랙트입니다. WEB2X 플랫폼 측에서 각 체인 네트워크마다 1개씩 배포하여 운영합니다.

<p><br/></p>

<details/>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "request_id": "400a322c-da20-468c-a53d-2a5986c1b2bd",
  "status": "COMPLETE",
  "results": [
    {
      "type": "Lock",
      "results": {
        "request_id": "aee9b229-8053-4b62-8dd7-cbf66434b167",
        "transaction_gas_used": 167027,
        "finished_at": "2024-12-04T17:12:33+09:00",
        "transaction_fee": "0.013362160000000000",
        "transaction_hash": "0x679aaa8a460e031eddca4fee42d4dfbdd063be9057afdfc9fdbe78bf95928a04",
        "requested_at": "2024-12-04T08:12:28+09:00"
      }
    },
    {
      "type": "Mint",
      "request_id": "400a322c-da20-468c-a53d-2a5986c1b2bd",
      "results": {
        "transaction_gas_used": 124646,
        "finished_at": "2024-12-04T17:12:47+09:00",
        "transaction_fee": "0.009971680000000000",
        "transaction_hash": "0x719487760be45c3950e6f1a43f119f67f7845cbbfb85868e9f47f3de04774351",
        "requested_at": "2024-12-04T08:12:28+09:00"
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
    "request_id": "aee9b229-8053-4b62-8dd7-cbf66434b167",
    "status": "COMPLETE",
    "results": [
        {
            "type": "Lock",
            "request_id": "aee9b229-8053-4b62-8dd7-cbf66434b167",
            "status": "COMPLETE",
            "results": {
                "transaction_gas_used": 167027,
                "finished_at": "2024-12-04T17:12:33+09:00",
                "transaction_fee": "0.013362160000000000",
                "transaction_hash": "0x679aaa8a460e031eddca4fee42d4dfbdd063be9057afdfc9fdbe78bf95928a04",
                "requested_at": "2024-12-04T08:12:28+09:00"
            }
        },
        {
            "type": "Mint",
            "request_id": "400a322c-da20-468c-a53d-2a5986c1b2bd",
            "results": {
                "transaction_gas_used": 124646,
                "finished_at": "2024-12-04T08:12:47+09:00",
                "transaction_fee": "0.009971680000000000",
                "transaction_hash": "0x719487760be45c3950e6f1a43f119f67f7845cbbfb85868e9f47f3de04774351",
                "requested_at": "2024-12-04T08:12:28+09:00"
            }
        }
    ]
}
```

</details>
