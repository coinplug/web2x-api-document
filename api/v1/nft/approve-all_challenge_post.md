NFT 전체 위임을 위해 필요한 데이터를 전송하고, 응답값으로 참조 토큰을 받습니다.
<br />
* NFT 토큰 내보내기/가져오기를 호출하기 위해서는 토큰의 위임 대상 id(operator_wallet_id)를 'WEB2X-CCMP-LANE'으로 입력해야합니다.  
* WEB2X-CCMP-LANE 컨트랙트: WEB2X 플랫폼에서 운영하는 NFT 토큰 교환 기능 용 컨트랙트입니다. WEB2X 플랫폼 측에서 각 체인 네트워크마다 1개씩 배포하여 운영합니다. 

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "request_id": "d4e748da-004c-4c41-a2ff-b32864361b1d",
  "status": "COMPLETE",
  "results": {
    "transaction_gas_used": 137547,
    "finished_at": "2024-12-04T17:10:30+09:00",
    "transaction_fee": "0.011003760000000000",
    "transaction_hash": "0xba73f745a70bda9c1393fec620e548b349cfc470e131e67ea7d71f7dc2d180d9",
    "requested_at": "2024-12-04T08:10:25+09:00"
  }
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "d4e748da-004c-4c41-a2ff-b32864361b1d",
    "status": "COMPLETE",
    "results": {
        "transaction_gas_used": 137547,
        "finished_at": "2024-12-04T17:10:30+09:00",
        "transaction_fee": "0.011003760000000000",
        "transaction_hash": "0xba73f745a70bda9c1393fec620e548b349cfc470e131e67ea7d71f7dc2d180d9",
        "requested_at": "2024-12-04T08:10:25+09:00"
    }
}
```

</details>
