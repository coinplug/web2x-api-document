## 소개

WEB2X API는 웹2 개발자가 웹3 기술을 쉽게 사용할 수 있도록 도와주는 기술입니다. 기존의 여러 API 서비스들을 HTTP
API를 기반으로 쉽게 사용하듯이, WEB2X API 또한 HTTP API를 이용하여 간단히 사용할 수 있습니다.

이 API 문서는 개발자가 WEB2X API를 사용하는 데 필요한 모든 기술 문서가 포함하고 있습니다. WEB2X API에 관해 더
궁금한 점이 있으시면 ‘[문의하기](https://forms.gle/AYBw8P7V5oeVsgVg6)'를 통해 문의해주시기 바랍니다.

## WEB2X API

1. API 구조 및 프로세스

   WEB2X 플랫폼은 웹2 개발자들이 쉽게 웹3 서비스를 활용할 수 있도록 HTTP API를 통해 트랜잭션을 호출할 수 있는 환경을 제공합니다.

   <br/>

   **플랫폼 구성 요소**

   - **WEB2X API 서버**: 서비스 이용자가 호출하는 API를 관리하고, 요청을 검증하여 WEB2X 노드 서버로 전달합니다. API 호출 결과를 반환하거나 콜백을 처리하는 기능을 담당합니다.

   - **WEB2X 노드 서버**: 여러 블록체인 네트워크와의 연결을 관리하며, 서비스 이용자의 API 요청을 블록체인 트랜잭션으로 변환하여 네트워크에 전송합니다. 또한 트랜잭션 처리 상태를 감지하고 결과를 반환합니다.

   <br/>

   **요청 처리 과정**

   1. API 호출: WEB2X 서비스 이용자가 HTTP API를 통해 WEB2X 플랫폼에 API를 호출합니다.
   2. API 서버 처리: WEB2X API 서버는 이용자의 요청을 수신하고, 인증 및 검증 과정을 거친 후 WEB2X 노드 서버로 전달합니다.
   3. 트랜잭션 처리: WEB2X 노드 서버는 받은 요청을 블록체인 네트워크에 전파할 수 있는 형태로 변환합니다. 이 과정에서 합의 알고리즘을 통해 트랜잭션을 생성하고, 네트워크에 전송합니다.
   4. 트랜잭션 완료: 블록체인 네트워크는 전송된 트랜잭션을 처리하고, 이후 네트워크의 참여자들에 의해 선택된 블록에 포함되어 처리가 완료됩니다.

   이러한 방식을 통해 WEB2X 플랫폼은 간편하고 안전한 방법으로 웹3 서비스를 활용할 수 있는 환경을 제공합니다.

2. API 신청

   1. www.web2x.io 에서 ‘로그인' 버튼을 클릭하여, 회원가입과 로그인을 진행합니다.
   2. ‘프로젝트' 메뉴를 클릭합니다.
   3. ‘신청하기' 버튼을 클릭합니다.
      ![](https://github.com/coinplug/web2x-api-document/raw/master/images/1-2-3-n.png)
   4. ‘회사명'과 ‘상품 사용 용도'를 알맞게 작성합니다.
      ![](https://github.com/coinplug/web2x-api-document/raw/master/images/1-2-4-n.png)
   5. ‘신청하기' 버튼을 클릭해 API 사용 신청을 완료합니다.

   ※ API 사용 신청 후 최대 2 영업일 안에 연락을 드립니다.

   ※ 무료 API의 경우 메타디움 메인넷에서 100META까지 수수료 지원이 되며, 더 많은 사용을 원할 시 별도로 문의 부탁드립니다. (response 오류가 날 경우, 카운트되지 않음)

## API 사용

1. API 키 확인

   ‘프로젝트 관리'에서 API 키를 확인하고, 복사하실 수 있습니다.

   ※ API 키는 회원가입과 동시에 발급되어 메타디움 테스트넷의 경우, 바로 사용하실 수 있습니다.
   ![](https://github.com/coinplug/web2x-api-document/raw/master/images/2-1-n.png)

2. API 키 사용

   WEB2X 서비스 포털 사이트에서 발급한 API 키는 WEB2X API를 호출하기 위한 HTTP 요청에서 사용됩니다. API 키는 다음과 같은 방식으로 사용됩니다.

   <br/>

   **API 키 사용 방법**

   API 키는 모든 WEB2X API 호출 시 HTTP 요청의 헤더에 포함되어야 합니다. 이를 통해 서비스 이용자의 API 사용량과 사용 권한 등을 식별하고 관리합니다.

   - **API 키 입력**: HTTP 요청 헤더에 API 키 값을 포함하여 API를 호출합니다.
   - **보안 유지**: API 키는 사용자의 식별 및 인증 용도로 사용되므로 외부에 노출되지 않도록 보관해야 합니다. API 키가 유출된 경우, 즉시 WEB2X 서비스 포털 사이트에서 API키를 재발급 받아야 합니다.

   <br/>

   **API Key 관련 HTTP 상태코드**

   아래는 API 요청 시 발생할 수 있는 HTTP 상태코드와 서비스 응답코드를 보여줍니다. 'api-key' 헤더가 필수임을 나타내며, 유효하지 않은 경우에 대한 처리를 설명합니다.
   | HTTP 상태코드 | 서비스 응답코드 | 서비스 응답메시지 |
   | ------------- | --------------- | ---------------------------- |
   | 401 | 40100 | 'api-key' header is required |
   | 401 | 40101 | 'api-key' header is invalid |

## API. 요청, 응답

1. API 요청

   WEB2X API는 쿼리 파라미터를 사용하는 GET 방식과 BODY 파라미터를 사용하는 POST 방식을 지원합니다. GET 방식의 쿼리 파라미터 데이터는 URL 인코딩을 거쳐 HTTP URL에 연결되어야 하며 이는 대부분의 HTTP 요청 라이브러리에서 기본 지원됩니다.

   <br/>

   **HTTP 메소드 및 파라미터 유형**

   | HTTP 메소드 | 파라미터 유형 | 파라미터 입력 값                     |
   | ----------- | ------------- | ------------------------------------ |
   | GET         | 쿼리 파라미터 | HTTP URL 값에 URL 인코딩된 값 입력   |
   | POST        | BODY 파라미터 | HTTP data 필드에 JSON 형식의 값 입력 |

   또한, WEB2X API 요청 시에는 아래와 같은 공통 HTTP Header를 항상 입력해야 합니다.

   <br/>

   **WEB2X API 공통 HTTP 헤더**

   | 헤더 필드명  | 헤더 데이터                              |
   | ------------ | ---------------------------------------- |
   | Content-type | application/json                         |
   | API_KEY      | _{서비스 포탈에서 발급한 API 키 문자열}_ |

2. API 응답

   **HTTP 상태코드 및 응답 메시지**

   WEB2X API의 응답은 다음과 같은 구조로 제공됩니다:

   - **WEB2X 응답**: WEB2X의 API 응답 데이터에는 HTTP 요청에 대한 기본적인 응답코드(HTTP Status)와 JSON 형식의 응답 본문 데이터가 포함됩니다.
   - **WEB2X HTTP 상태코드**: HTTP 표준 상태코드를 따르며, 각 상태코드는 특정 상황을 나타내므로 서비스 이용자는 클라이언트 개발 시 상태코드에 따라 요청에 대한 적절한 처리(에러 처리 등)를 해야 합니다.

   | HTTP 상태코드 | 메시지                |
   | ------------- | --------------------- |
   | 200           | OK                    |
   | 400           | Bad Request           |
   | 401           | Unauthorized          |
   | 404           | Not Found             |
   | 500           | Internal Server Error |

   <br/>

   **WEB2X API 응답 규격**

   WEB2X API의 응답 본문은 JSON 형식으로 데이터를 반환합니다. WEB2X API의 JSON 형식의 응답 데이터에는 다음과 같은 공통 응답 필드가 포함되어있습니다.

   ```json
   {
     "code": "20000",
     "message": "SUCCESS"
   }
   ```

   - **code**: WEB2X API에서 정의한 서비스 응답 코드로, 각 API의 요청 결과를 식별합니다. HTTP 상태코드와 유사하지만 추가적인 식별을 위한 2자리 코드를 포함합니다. (총 5자리의 코드)
   - **message**: code에 대한 상세 설명을 제공합니다. 요청 실패 시의 디버깅에 유용한 추가 정보를 포함합니다.

   클라이언트는 API 요청 후 반환된 code와 message 값을 확인하여 API의 성공 여부 및 실패 사유를 확인할 수 있습니다. 또한, 각 API 문서를 통해 추가적인 응답 데이터에 대한 규격을 확인할 수 있습니다.

## 용어 정의

**챌린지**

챌린지는 보안 인증 방식 중 하나로, 사용자가 자신의 신원을 증명하거나 데이터의 무결성을 검증하기 위해 사용되는 도전 과제를 의미합니다.
WEB2X API에서는 챌린지를 사용하여 사용자가 서명한 데이터를 검증하고, 이를 통해 API 요청의 정당성을 보장합니다.

<p><br/></p>

**컨트랙트**

블록체인에서 컨트랙트는 스마트 계약을 의미합니다. 스마트 계약은 코드로 작성된 자동화된 계약으로, 코드가 블록체인 네트워크에 배포되어
실행될 수 있으며, 한번 배포하면 수정이 불가합니다. 이더리움과 같은 플랫폼에서는 컨트랙트를 통해 사용자 간의 자동화된 거래나 조건부
실행을 수행할 수 있습니다.

<p><br/></p>

**토큰**

블록체인에서 토큰은 자산이나 유틸리티를 나타내는 디지털 자산입니다. 토큰은 블록체인 네트워크에서 발행되어 사용될 수 있으며, 대표적으로
이더리움 네트워크에서 ERC-20과 같은 표준 인터페이스를 통해 발행됩니다.

<p><br/></p>

**토큰ID**

토큰ID는 특정 토큰을 식별하는 고유한 식별자입니다. 이더리움과 같은 블록체인 네트워크에서 각 토큰은 고유한 토큰ID를 가지며, 이를
통해 특정 토큰을 참조하거나 식별할 수 있습니다.

<p><br/></p>

**AA 지갑**

AA(Account Abstraction) 지갑은 이더리움과 같은 블록체인 플랫폼에서 사용되는 지갑 계정의 추상화 형태를 의미합니다.
AA 지갑은 트랜잭션을 보낼 때 지정된 개인키로 서명하는 기존 지갑과 달리, 구현에 따라 여러 형태의 인증/서명 방식을 통해 계정을
제어하고 트랜잭션을 서명할 수 있는 기능을 제공합니다.

<p><br/></p>

**공개키**

공개키는 공개키 암호화에서 사용되는 키로, 데이터를 암호화하거나 서명을 확인하는 데 사용됩니다. 이더리움과 같은 블록체인에서는 공개키가
지갑 주소로 사용되며, 다른 사용자들과 공유될 수 있는 키입니다.

<p><br/></p>

**개인키**

개인키는 공개키 암호화에서 사용되는 키로, 데이터를 복호화하거나 서명을 생성하는 데 사용됩니다. 개인키는 사용자가 자신의 자산을 안전하게
보호하고 관리할 수 있도록 합니다. 개인키는 절대적으로 비밀로 유지되어야 하며, 노출될 경우 보안에 심각한 위협이 될 수 있습니다.

## 지갑 서명 키와 서명

1. WEB2X 지갑과 서명의 필요성

   블록체인 내 자산(토큰)의 소유권은 모두 체인 위에 기록되며 체인에 기록된 자산을 편리하게 거래하기 위해서 자산에 대한 소유권을 보관하는 지갑을 사용합니다. 기존 블록체인 네트워크에서 제공하는 지갑은 거래를 요청할 때마다 지정된 개인키와 암호 알고리즘으로 서명을 해야 하는 제한이 있어 다양한 인증방식을 지원하기에는 어려움이 있습니다.

   이를 해결하기 위해 WEB2X 플랫폼의 지갑은 Ethereum의 계정 추상화(Account Abstraction) 지갑 컨트랙트를 이용하여 다양한 방식으로 인증/서명한 결과를 검증하여 트랜잭션을 실행하는 방안을 제공합니다. 이를 통해 서비스 이용자는 자신의 지갑 계정에 여러 종류의 서명 키를 등록하여 다양한 형태의 인증/서명 방식으로 지갑을 더 편리하게 제어할 수 있도록 권한을 제한 합니다.

   - **서명 키 등록**: 서비스 이용자는 지갑을 생성할 때 해당 지갑을 제어할 수 있는 서명 키를 등록합니다.
   - **서명을 통한 API 제어**: 서비스 이용자는 지갑에 등록된 서명 키로 API 요청 정보를 서명하여 지갑을 제어할 수 있습니다.

   **참고**: 지갑에서 실행가능한 기능과 각 요청 데이터(챌린지) 정보는 WEB2X API 문서에서 확인할 수 있습니다.

2. 서명 키 종류 및 사용 방법

   WEB2X 플랫폼에서 지원하는 서명 키는 EoAKey와 PassKey를 시작으로 다양한 서명 키 유형을 지원할 예정에 있습니다. 각 서명 키는 지갑을 생성할 때 서명 키의 종류를 입력하여 서명 키를 등록합니다.

   **주의**: 서명 키의 종류는 지갑을 이미 생성한 뒤에는 변경할 수 없습니다.

   <br/>

   - **EoA 키**

   - EoA(Externally Owned Account) 키는 이더리움 블록체인 기술에서 사용되는 암호키의 유형입니다. 이 키는 사용자가 자신의 자산을 안전하게 보호하고 관리하기 위해 필요한 서명과 검증을 위해 생성됩니다.
   - 공개키 암호화에서 사용되는 EoA 키는 공개키(public key)와 개인키(private key)로 구성됩니다. 공개키는 다른 사용자들과 공유되어 계정의 식별자 역할을 하며, 개인키는 사용자가 자신의 자산을 관리하고 트랜잭션을 서명하는 데 사용됩니다. 이 키는 절대적으로 비밀로 유지되어야 하며, 타인에게 노출되면 보안에 심각한 위협이 될 수 있습니다.
   - EoA 키는 ECDSA(타원 곡선 디지털 서명 알고리즘)을 기반으로 생성됩니다. WEB2X API에서는 압축되지 않은(uncompressed) 공개키를 사용하며, 이는 128 글자(64 바이트)의 길이를 갖습니다.

   <br/>

      1. **EoA 키 생성 및 키 서명 예시코드 (Java)**

      ```java
      import org.web3j.crypto.*;
      import org.web3j.utils.Numeric;

      ...

      // 키 생성
      ECKeyPair keyPair = Keys.createEcKeyPair();
      Credentials credentials = Credentials.create(keyPair);
      System.out.println("Private Key: " + credentials.getEcKeyPair().getPrivateKey().toString(16));
      System.out.println("Public Key: " + credentials.getEcKeyPair().getPublicKey().toString(16));

      // 서명할 메시지인 챌린지 값 입력
      String challenge = "0x201850223ca06071ffb0914104ba4dbeffa51e14417aa26e036e7c8a51cd9dd8"
      byte[] messageHash = Numeric.hexStringToByteArray(challenge)
   

      // 서명
      Sign.SignatureData signatureData = Sign.signPrefixedMessage(messageHash, keyPair);
      String signature = Numeric.toHexString(signatureData.getR()) +
            Numeric.toHexString(signatureData.getS()).substring(2) +
            Numeric.toHexString(signatureData.getV()).substring(2);
      System.out.println("Signature: " + signature);
   
      // 서명 검증
      BigInteger publicKey = Sign.signedMessageToKey(messageHash, signatureData);
      System.out.println("Recovered Public Key: " + publicKey.toString(16));
      System.out.println("Original Public Key: " + credentials.getEcKeyPair().getPublicKey().toString(16));
      System.out.println("Signature Verification Result: " + publicKey.equals(credentials.getEcKeyPair().getPublicKey()));
   
      ...

      ```

   <br/>

   - **패스키 (Passkey)**

   - 패스키(Passkey)는 웹과 모바일 애플리케이션에서 사용되는 현대적인 인증 솔루션으로, 비밀번호를 사용하지 않고 보다 안전하고 간편하게 사용자를 인증하는 방식입니다. 패스키는 FIDO(패스트 ID 온라인) 얼라이언스에서 개발한 WebAuthn(Web Authentication) 표준을 기반으로 하며, 사용자 인증을 위한 공통의 인터페이스를 제공합니다.

   - 패스키는 공개키 암호화를 사용하여 작동하며, 사용자 장치에서 생성된 공개키(public key)와 개인키(private key) 쌍으로 구성됩니다. 사용자는 자신의 기기(스마트폰, 태블릿, 컴퓨터 등)에 패스키를 저장하고, 생체 인식(지문, 얼굴 인식) 또는 장치 PIN을 사용해 인증할 수 있습니다. 공개키는 서버에 저장되며, 개인키는 사용자의 기기에 안전하게 보관됩니다. 패스키는 사용자의 개인키를 기기 외부로 노출하지 않기 때문에 높은 보안성을 제공합니다.

   - 패스키는 사용자 경험을 크게 개선합니다. 사용자는 복잡한 비밀번호를 기억할 필요가 없고, 비밀번호 재설정이나 피싱 공격에 대한 걱정 없이 안전하게 로그인을 수행할 수 있습니다. 또한, 패스키는 멀티 기기 환경에서도 원활히 작동하며, 사용자의 기기 간 동기화가 가능합니다.

   - 패스키는 WebAuthn 표준을 따르며, ECDSA(타원 곡선 디지털 서명 알고리즘)를 사용하여 보안을 제공합니다. WebAuthn에서는 NIST 표준에 따라 P-256(secp256r1) 커브를 사용하며 패스키의 공개키는 일반적으로 압축된(compressed) 형식의 약 33 바이트의 길이를 갖습니다. WEB2X 서비스에서 사용되는 공개키는 표준 Base64 인코딩을 통해 문자열로 표현됩니다. Base64 인코딩은 바이너리 데이터를 텍스트로 변환하여, 전송 및 저장이 용이하도록 돕습니다. Base64로 인코딩된 공개키는 길이가 인코딩된 바이트 수에 따라 달라지며, 패딩 문자 =를 포함할 수 있습니다.
   
   <br/>

      1. **패스키 생성 및 키 서명 예시코드 (Javascript)**

   ```javascript
   // 키 생성 함수
   async function generateKey() {
       // WebAuthn 생성 요청 설정
       const publicKey = {
           challenge: new Uint8Array(32), // 랜덤한 값 사용
           rp: {
               name: "Example Corporation",
           },
           user: {
               id: new Uint8Array(16), // 고유한 사용자 ID
               name: "user@example.com",
               displayName: "User Example",
           },
           pubKeyCredParams: [
               {
                   type: "public-key",
                   alg: -7, // ES256 - ECDSA with SHA-256
               },
           ],
           authenticatorSelection: {
               authenticatorAttachment: "platform",
               requireResidentKey: false,
               userVerification: "preferred",
           },
           timeout: 60000,
           attestation: "direct",
       };
   
       try {
           // 키 생성 요청
           const credential = await navigator.credentials.create({
               publicKey,
           });
   
           console.log("Public Key Credential:", credential);
           return credential;
       } catch (err) {
           console.error("Error during key generation:", err);
       }
   }
   
   // 16진수 변환 함수
   function toHexString(byteArray) {
       return Array.from(byteArray)
           .map((byte) => byte.toString(16).padStart(2, '0'))
           .join('');
   }
   
   // 메시지 서명 함수
   async function signChallenge(credential, challenge) {
       // 주어진 해시된 challenge를 사용하여 서명
       const publicKey = {
           challenge: challenge, 
           allowCredentials: [
               {
                   type: "public-key",
                   id: credential.rawId, // 생성된 키의 ID
               },
           ],
           userVerification: "preferred",
       };
   
       try {
           // 서명 요청
           const assertion = await navigator.credentials.get({
               publicKey,
           });
   
           console.log("Assertion:", assertion);
   
           // assertion.response.signature에 서명된 challenge가 포함됨
           const signature = new Uint8Array(assertion.response.signature);
   
           // 서명된 챌린지와 서명 결과를 16진수로 출력
           console.log("Signed Challenge (Hex):", toHexString(challenge));
           
       } catch (err) {
           console.error("Error during message signing:", err);
       }
   }
   
   // 사용 예시
   (async () => {
       const credential = await generateKey();
       if (credential) {
           // WEB2X의 챌린지 API 응답 내 challenge 데이터 입력 (예시)
           const challenge = "0x201850223ca06071ffb0914104ba4dbeffa51e14417aa26e036e7c8a51cd9dd8"
           await signChallenge(credential, challenge);
       }
   })();
   ```
   
   **패스키 생성 예시결과**
   - 패스키 생성 시 아래 JSON 형태의 결과를 확인할 수 있습니다. WEB2X 서비스에서는 결과 데이터 내 public_key 필드의 데이터를 지갑생성 챌린지 API 내 공개키 파라미터로 사용합니다. id 값 또한 서명 시 필요하므로 별도 기록이 필요합니다. 
   ```json
   {
     "id": "-NywVTlXUEoqd5HOrCfJf58t59E",
     "response": {
       "authenticator_data": "...",
       "client_data_json": "...",
       "transports": [],
       "public_key": "MFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAElEitAxLGEpsEK2MQaU3t8RFR0NEBJqBWnQDFoJHIlgzgNdt0C1-2biJsZCwS9u-5qD-   Pr7wcIy8UYfWOmu1LKA==",
       "public_key_algorithm": -7
     },
     "type": "public-key"
   }
   ```


   **패스키 서명 예시결과**
   - 패스키 서명 시 아래 JSON 형태의 결과를 확인할 수 있습니다. WEB2X 서비스에서는 결과 데이터 내 client_data_json, authenticator_data, signature 필드의 데이터를 요청 API 파라미터 내 서명값으로 사용합니다.

   ```json
   {
     "id": "nBmYEcBy5xupLjRGdti7FprUaF0",
     "type": "public-key",
     "authenticator_attachment": "platform",
     "response": {
       "client_data_json": "eyJ0eXBlIjoid2ViYXV0aG4uZ2V0IiwiY2hhbGxlbmdlIjoiQVFBQUFBQUFBUDBNRmZ6THFnRDZmcHVxV05FMU02dkVhd09BU   0hhX284aDNOQ0l1RFU3SCIsIm9yaWdpbiI6Imh0dHA6Ly9sb2NhbGhvc3Q6MzAwMCIsImNyb3NzT3JpZ2luIjpmYWxzZX0=",
       "authenticator_data": "SZYN5YgOjGh0NBcPZHZgW4_krrmihjLHmVzzuoMdl2MdAAAAAA==",
       "signature": "MEQCIFofJWsqFQg-dS9zhTdf-OMIQ9sX3Gld2f_RxEeuLRWpAiBHgXaC-7awLszXBlwfSL3WNGTaDlM_rfyOWi5_wDbugQ==",
       "user_handle": "eWo="
     }
   }
   ```
4. WEB2X API 호출 시 서명 값 사용 방법

   eoakey 혹은 패스키를 이용하여 서명을 완료한 뒤 생성된 서명 값은 아래 코드와 같이 WEB2X 요청 API 호출 시에 사용할 수 있습니다. 

   ```
   // eoakey 서명값 사용
   "credential_data": {
    "signature": "0x7e6884b93962258799b5a74bbb44a1c7b0ae49ceaee0209c4383850b0ca6cd580052889ba35b541e1c9f2bfcbff649e210d8c012f81e55fdf5003473006ba6821c"
   }  
   
   // 패스키 서명값 사용
   "credential_data": {
      "signature": "MEQCIFofJWsqFQg-dS9zhTdf-OMIQ9sX3Gld2f_RxEeuLRWpAiBHgXaC-7awLszXBlwfSL3WNGTaDlM_rfyOWi5_wDbugQ==",
      "client_data_json": "eyJ0eXBlIjoid2ViYXV0aG4uZ2V0IiwiY2hhbGxlbmdlIjoiQVFBQUFBQUFBUDBNRmZ6THFnRDZmcHVxV05FMU02dkVhd09BU   0hhX284aDNOQ0l1RFU3SCIsIm9yaWdpbiI6Imh0dHA6Ly9sb2NhbGhvc3Q6MzAwMCIsImNyb3NzT3JpZ2luIjpmYWxzZX0=",
      "authenticator_data": "SZYN5YgOjGh0NBcPZHZgW4_krrmihjLHmVzzuoMdl2MdAAAAAA=="
   }
   ```



## 챌린지-검증 API 방식

1. 챌린지-검증 방식의 목적과 특징

   챌린지-검증 방식은 API 서비스에서 사용자 인증과 데이터 무결성을 보장하기 위한 방법으로, 다음과 같은 주요 목적을 가집니다.

   - **인증 보장**: 사용자가 자신의 신원을 증명할 수 있도록 합니다. 이는 서비스의 자원에 접근할 때 사용자가 정당한 권한을 가지고 있는지 확인하는 데 중요합니다.
   - **데이터 무결성 검증**: 데이터가 전송 중에 변조되지 않았음을 확인합니다. 데이터 무결성은 데이터가 송수신 과정에서 변경되거나 손상되지 않았음을 보장하는 중요한 보안 요소입니다.

   <br/>

   WEB2X 플랫폼에서는 사용자가 서명 키로 직접 서명한 요청을 지갑에 전달하여 사용자의 요청에 대한 무결성을 보장합니다. 챌린지-검증 방식은 다음과 같은 특징을 가집니다.

   - **보안 강화**: 사용자가 API에 접근하기 전에 챌린지(challenge)라는 도전 과제를 제공하여, 이를 해결하기 위한 서명을 통해 인증을 완료합니다. 이는 비밀번호와 같은 정적인 인증 방식보다 더 강력한 보안을 제공합니다.
   - **단방향성 인증**: 서버가 생성한 챌린지를 통해 사용자는 인증을 완료하게 되며, 이 과정에서 사용자의 개인키 등의 중요 정보가 서버로 전송되지 않습니다. 따라서 보안성이 더욱 향상됩니다.
   - **실시간 인증**: 챌린지를 통한 서명 검증은 실시간으로 이루어지며, 트랜잭션이나 요청 처리 과정에서 사용자가 직접 서명을 수행하여 더욱 빠르고 효율적인 인증을 제공합니다.
   - **확장성**: 다양한 인증 요구에 대응할 수 있는 유연성을 제공합니다. 여러 API 요청이나 서비스 접근 시, 동일한 방식으로 인증을 적용할 수 있어 관리와 운영이 용이합니다.

2. WEB2X API에서의 챌린지-검증

   WEB2X API에서는 챌린지-검증 방식으로 API를 제공하기 위해 지갑에서 실행한 요청 데이터를 챌린지 데이터로 사용합니다. 서비스 이용자가 WEB2X API를 이용하여 지갑에서 특정 기능을 실행하는 과정은 다음과 같습니다.

   1. 서비스 이용자는 지갑에서 실행할 기능에 대해서 WEB2X API의 챌린지 API를 먼저 호출하여 챌린지 데이터를 받습니다.
   2. 서비스 이용자는 지갑에 등록된 서명 키를 이용하여 챌린지 데이터를 서명합니다.
   3. 서비스 이용자는 챌린지 데이터를 서명한 서명값을 기능에 맞는 요청(트랜잭션) API를 통해 WEB2X API 서버로 전달합니다.
   4. 서비스 이용자는 'API 결과 조회' API를 통해 자신이 요청한 API의 처리 결과를 확인합니다.

   **정보**: WEB2X 플랫폼은 챌린지-검증 방식을 모든 API에서 사용하지 않습니다. 챌린지-검증 방식을 사용하는 API는 챌린지 API와 요청 API가 쌍으로 존재합니다.

   **정보**: 챌린지 API는 트랜잭션 요청 준비를 위한 단계이므로 챌린지 API만 호출한 상태에서는 지갑에 대한 요청이 처리되지 않습니다.

## 요청결과 조회 방법

WEB2X 플랫폼은 API를 통해 서비스 이용자의 요청을 받아 블록체인 네트워크에 실제 트랜잭션을 전파하여 요청을 처리합니다. 블록체인
네트워크의 특성상 트랜잭션 처리(새로운 블록이 생성되기까지)에 시간이 소요되므로 WEB2X API는 비동기 방식으로 처리를 진행합니다.
따라서, 서비스 이용자는 WEB2X API의 처리 결과를 비동기적으로 확인해야 합니다. WEB2X API에서는 이러한 비동기 처리 결과를
API 호출 방식과 콜백 방식으로 모두 제공합니다.

<p><br/></p>

1. 'API 결과 조회' API 호출 방식

   API 호출 방식은 서비스 이용자가 직접 요청의 상태를 조회하는 방식입니다.

   - API 요청 처리가 완료되지 않았다면 '처리중(PENDING)' 상태를 반환합니다.
   - API 요청 처리가 완료되면 처리 결과 정보(Request ID)를 응답으로 받습니다.
   - 서비스 이용자는 주기적으로 'API 결과 조회' API를 호출하여 요청의 처리 상태를 확인해야 합니다. (권장 주기: 1~5초)
   - WEB2X 플랫폼 혹은 블록체인 네트워크 상황에 따라 처리 소요 시간이 변동 될 수 있습니다.

   **주의**: 일반적으로 처리 시간은 수 초 혹은 수십 초 내에 완료되지만, 예외적인 경우에는 고객센터로 문의 바랍니다.

   <br/>

   **'API 결과 조회' API의 데이터 예시**

   - 처리 성공 상태 (API 별로 results 내 추가 데이터가 포함될 수 있음)

     ```json
     {
       "code": "20000",
       "message": "SUCCESS",
       "request_id": "ac7f1ec3-ae32-4cfd-9767-d10495f1ce9a",
       "status": "COMPLETE", // 요청 처리 성공
       "results": {
         "transaction_hash": "0xf174631f476cfb63f49f945c70e8d1db0fce39e009fe226f41b3bbdf172a5cd5",
         "transaction_gas_used": 118012,
         "transaction_fee": "0.239949336000000000",
         "requested_at": "2024-07-17T08:31:23+09:00",
         "finished_at": "2024-07-17T08:31:33+09:00"
       }
     }
     ```

   - 처리 진행 중 상태

     ```json
     {
       "code": "20000",
       "message": "SUCCESS",
       "request_id": "0f564185-a73d-4028-a42d-7b4483ce28d8",
       "status": "PENDING", // 요청 처리 중
       "results": {
         "requested_at": "2024-07-15T03:18:00+09:00"
       }
     }
     ```

   - 처리 실패 상태 (트랜잭션 전송 실패)

     ```json
     {
       "code": "20000",
       "message": "SUCCESS",
       "request_id": "b4a8894e-436e-4810-a6b6-5f031f1c2f27",
       "status": "FAILED", // 요청 처리 실패
       "reason": "failed to send transaction", // 실패 사유
       "results": {
         "finished_at": "2024-07-17T10:53:32+09:00",
         "requested_at": "2024-07-17T01:53:30+09:00"
       }
     }
     ```

   - 처리 실패 상태 (트랜잭션 실행 실패(revert))

     ```json
     {
       "code": "20000",
       "message": "SUCCESS",
       "request_id": "45501dc1-e1e2-4808-bdb1-8058cb08a653",
       "status": "FAILED", // 요청 처리 실패
       "reason": "transaction is reverted", // 실패 사유
       "results": {
         // 실패로 인해 Revert 된 트랜잭션 정보
         "transaction_hash": "0x5d50abefc87f2e894a1b62e2ae8143800532d71f499c64c836c9b68f7f764b0f",
         "transaction_gas_used": 2426585, // 실패에 소모된 Gas
         "transaction_fee": "0.239949336000000000",
         "requested_at": "2024-07-17T08:31:23+09:00",
         "finished_at": "2024-07-17T08:31:33+09:00"
       }
     }
     ```

2. 콜백 방식

   콜백 방식은 요청 처리가 완료되면 WEB2X 플랫폼이 서비스 이용자에게 결과를 전달하기 위해 콜백 API를 요청하는 방식입니다.

   - 서비스 이용자는 챌린지 API 호출 시 콜백을 받을 주소를 지정해야 합니다. 이 주소는 API 호출을 완료한 후 결과를 전달 받기 위해 필요합니다. 또한, 지정한 주소로 콜백 API를 구현해야 합니다.
   - 각 API 별 콜백으로 전달받은 데이터 규격은 WEB2X API 문서를 참고하세요.
   - 서비스 이용자의 콜백 주소가 유효하지 않거나 네트워크 상태가 불안정할 경우 콜백 요청이 실패할 수 있습니다.
   - 요청에 대한 콜백은 성공이나 실패 등 요청에 대한 처리가 완료된 시점에 호출됩니다.

   <br/>

   **콜백 API 요청 시 BODY 파라미터 예시**

   - 처리 성공 상태

     ```json
     {
       "request_id": "ac7f1ec3-ae32-4cfd-9767-d10495f1ce9a",
       "status": "COMPLETE", // 요청 처리 성공
       "results": {
         "transaction_hash": "0xf174631f476cfb63f49f945c70e8d1db0fce39e009fe226f41b3bbdf172a5cd5",
         "transaction_gas_used": 118012,
         "transaction_fee": "0.239949336000000000",
         "requested_at": "2024-07-16T23:31:29+09:00",
         "finished_at": "2024-07-17T08:31:33+09:00"
       }
     }
     ```

   - 처리 실패 상태 (트랜잭션 전송 실패)

     ```json
     {
       "request_id": "b4a8894e-436e-4810-a6b6-5f031f1c2f27",
       "status": "FAILED", // 요청 처리 실패
       "reason": "failed to send transaction", // 실패 사유
       "results": {
         "finished_at": "2024-07-17T10:53:32+09:00",
         "requested_at": "2024-07-17T01:53:30+09:00"
       }
     }
     ```

   - 처리 실패 상태 (트랜잭션 실행 실패(revert))

     ```json
     {
       "request_id": "45501dc1-e1e2-4808-bdb1-8058cb08a653",
       "status": "FAILED", // 요청 처리 실패
       "reason": "transaction is reverted", // 실패 사유
       "results": {
         // 실패로 인해 Revert 된 트랜잭션 정보
         "transaction_hash": "0x5d50abefc87f2e894a1b62e2ae8143800532d71f499c64c836c9b68f7f764b0f",
         "transaction_gas_used": 2426585, // 실패에 소모된 Gas
         "transaction_fee": "0.239949336000000000",
         "requested_at": "2024-07-16T23:58:57+09:00",
         "finished_at": "2024-07-17T08:59:02+09:00"
       }
     }
     ```

   <br/>

   **주의**: 콜백 API를 수신하는 WEB2X API 서버의 IP는 다음과 같습니다. 서비스 이용자는 콜백 요청이 정상적으로 처리될 수 있도록 해당 IP를 방화벽 화이트리스트에 등록하여야 합니다.

   ```plaintext
   // 콜백 발신 IP 목록

   13.124.113.189
   ```
