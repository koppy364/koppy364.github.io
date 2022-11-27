---
title: "데이터베이스"
excerpt: "데이터베이스 정리"
toc: true
toc_sticky: true
categories:
 - interview
tag:
 - DB
---

# 1. 데이터베이스(Database)
여러 사람이 공유하여 사용할 목적으로 체계화해 통합, 관리하는 데이터의 집합이다.

## 1.1 용어
  1. 열(column) - 필드(field) 또는 속성(attribute)이라고도 부른다.  
  2. 행(row) - 튜플(tuple) 또는 레코드(record)라고도 부른다.
  3. 값(value) - 각각의 행과 열에 대응하는 값.
  4. 스키마(schema) - 데이터베이스를 구성하는 요소를 정의한것.


## 1.2 Key
검색, 정렬시 Tuple을 구분할 수 있는 기준이 되는 Attribute.  


1. Candidate Key (후보키)
  - Tuple을 유일하게 식별하기 위해 사용하는 속성들의 부분 집합.(기본키로 사용가능한 속성들)
  - 유일성 : Key로 하나의 Tuple을 유일하게 식별할 수 있어야 한다.
  - 최소성 : 꼭 필요한 속성으로만 구성
2. Primary Key (기본키)
  - 후보키 중 선택한 Main Key
  - Null값을 가질 수 없다.
  - 동일한 값이 중복될 수 없다.
3. Alternate Key (대체키)
  - 후보키 중 기본키를 제외한 나머지 키 = 보조키
4. Super Key (슈퍼키)
  - 유일성은 만족하지만, 최소성은 만족하지 못하는 키
5. Foreign Key (외래키)
  - 다른 릴레이션의 기본키를 그대로 참조하는 속성의 집합  

-----

# 2. 데이터베이스의 특징
1. **실시간 접근성(Real-Time Accessibility)** : 비정형적인 질의(조회)에 대하여 실시간 처리에 의한 응답이 가능해야 하며,  
2. **지속적인 변화(Continuous Evloution)** : 데이터베이스의 상태는 동적이다. 즉 새로운 데이터의 삽입(Insert), 삭제(Delete), 갱신(Update)으로 항상 최신의 데이터를 유지해야 한다.  
3. **동시 공용(Concurrent Sharing)** : 데이터베이스는 서로 다른 목적을 가진 여러 응용자들을 위한 것이므로 다수의 사용자가 동시에 같은 내용의 데이터를 이용할 수 있어야 한다.  
4. **내용에 의한 참조(Content Reference)** : 데이터베이스에 있는 데이터를 참조할 때 데이터 레코드의 주소나 위치에 의해서가 아니라 사용자가 요구하는 데이터 내용으로 찾는다.  


-------

# 3. 데이터베이스 언어(DDL, DML, DCL)
1. **DDL (정의어 : Data Definition Language)** : 데이터베이스 구조를 정의, 수정, 삭제하는 언어 ( alter, create, drop )  
2. **DML (조작어 : Data Manipulation Language)** : 데이터베이스내의 자료 검색, 삽입, 갱신, 삭제를 위한 언어 ( select, insert, update, delete )
3. **DCL (제어어 : Data Control Language)** : 데이터에 대해 무결성 유지, 병행 수행 제어, 보호와 관리를 위한 언어 ( commit, rollback, grant, revoke )

------

# 4. Join
  두개 이상의 테이블이나 데이터베이스를 연결하여 데이터를 검색하는 방법
## 4.1 JOIN 종류
  1. INNER JOIN
  2. LEFT OUTER JOIN
  3. RIGHT OUTER JOIN
  4. FULL OUTER JOIN
  5. CROSS JOIN
  6. SELF JOIN
  
