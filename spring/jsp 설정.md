# spring jsp 설정

## 1. 의존성 추가

### build.gradle
```
implementation 'org.apache.tomcat.embed:tomcat-embed-jasper'
```

## 2. jsp 설정 추가 
### application.yml 변경 (views 폴더명 변경 가능)
```
spring:
  mvc:
    view:
      prefix: /WEB-INF/views/
      suffix: .jsp
```

## 3. Controller 생성 
### JspController.java 생성 
```
@Controller
public class JspController {
    @GetMapping("/index")
    public String getIndex(){
        return "index";
    }
}
```

## 4. jsp 파일 생성 
### 생성 경로 : src/main/webapp/WEB-INF/views/index.jsp 
```

<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    </head>
    <body>
        <div>JSP</div>
    </body>
</html>
```

## 5. 확인 
### 브라우저에서 localhost:8080/index 접속후 페이지 확인 

