---
layout: post
title:  " BlockChain (1) "
categories: BlockChain
author: goodGid
---
* content
{:toc}






  /assets/img/block_chain/ethereum.png)



* 원문은 [Blog](http://www.chaintalk.io/archive/lecture/1)에서 확인하자 !

* 아래는 위 Blog에서 핵심적인 부분(주관적)을 발췌하였다.

---

이더리움은 

기존의 비트코인처럼
<br><br>
  

이더 자체를

달러나 원화와 같은 화폐를

대체하기 위한
<br><br>

 
새로운 지불수단으로서의

기능을 구현하려고

만들어진 것이 아닙니다.
<br><br>
 

물론 이더리움도 비트코인처럼

지불수단으로서의 기능도

훌륭히 수행할 수 있고,
<br><br>
 

비트코인과 비교하면

처리용량, 속도, 옵션 추가 등의 면에서

더 발전된 형태의 수단입니다.
<br><br>
 

하지만 `이더리움`의 `진정한 가치`는

단순한 지불 수단의 의미를 넘어서서,

매우 `다양한 스마트 컨트랙트`와

이를 바탕으로 한 `탈중앙화된 어플리케이션(dApp)`을

만들 수 있는 `플랫폼`이라는 점에 있습니다.
<br><br>


2008년 비트코인의 등장 이후

비트코인의 단점을 해결하기 위한

정말 무수히 많은 카피코인들이

많이 나왔었습니다.
<br><br>
 

이 가운데는 지불 수단 이외의

여러 가지 특수한 기능들을

구현해보기 위한 시도들도 많았습니다.
<br><br>

 
하지만 대부분의 이러한 시도는

어떤 특정한 문제 하나를

해결하기 위한

단순한 시도들이었습니다.

좀 더 철학적 용어로

자기완결적인 시도들이다

이렇게 이야기합니다.

외부로의 확장성이 적다는거죠.

그 안에서만 놀고 끝낸다 이런 이야기.
<br><br>


즉, 별도의 독자적인 블록체인을 만들고,

필요한 기능을 구현하기 위한 코드들을

전부 자체적으로 다 구축하는 방식이었습니다.

그 블록체인을 유지하기 위한

인프라(채굴, 합의시스템 등)도

별도로 구축해야 했습니다.

대충 듣기만 해도 좀 비효율적이다

이런 생각이 듭니다.
<br><br>
 

이러한 독립적인 체인과 시스템이

유리한 경우도 분명히 있습니다.
<br><br>
 

하지만,

많은 경우에 충분한 리소스가 없는 상태에서

안정적으로 이러한 시스템을 개발, 유지, 확대하는 것은

무척 어려운 일입니다.
<br><br>
 

몇 년간 수도 없이 많은 코인들이

나타났다가 쉽게 사라지는 것이

바로 이 이유 때문입니다.
<br><br>
 

또한 이렇게 만들어진 여러 블록체인/코인 들 간에

상호운용성이 결여 되어 있다보니,

서로 시너지 효과를 살리지 못하고

단절되어 독자적인 생태계를 확보해야하는

어려움에 직면하게 됩니다.
<br><br>
 

`이더리움`은

이러한 블록체인 개발 환경을

보다 `통합적`이고 `상호 유기적`으로

발전시킬 수 있도록,
<br><br>
 

여러 `어플리케이션`의 `공통 분모`를

`플랫폼`으로 만들어 버리고자 한 것입니다.

특수한 기능을 구현하기 위해,

별도의 체인을 다시 만들 필요 없이,

공통의 이더리움 체인을 기반으로 해서,

공통의 개발환경과 개발언어를 사용해서

보다 효율적으로 어플리케이션을

만들 수 있게 하자는 것이지요.
<br><br>

 
비탈릭이 이더리움이 무엇인지를

설명하는 프리젠테이션에 항상 등장하는 그림이 있는데,

이더리움의 장점과 특징을 잘 설명하고 있다고 봅니다.
<br><br>


단일 기능에 특화되어 있는 기존의 솔루션들은

이런 계산기와 같습니다.

한 가지 기능만을 잘 수행하기 위해 만들어져 있습니다.
<br>


  /assets/img/block_chain/blockchain(1)_1.png)



조금 더 발전된 형태는 이 정도입니다.
<br>


  /assets/img/block_chain/blockchain(1)_2.png)


<br>

이들 툴에 비교하자면 이더리움은 스마트 폰과 같습니다.


  /assets/img/block_chain/blockchain(1)_3.png)


<br><br>


즉, `이더리움`은 특정한 기능 몇 가지를

구현하기 위해서 만들어진 어플리케이션이 아니라,

온갖 종류의 다양한 `탈중앙화된 어플리케이션(dApp)`을

만들 수 있도록 해주는 `베이스 플랫폼`입니다.
<br><br>


범용 플랫폼이다 보니,

이더리움 시스템의 개발에는

더 많은 노력과 시간이 필요한 것은

사실입니다.
<br><br>
 

새로 윈도우즈나 리눅스를 만든다고

생각해보시면 되십니다.

대단히 규모가 큰 프로젝트인거죠.
<br><br>
 

전체 블록체인 사이즈 스케일링도

매우 중요한 이슈가 됩니다.

많은 어플리케이션들의 로직과 데이터를

다 담아야 되니까
<br><br>
 

체인의 부피도 커지고

효율적인 속도를 유지하는 것도

매우 어려운 과제가 됩니다.
<br><br>
 

하지만 좋은 아이디어가 있어서

이를 블록체인을 이용해

구현해보려는

많은 개발자들에게는

너무나 반가운 시스템이

아닐 수 없습니다.
<br><br>
 


체인 자체를 개발하고 운영해야 하는

모든 수고를 다 들어주기 때문입니다.

구현하려고 하는 비지니스 로직자체에

촛점을 맞추면 되기 때문입니다.
<br><br>
 

 
비유를 하자면 기존 웹사이트 하나를 만들기 위해서

아파치 웹서버 자체를 본인이 다 코딩해서 만들어야 된다고 한다면,

사이트 하나 만들기 위해 얼마나 많은 시간과 노력이 들어갈까요?
<br><br>
 

아파치 서버를 잘 쓰기 위한

기본적인 지식과 셋팅 노하우만 있으면

아파치 서버 내부의 로직을 정확히 알지 못해도

웹 사이트 를 만드는 과정에 별 장애가 안됩니다.

이더리움 플랫폼이 블록체인을 기반으로

한 어플리케이션 개발에 얼마나 중요한 역할을

할지 알 수 있는 하나의 대목입니다.
<br><br>



제가 아직 미흡한 수준임에도 불구하고,

dApp 개발 시리즈를 시작할 수 있게 한 것도

바로 이러한 이더리움 플랫폼이 가진 장점 때문입니다.
<br><br>
 

dApp을 돌아가게 하는 모든 내부 메카니즘과 코드를

일일히 다 들추어서 보여주지 않더라도,

dApp의 기본적인 구성과 작동 메카니즘을

보여줄 수 있기 때문입니다.
<br><br>
 

그만큼 dApp 개발에 참여할 수 있는 문턱이

낮아졌다는 것을 의미합니다.
<br><br>


물론 아직 이더리움이 완성단계가 아니기 때문에,

보안과 여러 가지 성능 향상을 위해서는

내부 메카니즘에 대한

보다 세부적인 이해가 절대적으로 필요한 경우도 있고

많은 도움이 될 때도 있습니다.
<br><br>

 

한글로 된 dApp개발 강좌나 문서가

너무나 부재한 상태에서

저의 이 시리즈가 dApp 에 대한

한국 개발자들의 관심을 불러일으키고,

처음으로 dApp에 입문하는 사람들에게

조금이라도 도움이 되었으면 하는 바램입니다.
<br><br>
 


설사 dApp 개발에 직접 참여하지 않더라도,

이더리움에 관심이 있는 분이라면,

한번 쯤 배워보는 것도 나쁘지 않다고 봅니다.

이더리움에 대한 심층적인 이해에 많은 도움이 될 것입니다.
<br><br>

[다음 편](https://goodgid.github.io/BlockChain(2)/)

