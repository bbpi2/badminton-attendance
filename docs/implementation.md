## Implementation Plan

1. **Repo Setup**
   - Create `/frontend` and `/backend` folders.
   - Add README and version control.

2. **Backend**
   - Use Go (Gin) or Kotlin (Ktor)
   - Create models and API endpoints for:
     - Sessions
     - Attendance
     - Admin updates
   - Connect SQLite and apply migrations.
   - Gate `/admin` routes with a shared password check.

3. **Frontend**
   - Build with React.
   - Pages:
     - `/attendance`: checkbox calendar + +1s input
     - `/admin`: editable dashboard
   - Style with Tailwind CSS or plain CSS.
   - Use `fetch()` to talk to backend.

4. **Cost Handling**
   - Backend computes per-person cost using venue rate × court count ÷ actual attendees.

5. **Deployment**
   - Backend to Render/Railway.
   - Frontend to Vercel or Netlify.
