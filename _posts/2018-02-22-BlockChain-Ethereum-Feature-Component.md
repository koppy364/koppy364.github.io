---
layout: post
title:  " Ethereum Feature & Component "
categories: BlockChain
author: goodGid
---
* content
{:toc}

## Ethereum Feature

### 기존 비트코인과 동일 속성

\- 1. 익명성(Anonymity) : 애초에 어떤 개인정보도 입력하지 않기 때문에 개인 정보 유출의 염려가 없다.

\- 2. 무국격성(Boderlessness) : 네트워크 상에 존재하는 것이므로, 국격에 구애받지 않아 범국가적으로 사용될 수 있다.

\- 3. 탈중앙성(Decentralization) : 중앙관리서버나 주체가 없으므로 시스템을 장악하거나 변조하여 유용할 수 없다.

\- 4. 분산 네트워크(Distributed network) : 하나의 서버가 아니라 근처 노드에 얽혀있어 

중앙서버를 공격해 시스템을 다운시키는 것이 불가능하다.

<br>

\- 5. DDoS차단 : 수수료 시스템이 있기 때문에 DDoS공격을 통한 시스템 마비가 불가능

즉 애초에 막대한 자본이 없다면

블록체인 상에서는 

각 작업에 수수료를 청구하고 있으므로 

DDoS 공격이 불가능

<br>

\- 6. 분할성(Divisibility into pieces) : 화폐의 단위를 낮게 분할 가능

암호화화폐(Crypto Currency)는 원하는 가격에 맞게 지출하기 때문에 

단위를 무한히 낮출 수 있다.

<br>

\- 7. 투명성(Transparency) : 각 블록 안에 포함된 거래내역을 모두 조회 가능하다. 

또한 시스템이 구동되는 원리가 포함된 소프트웨어 소스자체가 모두 공개되어있다.

<br>

<br>

### 진보 속성

\- 1. [튜링완전성(Turing Completeness)](https://goodgid.github.io/BlockChain-Ethereum/) : 이더리움을 사용하는 과정에서 튜링완전한 언어를 사용 가능

\- 2. 플랫폼을 통한 응용성(dApps on Platform) : 서비스를 창조해낼 수 있는 거대한 플랫폼이기 때문에 무한한 응용이 가능

\- 3. 스마트 컨트랙트(Smart Contract) : 자기강제적언어(Self-Enforcing Language)

이더리움을 통해 여러가지 계약을 창조해낼 수 있으며,

상호 신뢰가 어려운 디지털 환경에서

파기할 수 없는 강력한 계약을 

프로그램이 자동적으로 수행되게 하는

스마트 계약을 제공할 수 있다.

<br>

===> 이더리움은 위와 같은 진보한 특징들을 통해, 

사실상 상상 가능한 모든 형태의 거래를 프로그래밍 할 수 있으며,

전혀 다른 차원의 높은 자유도와 효과성을 누릴 수 있다.

<br>


## Ethereum Component 

* Prev Hash : 이전 블록의 해시 값을 지칭(Parent Hash)

* Nonce : 작업증명 시 이용되는 64비트 해시로, 충분한 양의 계산을 위해 이용

* Timestamp : 유닉스 time() 함수의 출력 값으로 생성 시간을 의미

* Uncles Hash : 블록의 Uncle 목록의 SHA3 해시

* Beneficiary : 채굴 성공 시 모든 수수료가 전송되는 160비트 주소

* Logs Bloom : Bloom filter는 거래 목록의 각 거래 영수증에서 각 로그항목에 포함된 색인 정보(로그 주소 및 주제를 기록)로 구성

* Difficulty : 블록의 난이도에 해당되는 값으로 이전 블록의 난이도 및 Timestamp로부터 계산

* Extra Data : 블록과 관련된 데이터를 포함하는 임의의 바이트 배열

* Block Num : 상위 블록의 수

* Gas Limit : 블록 당 가스 비용을 제한하는 값

* Gas Used : 블록에서 트랜잭션에 사용된 총 가스 값

* Mix Hash : 충분한 양의 계산을 위해 블록에 수행되는 Nonce와 작업 증명을 하는데 이용되는 256비트 해시

* State Root : 모든 트랜잭션이 실행된 후 완결 짓는데 적용되는 상태 트리의 루트 노트(SHA-3 해시 값)

* Transaction Root : 블록의 거래 목록 부분에 각 트랜잭션으로 채워진 상태 트리의 루트 노드(SHA-3 해시 값)

* Receipt Root : 블록의 거래 목록 부분에 각 거래 영수증으로 채워진 상태 트리의 루트 노드(SHA-3 해시 값)

---


## Bitcoin vs Ethereum

|   특징       | Bitcoin    | Ethereum |
|:-------:|:-------:|:-------:|
| 기능 <br> <br>  | 화폐로서의 교환 기능에 중점 <br> <br>  | 화폐로서의 교환 기능에 중점 <br> 프로그램 실행을 위한 기능 추가 <br> <br> |
|----|----|----|
| 설계 사상 <br> <br>   | 블록체인 기술에 기반하여 <br> 안전한 암호 화폐 시스템으로 설계됨 <br> <br>   | 블록체인을 기반으로 <br> 다양한 분산 어플리케이션을 개발하고 <br> 구동할 수 있는 플랫폼으로 설계됨 <br> <br> |
|----|----|----|
| 방식 <br> <br>  | 튜링 미완전성 <br> <br> | 튜린 완전성 <br> <br> |
|----|----|----|
| 화폐 가치 <br> <br>  | 화폐 가치의 불투명성 <br> 가치를 쉽게 알지 못함 <br> <br>  | 화폐 가치의 투명성 <br> 가치 파악이 쉬움  <br> <br> |
|----|----|----|
| 상태  <br> <br> | 상태의 단순성 <br> (사용 유무 비트코인 상태밖에 없음) <br> <br>| 할부나 여러 조건에 따른 이용 가능  <br> <br> |
|----|----|----|
| 검증 시간 <br> <br>  | 한 블록 생성시간 10분 <br> <br>  | 한 블록 생성시간 12초  <br> <br> |
|----|----|----|
| 주요 속성  <br> <br> | 익명성, 무국경성, 탈중앙성 <br> 분산 네트워크, 분할성 <br> 투명성 등의 속성을 보유  <br> <br> | 가상화폐의 속성을 동일하게 보유하면서 <br> 진보된 속성인 튜링완전성, 플랫폼 응용성 <br> 스마트 컨트랙의 속성을 보유  <br> <br> |
|=====|=====|=====|



