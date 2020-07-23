# NestJS
Nestjs tutorial.. For Korean students 
2020.07.23 ~

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

 간단한 텍스트 요청을 controller에 전달. 
 
 핵심 Inject dependencies : 여러 relationship들을 만든다.
 
#### Module

 application 내 모듈. Application structure를 만들기 위한 metadata를 가지고 있음
 
#### Main

 application 엔트리 파일
 
 
## Import

import { _Decorator } from '@nestjs/common';


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

@Post(), @Put(), @Delete() ..
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

## Providers
```
nest g service cats
```

### Services

데이터 저장, 회수. Contorller로 사용됨
@Injectable() decorator 사용 & interface

Interface 선언
```
export interface X{
  variable : type;
  ...
}
```
Interface 사용
```
import {X} from './interfaces/X.interface'
```
---

## Modules

import, expor를 통해 Metadata를 지정함
터미널에 nest 명령어를 통해 추가하면 자동으로 파일이 변경됨 -> 건들 필요 없음

---
## Middleware

Client    ->   Middleware  -> RouteHandler
 side   

Request & response 함수에 access.

EX) logger
```
import { Injectable, NestMiddleware } from '@nestjs/common';
import { Request, Response } from 'express';

@Injectable()
export class LoggerMiddleware implements NestMiddleware {
  use(req: Request, res: Response, next: Function) {
    console.log('Request...');
    next();
  }
}

```

---

## Exception filters

---

# Techniques

## Authentication

### Passport library

JWT strategy를 이용하여 인증을 진행
Vanilla Passport

#### Download
```
npm install --save @nestjs/passport passport passport-local
npm install --save-dev @types/passport-local
```








---
