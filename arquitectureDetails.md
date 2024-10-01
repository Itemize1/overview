# Arquitecture Details
# Project Architecture

## /src
- [/auth](#auth)
- [/users](#users)
- [/inventory](#inventory)
- [/lost-found](#lost-found)
- [/reports](#reports)
- [/notifications](#notifications)
- [/database](#database)
- [/common](#common)
- [/config](#config)

## <a name="auth"></a> /auth
Handles authentication and authorization.
- **/dto**: Defines `login.dto.ts` and `register.dto.ts` for login and registration.
- **/guards**: Contains `jwt.guard.ts` for route protection.
- **/strategies**: Defines authentication strategies like `jwt.strategy.ts` and `local.strategy.ts`.
- **auth.controller.ts**: Handles authentication routes.
- **auth.service.ts**: Manages authentication logic like generating JWT tokens.
- **auth.module.ts**: Organizes authentication logic.

## <a name="users"></a> /users
Handles user management.
- **/dto**: Defines DTOs like `create-user.dto.ts` and `create-user-response.dto.ts` for user operations.
- **/controllers**: `create-user.controller.ts`, `update-user.controller.ts` for handling user operations.
- **/services**: Contains business logic for user operations such as `create-user.service.ts` and `update-user.service.ts`.
- **users.module.ts**: Module managing all user-related logic.

## <a name="inventory"></a> /inventory
Manages inventory of items.
- **/dto**: Defines DTOs like `create-item.dto.ts` and `create-item-response.dto.ts`.
- **/entities**: Defines `item.entity.ts` for inventory items in the database.
- **inventory.controller.ts**: Routes for managing inventory.
- **inventory.service.ts**: Handles inventory logic.
- **inventory.module.ts**: Module managing the inventory system.

## <a name="lost-found"></a> /lost-found
Handles the lost and found functionality.
- **/dto**: Contains DTOs such as `report-lost-item.dto.ts` and `claim-found-item.dto.ts`.
- **/entities**: Defines `lost-item.entity.ts` for database representation.
- **lost-found.controller.ts**: Routes for reporting and claiming lost items.
- **lost-found.service.ts**: Business logic for lost and found items.
- **lost-found.module.ts**: Module that organizes lost and found logic.

## <a name="reports"></a> /reports
Manages report generation and tracking.
- **/dto**: Contains DTOs like `create-report.dto.ts` and `update-report.dto.ts`.
- **reports.controller.ts**: Routes for generating and viewing reports.
- **reports.service.ts**: Handles the logic for report management.
- **reports.module.ts**: Module for handling reports.

## <a name="notifications"></a> /notifications
Manages notifications and alerts.
- **/dto**: Defines `notification-payload.dto.ts` for notification data structure.
- **notifications.controller.ts**: Routes for handling notifications.
- **notifications.service.ts**: Logic for sending notifications (e.g., email).
- **notifications.module.ts**: Module managing notifications.

## <a name="database"></a> /database
Handles database connections and migrations.
- **/migrations**: Contains migration files like `create-users-table.ts`.
- **/entities**: Defines shared entities like `user.entity.ts`, `item.entity.ts`, and `report.entity.ts`.
- **database.module.ts**: Global module that manages the database connection.

## <a name="common"></a> /common
Contains shared utilities and services.
- **/decorators**: Defines custom decorators like `roles.decorator.ts`.
- **/filters**: Contains global exception filters like `http-exception.filter.ts`.
- **/pipes**: Pipes for validation, such as `validation.pipe.ts`.
- **/interceptors**: Defines interceptors like `logging.interceptor.ts`.
- **/interfaces**: Shared interfaces like `user.interface.ts`.

## <a name="config"></a> /config
Handles application configuration.
- **config.module.ts**: Module for loading and managing configurations.
- **/environments**: Contains environment-specific configuration files (`development.env`, `production.env`).
