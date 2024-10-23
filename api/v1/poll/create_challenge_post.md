안건을 등록하기 위해 필요한 데이터(안건 정보, 선택지 내용 등)를 전송하고, 응답값으로 참조 토큰을 받습니다.

<p><br/></p>

<details>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
# proposal_id 필드는 등록된 안건의 식별자이며 안건을 사용하는 API에서 필요합니다. 
{
  "request_id": "52e657ee-cc9b-4b7f-b5e7-2e05477ecbaa",
  "status": "COMPLETE",
  "results": {
      "proposal": {
          "proposal_id": "51829201-a2ed-40b3-9141-f684970b1388",
          "network_chain_id": 12,
          "name": "안건 제목",
          "description": "안건 내용",
          "is_revotable": true,
          "is_multivotable": true,
          "start_timestamp": 1729662837,
          "end_timestamp": 1729672837,
          "contract_addr": "0x30101bdc79898dfd910ba77d0155acaff0e60ac7",
          "owner_addr": "0x1214Ae02C495E96Fd102705FA3c00721fbD52BC9"
      },
    "transaction_hash": "0x7442ed2bbf599c9ad8391ca08330ade641308c07d6445e498f38479364ae6610",
    "transaction_gas_used": 2241774,
    "transaction_fee": "0.239949336000000000",
    "requested_at": "2024-07-16T23:51:48+09:00",
    "finished_at": "2024-07-17T08:51:50+09:00"
  }
}
```

</details>

<details>
  <summary><b>요청처리결과 조회 API 응답 데이터 예시</b></summary>

```json
# proposal_id 필드는 등록된 안건의 식별자이며 안건을 사용하는 API에서 필요합니다. 
{
    "code": "20000",
    "message": "SUCCESS",
    "request_id": "8738f026-fcaa-4e9e-80d3-9bb1e6361ec0",
    "status": "COMPLETE",
    "results": {
        "transaction_gas_used": 3764105,
        "finished_at": "2024-10-22T16:04:26+09:00",
        "proposal": {
            "proposal_id": "51829201-a2ed-40b3-9141-f684970b1388",
            "network_chain_id": 12,
            "name": "안건 제목",
            "description": "안건 내용",
            "is_revotable": true,
            "is_multivotable": true,
            "start_timestamp": 1729662837,
            "end_timestamp": 1729672837,
            "contract_addr": "0x30101bdc79898dfd910ba77d0155acaff0e60ac7",
            "owner_addr": "0x1214Ae02C495E96Fd102705FA3c00721fbD52BC9"
        },
        "transaction_fee": "0.301128400000000000",
        "transaction_hash": "0x8676ce89d88a21127f600310f9c214195523642eefff14b133c055f183d7b567",
        "requested_at": "2024-10-22T07:04:21+09:00"
    }
}
```
