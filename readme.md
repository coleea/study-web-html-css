# css-in-depth 정리물

<img src="./img/css-in-depth-book.png" width="200px" />

- [챕터 1](./css-in-depth-study/챕터_01.md) <- 링크를 클릭

- [챕터 3](./css-in-depth-study/챕터_03.md) <- 링크를 클릭

---

# 웹 펀더멘탈

<img src="./img/web_fundamentals.jpg" width="500px" />

#### Q. 네트워크 요청시에 직렬화를 하라는데 직렬화가 뭔가?

A. 직렬화란 특정한 자료구조를 문자열로 바꾸는 작업이다
http 통신시에 서버로 넘어가는 패킷은 문자열이므로 그 패킷안에 포함되는 자료 역시 문자열이 되어야 한다
js에서는 `JSON.stringify(객체)`를 직렬화 방법으로 사용한다

#### Q. 지라(jira)가 뭔가?

지라는 프로젝트 스케줄 매니지먼트 툴이며 이 툴을 이용해서 개발자간 작업을 분배한다\
전체적인 프로젝트 진행 상황을 확인하고 프로젝트 일정을 조율하고 수정하는 등의 기능을 수행한다\
지라 대신 노션(notion), 콘플루언스(confluence), 트렐로(trello) 등을 쓰기도 한다

#### Q. CI/CD가 뭔가?

A. CI는 지속적 통합(Continuous Integration)의 약자이고 CD는 지속적 배포(Continuous Deployment)의 약자이다. 이렇게 말해도 전혀 감이 오지 않을 것이다
먼저 지속적 통합(CI)은 여러 개발자가 하나의 리포지토리에 커밋한 코드를 통합하는 작업이다. 이 통합 과정에서 코드가 정상적으로 작동하는지 여부가 자동으로 테스트된다. 만일 통합한 코드가 정상적으로 실행되지 않는다면 개발자는 즉각적으로 그 피드백을 받아서 문제가 있는 코드를 수정할 수 있다. 이러한 통합의 자동화 프로세스는 개발 사이클을 빠르게 만드는데 일조한다\
지속적 배포(CD)는 엔드유저가 서비스를 이용할 수 있도록 배포하는 마지막 단계를 뜻한다. 이 배포도 마찬가지로 자동으로 수행된다\
깃헙 페이지(Github Pages)로 블로그를 만들어 본 개발자라면 커밋하는 즉시 블로그가 업데이트되거나 배포에 문제가 발생할 경우 이메일로 경고알람이 도착하는 것을 경험했을 것인데 이러한 자동 배포 프로세스도 일종의 지속적 배포(CD)에 속한다\
이러한 CI/CD 툴로는 `젠킨스(Jenkins)`가 전통적으로 사용되었으나 그 사용의 복잡성 문제로 여러 대안들이 등장했다. 대표적인 대안으로는 `AWS CodeBuild`나 `github actions`등이 있다

#### Q. 데스옵스 엔지니어가 뭔가?

간단히 말해서 DevOps 엔지니어는 개발 파이프라인 문제를 해결하는 엔지니어이다.\
이들은 팀 간의 의사소통이나 회의 및 의견조율, 갈등해소 등 개발의 시작부터 끝까지 발생하는 모든 파이프라인에 대한 책임을 수행한다\
이들은 디테일한 로직을 개발하는데 초점을 맞추기 보다는 팀과 팀간의 의사소통을 조율하는 역할을 주로 수행한다

#### Q. 사이트 신뢰성 엔지니어(SRE)가 뭔가 ?

A. SRE는 쉬운말로 인프라를 관리하는 개발자이다\
웹앱의 예를 들자면 웹앱의 배포, 장애관리, 확장 등 전반적인 인프라 관리 작업을 담당하며 안정적인 서비스 운영에 대한 신뢰성을 책임지는 개발자이다. 노골적으로 이야기하면 서버가 뻗지 않도록 관리하며 서버가 느려지거나 그 외의 모든 장애요인을 사전에 파악하고 원천차단하여 365일 24시간 언제나 서비스가 최상의 상태를 유지할 수 있도록 관리하는 업무를 수행한다\
2000년대 초반에 온라인 게임을 해본 유저들은 대부분 공감하는 이야기일 텐데 서버가 뻗는 일이 잦았다. 디아블로2 초창기는 서버가 정상적으로 돌아가는 때를 찾아보기 힘들 정도였다. 이것은 SRE담당자가 사전에 트래픽 파악을 하는데 실패했거나 트래픽을 어느정도 예상했더라도 그에 걸맞는 서버 확장에 실패한 케이스인데 만일 유능한 SRE담당자가 있었더라면 이런 참극은 피할 수 있었을 것이다\
SRE는 시중에 오픈소스로 돌아다니는 도커나 쿠버네틱스 등의 도구로 시스템을 관리하거나 필요에 따라서 본인이 직접 만든 프로그램을 이용하여 인프라를 관리한다. 대기업에 재직중인 SRE라면 많게는 수십만 대에 이르는 서버의 관리 및 확장을 책임지기도 하여 그 책임이 막중하다 할 수 있다\

#### Q. 웹브라우저에서 preload scanner가 뭔가 ?

A. html의 헤더 태그안의 link 태그 중에서 프리로드할 대상을 스캔하는 웹브라우저 엔진 내부의 모듈을 뜻한다\
프리로드 스캐너는 다운로드 해야할 리소스를 검출하고 그 리소스의 URL을 네트워크 프로세스에 전달하는 역할을 수행한다

#### Q. 누진적 레이아웃 변화(Cumulative Layout Shift, CLS)가 뭔가?

A. 웹 페이지를 읽을 때 레이아웃이 변화하는 현상은 `누진적 레이아웃 변화` 라는 지표로 표시된다. 레이아웃의 변화는 유저에게 안좋은 경험으로 다가오며 이용만족도에 악영향을 준다. 그러므로 `누진적 레이아웃 변화` 지표를 감소시킬수록 보다 나은 사용자에 일조한다\
`누진적 레이아웃 변화`를 개선하는 방법 중 하나로 스켈레톤 컴포넌트가 사용된다

#### Q. 스켈레톤 컴포넌트가 무엇인가 ?

A. 스켈레톤 컴포넌트란 실제 콘텐츠가 들어가게 될 자리를 잠시 대신할 빈 껍데기다.\
스켈레톤 컴포넌트는 일반적으로 흰색 배경에 회색으로 레이아웃이 표시되는 박스 형태로 표시된다. 예를들어 아래와 같다

<여기에 스켈레턴 컴포넌트의 이미지를 삽입하시오>

일반적으로 지루한 로딩시간을 달래기 위한 목적으로  스켈레톤 컴포넌트를 사용한다고들 하지만 그 외의 목적도 있는것이다. 위에서 말했듯 레이아웃 쉬프팅 현상을 방지하기 위한 용도로도 사용된다 

는 그저 화면의 레이아웃을 보여주는 컴포넌트이다. 이러한 스켈레톤 컴포넌트는 어떻게 만들 수 있을까 ?
일단 이미지에 대하여 수행할 수 있다.

1. 디자이너와 상담하여 이미지 비율을 결정합니다.
2. image onLoad 전은 자리 표시자의 요소를 표시시켜 높이를 유지하고 onLoad 후에 교체
자리 표시자의 요소를 이미지가 로딩되기도 전에 표시하는건 간단하다. 그저 width, height를 표기해주면 될 뿐이다
3. 정해진 비율에 부족한 부분은 자리 표시자의 색을 남기도록 한다(imageMagick의 기능을 사용)

#### Q. Core Web Vitals가 무엇인가 ?

A. 코어 웹 바이탈스는 W3C에서 만든 용어는 아니며 구글에서 만든 용어이다.\
이상적인 웹페이지를 만드는데 3가지가 필요하다고 한다\
첫쨰로 페이지가 로딩되는 시간, 둘째로 유저와의 상호작용이 얼마나 빨리 이루어지는가. 이것은 first input delay라는 지표로 판단된다. First Input Delay는 첫 번째 입력까지의 지연을 나타냅니다. 응답성을 측정하여 사용자가 먼저 페이지를 조작하려고 할 때 느끼는 경험을 정량화합니다.\
\
셋째로 웹페이지가 얼마나 일관된 UI를 제공해주는지를 살핀다. 이것은 Cumulative Layout Shift라는 지표로 측정된다. Cumulative Layout Shift는 페이지가 얼마나 안정적으로 느껴지는지 나타냅니다. 시각적 안정성을 측정하고 표시되는 페이지 콘텐츠의 예기치 않은 레이아웃 편차의 양을 정량화합니다.\
\
코어 웹 바이탈스에 대한 자세한 내용은 https://web.dev/i18n/ko/vitals/ 를 참조하라

#### Q. 웹 아키텍처 중에서 잼스택이란 것이 있다는데 잼스택이 무엇인가 ?

A. 정적파일들의 집합. 이 파일들은 CDN에서 배포된다.
정적파일들을 다운로드받은 클라이언트는 서버리스 혹은 헤드리스 CMS에 접속하여 추가적인 데이터를 다운로드 받는다. 즉 REST API나 Realm등을 호출하여 데이터를 다운로드 받는 형식이다. 이러한 잼스택은 기존의 서버 모델과는 다르게 중앙서버가 없다는 특징이 있다

#### Q. 렌더-블로킹 리소스가 무엇인가 ? (Render-blocking resources)

A. 렌더링시에 메인스레드를 블로킹하는 프로세스를 일컫는다. 브라우저가 페이지 내용을 화면에 렌더링하는 것을 차단하거나 지연시키는 스크립트 로딩, 스크립트 실행, 스타일시트 로딩, HTML 임포트 등의 작업을 일컫는다

#### Q. 웹애서 i18n이란 무엇인가 ?

A. i18n은 Internationalization의 약자이다. 웹페이지의 국제화라는 뜻이다\
첫글자와 마지막 글자 사이에 문자가 18개가 있어서 축약형으로 i18n 이라 불린다\
접속하는 클라이언트의 지역을 파악하여 해당 지역의 언어로 페이지를 렌더링하는 방식을 일컫는다\
웹브라우저에 설정된 디폴트 언어를 탐지하고 그 언어에 맞는 문자열을 가져오는 방식으로 작업이 수행된다\
\
참고 : https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Internationalization

#### Q. i18n을 구현할 때 해당 국가의 언어를 모를때는 어떻게 해야하는가 ?

A. 유저가 번역하도록 유도하는 방법을 택할 수 있다. 웹브라우저 화면상에 마우스 오른쪽 버튼을 클릭하면 번역 기능이 있으니 그것을 이용할 수 있다

#### Q. 만일 유저가 웹브라우저의 번역 기능을 이용해서 번역을 했는데 내가 번역을 원치 않는 컨텐츠까지 번역을 하면 어떻게하는가 ?

A. 그런 우려를 종식시키기 위해서 크롬에서는 translate 어트리뷰트를 만들었다. 아래와 같이 사용한다
`<p translate="no">hello</p>` 
이렇게 `translate="no"` 어트리뷰트가 기입된 엘리먼트는 번역을 수행하지 않는다

#### Q. 프론트엔드에 대한 백엔드 패턴(backend for frontend)이 무엇인가 ? 

A. 모바일 환경은 화면 크기나 cpu성능 등이 데스크톱과 다르다. 결과적으로 모바일 백엔드에 대한 요구사항은 데스크톱과 다를 수 있다\
모바일 환경과 데스크탑 환경에 대한 요구사항을 하나의 백엔드 팀에서 관리하는 경우 서로 상충되는 요구사항을 해결해야 하는 상황이 있는데 이러한 요구를 논의하고 결정하는 과정에서 개발시간이 지연될 수 있다. 하지만 모바일용 백엔드 환경과 데스크탑용 백엔드 팀이 별도로 운영되고 있다면 이런 상충되는 요구 사항을 절충할 필요가 없이 즉각적인 개발에 돌입할 수 있다\
따라서 모바일용 웹페이지와 데스크탑용 웹페이지를 별도로 개발하는 경우 백엔드 팀을 두개로 분리해서 개발하면 생산성 향상에 도움을 받을 수 있다. 이러한 개발론을 프론트엔드에 대한 백엔드 패턴(backend for frontend)이라고 한다.\
즉 백엔드 팀을 구성할 때 개별적으로 관리해야 하는 UI의 종류를 먼저 산출하고 그에 맞추어 백엔드 팀을 구성하는 전략을 뜻한다. 만일 데스크탑용 페이지와 태블릿용 페이지와 휴대폰용 페이지가 완전히 달라야 한다면 백엔드 팀은 3개로 구성될 것이다\
이 패턴을 구현할 때는 서비스 간에 코드가 중복될 가능성이 높다는 문제점이 있다
하지만 반응형으로 개발하는 웹페이지에는 적용할 수 없는 패턴으로 보여진다\
이 패턴은 마이크로서비스 컨설턴트인 샘 뉴맨(Sam Newman)이 처음으로 고안했다

상세는 https://docs.microsoft.com/ko-kr/azure/architecture/patterns/backends-for-frontends 를 참조하시오

#### Q. 레이아웃 트리가 무엇인가?

A. 레이아웃 트리의 목적은 레이아웃(리플로우)을 수행하고 페인트칠 및 히트 테스트를 위해 결과를 저장하는 것입니다. 

레이아웃은 페이지에서 노드 크기를 조정하고 위치를 지정하는 프로세스입니다. 

블링크 엔진에서 레이아웃은 항상  relayout boundary에서 시작합니다 

올바른 배치를 위해 외곽 배치 경계까지 조상을 표시해야 합니다.

출처 : https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction?hl=ko

#### Q. Web Browser의 프로세싱 중에서 리플로우 (Reflow)라는게 있던데 이게 무엇인가?

A. 리플로우는 다시 흐르다는 뜻인데 이것만으로는 의미를 이해하기 어렵다\
리플로우는 레이아웃을 재설정한다는 뜻으로 이해하는것이 더 직관적이다

#### Q. TCP/IP offload engine (TOE)이 무엇인가?

A. 운영 체계(OS) 내부에서 소프트웨어로 수행되는 TCP/IP 프로토콜 스택을 별도의 전용 하드웨어로 구현한 시스템과 분리된 하드웨어 프로토콜 스택. 즉 랜카드 같은 하드웨어에 독립적으로 구현되어 있다


#### Q. 어떻게 하면 유저가 원하는 정보를 빠르게 렌더링할 수 있을까 ?

주로 두가지 지표가 사용된다
1. first-meaningful-paint (FMP, 가장 의미있는 정보)가 뿌려지는 시간
1. largest-contentful-paint (LCP, 웹페이지에서 가장 큰 컨텐츠)가 뿌려지는 시간\
크롬 웹 바이탈에서 사용하는 지표는 LCP 이지만 상황에 따라서는 FMP가 더 중요하게 작용할 때도 있다


---
