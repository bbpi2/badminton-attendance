## Architecture Overview

**Frontend**: React SPA  
**Backend**: Golang (Gin/Fiber) or Kotlin (Ktor)  
**Database**: SQLite  
**Auth**: Shared password for admin  
**Deploy**: Render, Railway, or Fly.io

```text
Player --> Frontend --> Backend --> DB  
Admin  --> Frontend --> Backend --> DB
```
