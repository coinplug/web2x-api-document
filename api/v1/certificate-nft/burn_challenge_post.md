증명서 소각을 위해 필요한 데이터(소각할 증명서 id 등)을 전송하고, 응답값으로 참조 토큰을 받습니다.

- 증명서 토큰은 템플릿의 owner가 소각할 수 있습니다.

<p><br/></p>

<details/>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "request_id": "d0d197b8-1e69-4da6-9f0d-d4803b18ebd4",
  "status": "COMPLETE",
  "results": {
    "transaction_hash": "0xc3e266f70b759feff43324882fbec3f9d0fd8c2e390a86bc6fa7b91530985a90",
    "transaction_gas_used": 108496,
    "transaction_fee": "0.239949336000000000",
    "requested_at": "2024-07-16T23:26:50+09:00",
    "finished_at": "2024-07-17T08:26:53+09:00",
  },
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "d0d197b8-1e69-4da6-9f0d-d4803b18ebd4",
    "status": "COMPLETE",
    "results": {
        "transaction_hash": "0xc3e266f70b759feff43324882fbec3f9d0fd8c2e390a86bc6fa7b91530985a90",
        "transaction_gas_used": 108496,
        "transaction_fee": "0.239949336000000000",
        "requested_at": "2024-07-16T23:26:50+09:00",
        "finished_at": "2024-07-17T08:26:54+09:00"
    }
}
```

</details>

