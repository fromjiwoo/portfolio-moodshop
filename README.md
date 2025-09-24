# 🛒 Mood Shop

- **개발기간** : ﻿2025.06.10 ~ 2025.06.30 (총 23일) 
- **참여인원** : 5명  
- **담당업무** : 제안, 기획, 회원 관리 페이지 구현, 젠체적인 웹페이지 디자인인
- **개발환경** : Tomcat 8.5, Oracle DB, Eclipse
- **사용도구** : ﻿draw.io, Pencil, dbdiagram.io
- **사용기술** : Spring Web, JSP, MyBatis, Java, JavaScript, SQL, MVC, API

---

## 📖 개요
&nbsp;&nbsp;본 프로젝트는 감정을 단순히 텍스트나 데이터로 표현하는 데 그치지 않고, 디자인을 통해 시각화하여 사용자가 직관적으로 느낄 수 있도록 하는 데에 초점을 두었습니다. 이를 기반으로 자신의 감정을 기록하고 공유하거나, 다른 사람에게 선물할 수 있는 **감성 기반 쇼핑 플랫폼**을 구현하는 것을 목표로 하였습니다.  
&nbsp;&nbsp;즉, 개인의 감정을 하나의 경험으로 전환하고, 이를 사회적으로 소통 가능한 가치로 확장시켜 나감으로써 감정과 소비를 연결하는 새로운 형태의 서비스를 제안하는 프로젝트입니다.

---

## 💡 기획 의도(동기)
&nbsp;&nbsp;현대 사회에서 소비는 단순한 물건 구매를 넘어, **개인의 감정과 경험을 표현하는 수단**으로 자리 잡고 있습니다. 하지만 기존의 쇼핑 플랫폼은 가격·기능·브랜드 중심으로만 설계되어, 사용자의 감정적 가치를 충분히 반영하지 못하고 있습니다.  
&nbsp;&nbsp;이에 본 프로젝트는 감정을 **디자인적으로 시각화**하고, 이를 다른 사람과 **공유하거나 선물할 수 있는 기능**을 제공함으로써 감정과 소비를 연결하는 새로운 방식을 제안합니다. 사용자는 자신의 감정을 기반으로 쇼핑을 경험하고, 나아가 감정 자체를 교환 가능한 가치로 전환할 수 있습니다.  
&nbsp;&nbsp;즉, 단순한 거래 중심의 플랫폼을 넘어, **감성을 매개로 한 소통과 경험 중심의 서비스**를 구현하는 것이 이 프로젝트의 핵심 동기입니다.


---

## 🎯 목표 및 설계
### 목표
- 다양한 **감정을 테마로 한 마스코드 관련 굿즈** 쇼핑몰 구현
- 장바구니 담기, 찜 / 로그인, 회원가입, 댓글 대댓글 구현
- 관리자 페이지 -> 상품 등록, 수정, 삭제 / 회원 관리, 수정, 삭제 구현  
- 사용자들의 사용량 증가 유도  

### 📊 ERD & 테이블 설계
ERD 이미지 첨부 (https://drive.google.com/file/d/1k9GaeLMlN2osdp51_JrL5P1w0A_D_Zgj/view?usp=drive_link)

<details>
<summary>📷 ERD 이미지 더보기</summary>
  
<img width="971" height="584" alt="스크린샷 2025-09-23 122917" src="https://github.com/user-attachments/assets/b8bf6c30-4157-4942-88f2-1392fa69e55a" />


</details>

#### 주요 테이블
- **사용자/인증** : USER_TBL, QUESTION, ANSWER
- **리뷰** : REVIEW, REVIEW_SUB
- **주문/결제** : ORDER_TBL, ORDER_DETAIL
- **장바구니** : BASKET, BASKET_DETAIL
- **상품/옵션** : PRODUCT, PRODUCT_OPTION, RECENT_VIEW_TBL, WISHLIST
- **회사/관리자** : COMPANY, MANAGER
- **이벤트/공지사항** : EVENT_TBL, NOTICE_TBL


---

### 🛠️ 담당 역할
#### 1. 메인 페이지 제작
- 메인 배너 및 핵심 기능 영역 UI/UX 설계
- 반응형 디자인 적용으로 다양한 디바이스 대응
- 직관적인 네비게이션 구성으로 사용자 편의성 강화

#### 2. 상품 상세 페이지 구현
- 상품 이미지, 설명, 옵션 선택 UI 제작
- 리뷰/평점 기능과 연동하여 상세 정보 제공
- 장바구니/구매/찜하기/수량 선택 버튼 등 사용자 행동 유도 요소 디자인

#### 3. 전체 웹 디자인 총괄
- 서비스 전반의 디자인 컨셉 수립 및 통일성 유지
- 컬러, 폰트, 아이콘 등 공통 UI 가이드라인 제작
- powerpoint를 활용하여 팀원 간 협업 효율 극대화

#### 4. 관리자 페이지 - 회원 관리 기능
- 관리자 전용 회원 목록/검색/상세 페이지 구현
- 회원 상태(수정/삭제) 관리 기능 개발
- 직관적이고 간단한 UI 구성으로 관리자 편의성 향상

#### 5. 오프라인 매장 지도
- 카카오지도 API 연동
- 지역별 오프라인 매장 위치 표시
- 매장 클릭 시 상세 정보 팝업 제공

---

<details>
<summary>📷 화면 구성(클릭해서 보기) </summary>


|구분 | 화면 | 미리보기 |
|----------|----------|----------|
|공통| 메인화면 | <img width="812" height="685" alt="image" src="https://github.com/user-attachments/assets/630bea67-783b-45d5-b280-cb297cb8f702" /> |
|공통| 회원가입 | <img width="1055" height="469" alt="image" src="https://github.com/user-attachments/assets/ca7a269c-8c34-46e5-8b1a-37b4510e27da" /> |
|공통| 로그인 | <img width="894" height="475" alt="image" src="https://github.com/user-attachments/assets/d326e3bf-d1d8-4ae5-be2b-a344821813f5" /> |
|공통| 상품상세페이지 | <img width="879" height="473" alt="image" src="https://github.com/user-attachments/assets/9323d57e-86be-4fac-b7e5-bee0d5420e2b" /> |
|유저| 이벤트 페이지 | <img width="794" height="464" alt="image" src="https://github.com/user-attachments/assets/fd8b940e-22f6-43a9-be60-60adf835e0c6" /> |
|유조| 오프라인 매장 찾기| <img width="702" height="390" alt="image" src="https://github.com/user-attachments/assets/12b42aeb-4ba9-4d13-aaf2-13fed4dd161d" /> |
|유저| 결제하기| <img width="400" height="453" alt="image" src="https://github.com/user-attachments/assets/b7988708-66fe-44c4-ba80-412fc615cac7" /> |
|유저| 결제 완료 페이지 | <img width="732" height="571" alt="image" src="https://github.com/user-attachments/assets/23a79f9d-794f-444d-b639-5d355cfc547b" /> |
|유저| 마이페이지 | <img width="694" height="343" alt="image" src="https://github.com/user-attachments/assets/c94a4de6-27bf-4321-badc-74b4a821923d" /> |
|유저| 주문내역 페이지 | <img width="718" height="399" alt="image" src="https://github.com/user-attachments/assets/3f1d40f0-4ad2-4b29-aae8-9aa42f6f675a" /> |
|유저| 리뷰작성 페이지 | <img width="501" height="389" alt="image" src="https://github.com/user-attachments/assets/ad0b8d34-2245-4e13-bf17-b9099e331890" /> |
|유저| 장바구니 | <img width="800" height="445" alt="image" src="https://github.com/user-attachments/assets/f38b1634-147e-4278-931b-bd874381a803" /> |
|유저| 찜목록 | <img width="692" height="374" alt="image" src="https://github.com/user-attachments/assets/38e60909-999c-4d15-84ad-7aca6211d98b" /> |
|관리자| 회원통계 | <img width="389" height="429" alt="image" src="https://github.com/user-attachments/assets/83573a38-e9b3-44d3-bfe0-c354b876de6c" /> |
|관리자| 상품관리 | <img width="636" height="339" alt="image src="https://github.com/user-attachments/assets/dd631d9a-f890-4548-bf0c-e34c19411e9f" /> |
|관리자| 회원관리 | <img width="1294" height="552" alt="image" src="https://github.com/user-attachments/assets/67f429af-97c9-4eb2-9b3e-a63bd057488c" /> |

</details>

---

### 🏆 성과 및 후기 
- **메인 페이지 및 상품 상세 페이지 구현**  
  - 핵심 기능을 직관적으로 배치하여 사용자 경험(UX) 개선
  -  반응형 UI 설계를 통해 다양한 기기에서 일관된 서비스 제공  

- **웹 전체 디자인 총괄**  
  - 서비스 전반의 디자인 가이드라인(Figma 기반) 수립  
  - 통일성 있는 UI/UX 제공으로 프로젝트 완성도 향상  

- **관리자 페이지 - 회원 관리 기능 개발**  
  - 관리자 전용 회원 목록/검색/상세 페이지 구현  
  - 직관적이고 간결한 UI 설계로 관리 효율성 증대  

- **카카오지도 API 연동**  
  - 오프라인 매장 위치를 지도 기반으로 시각화  
  - 매장 클릭 시 상세 정보 팝업 제공으로 사용자 접근성 강화  

<details>
<summary> 후기 더보기 </summary>


## ✨ 후기

- **메인 페이지와 상품 상세 페이지 구현 경험**  
  단순히 화면을 구성하는 수준을 넘어, 사용자가 서비스를 처음 접했을 때 가장 직관적으로 이해할 수 있는 구조를 설계하는 것이 중요하다는 점을 깨달았습니다.
  메인 페이지에서는 핵심 기능을 전면에 배치하고, 상세 페이지에서는 정보 전달과 행동 유도를 균형 있게 고려하며 **UX 중심의 개발**을 실습할 수 있었습니다.  

- **웹 전체 디자인 총괄 경험**  
  프로젝트 전체의 톤앤매너를 통일시키는 과정에서 디자인 가이드라인의 중요성을 깊이 느꼈습니다. 색상, 폰트, 아이콘, 버튼 스타일 등을 통일하면서 팀원들이 각자 개발한 페이지를 하나의 서비스처럼 자연스럽게 연결할 수 있었고, 협업 속에서 디자인 리더십을 발휘할 수 있었습니다. 이를 통해 **일관성 있는 UI/UX가 서비스 완성도를 좌우한다**는 점을 배웠습니다.  

- **관리자 페이지 - 회원 관리 기능 개발**  
  관리자 기능은 일반 사용자와 달리 효율성과 직관성이 최우선이라는 점을 실감했습니다. 회원 검색, 상태 관리 등의 기능을 단순하면서도 강력하게 구현하면서 **사용자 그룹에 따라 요구되는 UX가 다르다는 점**을 배우게 되었습니다.  

- **카카오지도 API 연동 경험**  
  오프라인 매장을 지도 기반으로 시각화하는 과정에서 API 문서를 분석하고 원하는 기능을 최적화하는 과정을 거쳤습니다. 단순히 API를 연동하는 것이 끝이 아니라, 매장 상세 정보 팝업, 위치 마커 디자인 등 사용자 친화적으로 가공하는 것이 더 큰 가치라는 점을 깨달았습니다. 이를 통해 **외부 API를 서비스에 녹여내는 역량**을 키울 수 있었습니다.  

- **종합적인 배움**  
  이번 프로젝트를 통해 단순히 기능을 구현하는 것을 넘어, 서비스의 완성도를 높이는 데 필요한 **UX/UI 설계, API 최적화, 협업 디자인 가이드라인 수립** 같은 실무적인 역량을 쌓을 수 있었습니다. 특히, 초기 설계 단계에서 정책과 흐름을 명확히 잡아두는 것이 프로젝트 진행 속도와 품질에 직접적으로 연결된다는 점을 다시 한번 느끼게 되었습니다.  


</details>

---

### 🎥 시연 자료
- [📺 시연 영상 보기](https://drive.google.com/file/d/11aenAGHOXNpnOKYRPGKA2tLjNuQfC7b2/view?usp=drive_link)
- [📑 발표 자료 (PPT)](https://drive.google.com/file/d/1fp_ESbaVc9Ueg8G1MSAh-5vwLG-0K0ko/view?usp=drive_link)
- [📑 발표 자료 (pdf)](https://drive.google.com/file/d/1yLiWeerdpWLjofwh7jmJYIND-UUIviMq/view?usp=drive_link)
- [📑 UML](https://drive.google.com/file/d/1eTnMEkVAo3sjbwMe9hfZk0VudriDB37-/view?usp=drive_link)
