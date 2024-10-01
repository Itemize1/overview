## Project Architecture 🏗️

Here is the folder structure for our project:

```
src
├── /auth
│   ├── /dto
│   │   ├── login.dto.ts
│   │   ├── register.dto.ts
│   ├── /guards
│   │   └── jwt.guard.ts
│   ├── /strategies
│   │   ├── jwt.strategy.ts
│   │   └── local.strategy.ts
│   ├── auth.controller.ts
│   ├── auth.service.ts
│   └── auth.module.ts
│
├── /users
│   ├── /dto
│   │   ├── create-user.dto.ts
│   │   ├── create-user-response.dto.ts
│   │   ├── update-user.dto.ts
│   │   ├── delete-user.dto.ts
│   ├── /controllers
│   │   ├── create-user.controller.ts
│   │   ├── update-user.controller.ts
│   │   └── delete-user.controller.ts
│   ├── /services
│   │   ├── create-user.service.ts
│   │   ├── update-user.service.ts
│   │   └── delete-user.service.ts
│   ├── users.module.ts
│
├── /inventory
│   ├── /dto
│   │   ├── create-item.dto.ts
│   │   ├── create-item-response.dto.ts
│   │   └── update-item.dto.ts
│   ├── /entities
│   │   └── item.entity.ts
│   ├── inventory.controller.ts
│   ├── inventory.service.ts
│   └── inventory.module.ts
│
├── /lost-found
│   ├── /dto
│   │   ├── report-lost-item.dto.ts
│   │   ├── claim-found-item.dto.ts
│   ├── /entities
│   │   └── lost-item.entity.ts
│   ├── lost-found.controller.ts
│   ├── lost-found.service.ts
│   └── lost-found.module.ts
│
├── /reports
│   ├── /dto
│   │   ├── create-report.dto.ts
│   │   ├── update-report.dto.ts
│   ├── reports.controller.ts
│   ├── reports.service.ts
│   └── reports.module.ts
│
├── /notifications
│   ├── /dto
│   │   ├── notification-payload.dto.ts
│   ├── notifications.controller.ts
│   ├── notifications.service.ts
│   └── notifications.module.ts
│
├── /database
│   ├── /migrations
│   │   └── create-users-table.ts
│   ├── /entities
│   │   ├── user.entity.ts
│   │   ├── item.entity.ts
│   │   └── report.entity.ts
│   └── database.module.ts
│
├── /common
│   ├── /decorators
│   │   └── roles.decorator.ts
│   ├── /filters
│   │   └── http-exception.filter.ts
│   ├── /pipes
│   │   └── validation.pipe.ts
│   ├── /interceptors
│   │   └── logging.interceptor.ts
│   └── /interfaces
│       └── user.interface.ts
│
├── app.module.ts
├── main.ts
└── /config
    ├── config.module.ts
    └── /environments
        ├── development.env
        └── production.env
```
