NFT 활동 알림 수신을 위해 WEB2X API로 배포한 NFT 컨트랙트의 식별자를 입력받아 이벤트 리스너를 등록합니다. 

* 이벤트 리스너: 컨트랙트에서 발생하는 활동을 탐지하여 사용자가 등록한 주소로 결과를 콜백합니다. 
* NFT 컨트랙트에서 탐지 가능한 이벤트는 발행/소각/전송 시에 발생하는 'TRANSFER' 이벤트가 있습니다.
* 콜백 내용 중 이벤트 파라미터(event_parameter)의 from, to 주소에 따라 발행/소각/전송 타입을 식별할 수 있습니다.

<br />

> **이벤트 타입에 따른 From, To 주소 차이**
>    
> * 발행: from = 0x0000000000000000000000000000000000000000 , to = 특정 지갑 주소   
> * 전송: from = 특정 지갑 주소, to = 또 다른 특정 지갑 주소   
> * 소각: from = 특정 지갑 주소, to = 0x0000000000000000000000000000000000000000   
<p><br/></p>

<details/>
  <summary><b>Callback BODY 데이터 예시</b></summary>

```json
{
  "contract_id": "00dbb6e5-ab37-4183-b030-5302fc11f2e6",
  "event_name":"TRANSFER",
  "event_parameter" : {
      "from": "0x0000000000000000000000000000000000000000000000000000000000000000",
      "to": "0x0000000000000000000000004050f7afde4e0ddc595741d19574d320cc86a5c3",
      "token_id": "7" 
  },
  "log": {
    "removed": false,
    "logIndex": 1,
    "transactionIndex": 0,
    "transactionHash": "0x4bf8dad893d7d00bca478cf7bb761589e39d2bf489b11df905f1008e9d21dc69",
    "blockHash": "0x56b9acb15c3274f6d84c06ca2b7e5d2c2c01b5b27afe60b7825e98488f2ac4ca",
    "blockNumber": 63513756,
    "address": "0xb6d78af283619426f674f09309a254889868ce66",
    "data": "0x",
    "type": null,
    "topics": [
      "0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef",
      "0x0000000000000000000000000000000000000000000000000000000000000000",
      "0x0000000000000000000000004050f7afde4e0ddc595741d19574d320cc86a5c3",
      "0x0000000000000000000000000000000000000000000000000000000000000007"
    ],
    "blockNumberRaw": "63513756",
    "logIndexRaw": "1",
    "transactionIndexRaw": "0"
  }
}
```

</details>
