포트폴리오
===================

EzFramework - Bukkit 플러그인 프레임워크
---
[![Download](https://api.bintray.com/packages/kingcjy/ezframework/ezframework-core/images/download.svg) ](https://bintray.com/kingcjy/ezframework/ezframework-core/_latestVersion)
[![Maven Central](https://img.shields.io/maven-central/v/io.github.kingcjy/ezframework-core.svg?label=Maven%20Central)](https://search.maven.org/search?q=g:%22io.github.kingcjy%22%20AND%20a:%22ezframework-core%22)
[![Build Status](https://travis-ci.org/KingCjy/ezframework.svg?branch=master)](https://travis-ci.org/KingCjy/ezframework)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

마인프래프트 Bukkit 위에서 돌아가는 플러그인을 개발하기위한 오픈소스 프레임워크입니다.

마인크래프트내에 커맨드, 이벤트를 쉽게 등록할 수 있습니다.

소스코드 및 사용법은 [>> 이곳 <<](https://github.com/KingCjy/ezframework) 에서 확인해주세요

web-server-framework - 자바 웹 서버 프레임워크
---
    
스프링 클론코딩 3번째 버전입니다.

객체지향 프로그래밍, 디자인패턴, 스프링 프레임워크 내부 구조 공부를 위해 진행중인 프로젝트입니다.

소스코드는 [>> 이곳 <<](https://github.com/KingCjy/web-server-framework/tree/v3) 에서 확인해주세요

    * 소속 : 개인
    * 역할 : 프로젝트 개발
    * 사용 기술
        - Java
        - Tomcat
        - Jpa
        - hibernate
    * TODOS
        - Jpa Repository AutoConfiguration
        - Repository interface Proxy
        - Transactional Annotation
        - Query Annotation
        - AOP
실제 사용 샘플 코드       
```Java
@RestController
@RequestMapping("/api")
public class BoardController {

    @Autowired
    private BoardService boardService;

    @RequestMapping("/boards")
    public ResponseEntity<List<BoardDto.BoardResponseDto>> findAllBoards() {
        List<BoardDto.BoardResponseDto> dtoList = boardService.findAllBoards();
        return new ResponseEntity<>(dtoList, HttpStatus.OK);
    }

    @RequestMapping(value = "/boards/{id}", method = RequestMethod.GET)
    public ResponseEntity<?> findBoardById(@PathVariable(name = "id") Long id) {
        BoardDto.BoardResponseDto dto = boardService.findBoardById(id);
        return new ResponseEntity<>(dto, HttpStatus.OK);
    }

    @RequestMapping(value = "/boards", method = RequestMethod.POST)
    public ResponseEntity<?> addBoard(@RequestBody BoardDto.BoardRequestDto dto) {
        boardService.addBoard(dto);
        return new ResponseEntity<>(HttpStatus.OK);
    }

    @RequestMapping(value = "/boards/{id}", method = RequestMethod.PATCH)
    public ResponseEntity<?> updateBoardById(@PathVariable(name = "id", required = true) Long id,
                                            @RequestBody BoardDto.BoardRequestDto dto) {
        boardService.updateBoard(id, dto);
        return new ResponseEntity<>(HttpStatus.OK);
    }

    @RequestMapping(value = "/boards/{id}", method = RequestMethod.DELETE)
    public ResponseEntity<?> deleteBoardById(@PathVariable(name = "id") Long id) {
        boardService.deleteBoard(id);
        return new ResponseEntity<>(HttpStatus.OK);
    }
}
```
---

Airpick - 여행특가 서비스
---
항공, 호텔 액티비티 알림 서비스

    * 소속 : 지니웍스
    * 역할 : 백엔드 서버 개발 및 인프라 구성
    * 사용 기술
        - Spring Boot 2
        - Spring Data Jpa
        - Spring REST Docs
        - Mysql
        - GitLab, GitLab CI
        - Firebase
    * 업무 내용
        - REST API 개발
        - REST API 문서 자동화(Spring REST Docs)
        - 테스트 & 배포 자동화(AWS CodePipeline + GitLab)

        
<img src="https://github.com/KingCjy/resume/blob/master/images/airpick.PNG?raw=true" class="T75of lxGQyd" aria-hidden="true" height="310" alt="스크린샷 이미지" itemprop="image">

 ---
 
People - 피플 인사,부고 알리미
---
주변인물 인사, 부고 알림 서비스
    
    * 소속 : 개인
    * 역할 : 웹 서버 및 관리자페이지 개발
    * 사용 기술
        - Spring Boot 2
        - Spring Data Jpa
        - Spring REST Docs
        - Mysql
        - JSP
        - Firebase
    * 업무 내용
        - 인사, 부고 등록 페이지 개발
        - Android, IOS 앱에 필요한 REST API 개발
        - Android, IOS 푸시 개발(Firebase Admin SDK)
        - REST API 문서 자동화(Spring REST Docs)
        
<img src="https://github.com/KingCjy/resume/blob/master/images/people.png?raw=true" class="T75of lxGQyd" aria-hidden="true" height="310" alt="스크린샷 이미지" itemprop="image">

 ---
 
픽앤유니크 - pick&uniq
---
커머스 쇼핑몰
    
    * 소속 : 지니웍스
    * 역할 : 웹 서버 개발 및 유지보수
    * 사용 기술 
        - Spring Boot
        - Spring Security
        - Spring Batch
        - Mysql
        - MyBatis
        - Redis
        - AWS
    * 업무 내용
        - 쇼핑몰 정산 시스템 신규 개발
        - Android 및 IOS 앱의 런칭에 필요한 REST API 개발
        - 간편 로그인 개발(Kakao, Facebook, Naver, Payco)
        - 쇼핑몰 결제 수단 추가(Payco)
        - Cafe24 및 MakeShop 과의 상품 연동 유지보수
        - Samsungpay연동 API 개발 및 유지보수
        
<img src="https://github.com/KingCjy/resume/blob/master/images/picknuniq.png?raw=true" class="T75of lxGQyd" aria-hidden="true" height="310" alt="스크린샷 이미지" itemprop="image">

 ---
 
Admerce - 애드머스
---
게임기반 마켓팅 솔루션
    
    * 소속 : 지니웍스
    * 역할 : 게임서비스 관리페이지 개발
    * 사용 기술
        - Spring Boot
        - MyBatis
        - React
        - Redux
        - Redux-Saga
    * 업무 내용
        - 게임서비스 관리페이지 Frontend(React) 및 Backend(Spring boot) 개발

 ---
 
 
ParkingOn - 파킹온
---
통합형 자동차 서비스 앱

프리미엄 방문세차,광택,대리운전,자동차 검사대행,카딜리버리

    
    * 소속 : 지니웍스
    * 역할 : 기존 기능 PHP -> Java 마이그레이션 및 신규 기능 개발
    * 사용 기술
        - CodeIgniter
        - Spring Boot
        - AngularJS
        - Firebase
    * 업무 내용
        - 기존 PHP로 작성된 코드를 Java로 마이그레이션
        - 대리운전 배차, 요금계산 API 유지보수

<img src="https://github.com/KingCjy/resume/blob/master/images/parkingon.png?raw=true" class="T75of lxGQyd" aria-hidden="true" height="310" alt="스크린샷 이미지" itemprop="image">
