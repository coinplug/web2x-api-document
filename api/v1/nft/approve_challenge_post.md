NFT 위임 챌린지 API에서 받은 챌린지를 사용자의 개인키로 서명하여 NFT 위임을 요청합니다.
<br />
* NFT 토큰 내보내기/가져오기를 호출하기 위해서는 토큰의 위임 대상 id(spender_wallet_id)를 'WEB2X-CCMP-LANE'으로 입력해야합니다.  
* WEB2X-CCMP-LANE 컨트랙트: WEB2X 플랫폼에서 운영하는 NFT 토큰 교환 기능 용 컨트랙트입니다. WEB2X 플랫폼 측에서 각 체인 네트워크마다 1개씩 배포하여 운영합니다. 

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "request_id": "ac7f1ec3-ae32-4cfd-9767-d10495f1ce9a"
  "status": "COMPLETE",
  "results": {
    "transaction_hash": "0xf174631f476cfb63f49f945c70e8d1db0fce39e009fe226f41b3bbdf172a5cd5",
    "transaction_gas_used": 118012,
    "transaction_fee": "0.239949336000000000",
    "requested_at": "2024-07-16T23:31:29+09:00",
    "finished_at": "2024-07-17T08:31:32+09:00"
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
  "request_id": "ac7f1ec3-ae32-4cfd-9767-d10495f1ce9a",
  "status": "COMPLETE",
  "results": {
    "transaction_hash": "0xf174631f476cfb63f49f945c70e8d1db0fce39e009fe226f41b3bbdf172a5cd5",
    "transaction_gas_used": 118012,
    "transaction_fee": "0.239949336000000000",
    "requested_at": "2024-07-16T23:31:29+09:00",
    "finished_at": "2024-07-17T08:31:33+09:00"
  }
}
```

</details>
