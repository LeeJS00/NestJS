# NestJS
Nestjs tutorial.. For study 2020.07.23

---
## Download
```
npm i -g @nestjs/cli
```

## Start
```
nest new nest-next-typescript
```

### Directory
```
src
  - app.controller.ts
  - app.service.ts
  - app.module.ts
  - main.ts
 ```
#### Controller
 
 Requests, responses 들을 처리함
 classes & decorators 사용
 
#### Service

 간단한 텍스트 요청을 controller에 전달
 
#### Module

 application 내 모듈
 
#### Main

 application 엔트리 파일
 
---

## Controllers
```
nest g controller XXX
```
### Decorators

Format : @X() 
@Controller() 을 사용해서 controller써의 기능을 할 수 있게함

### Routing

@Get() 
Nest 가 http requests의 handler를 만들게함
findAll() 안에 여러것들을 넣어 기능을 다르게함

@Post, @Put(), @Delete ..
```
@Controller('cats')
export class CatsController {
  @Get()
  findAll(): string {
    return 'This action returns all cats';
  }
}
```

#### Redirection
```
@Get()
@Redirect('https:// ....',301)
```




---
