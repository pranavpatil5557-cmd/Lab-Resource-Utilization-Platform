# Render deployment files

Copy these files into the root of the combined GitHub repository:

- `render.yaml` -> repository root
- `backend/Dockerfile` -> backend folder
- `frontend/src/services/api.js` -> replace the existing file
- `backend/src/main/java/com/labresource/config/SecurityConfig.java` -> replace the existing file

Important:
- This Blueprint intentionally does NOT create a new Postgres database because you already created `lab-resource-utilization-postgresql` on Render.
- `render.yaml` references that existing database by name.
- Render will ask you for `MAIL_USERNAME` and `MAIL_PASSWORD` during the first Blueprint setup.
- Do not commit real email credentials to GitHub.
- The frontend gets the backend's public Render URL through `VITE_API_URL`.
- The backend gets the frontend's public Render URL through `FRONTEND_URL`.
