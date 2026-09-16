# Diagnóstico de Sostenibilidad NTC 6496 y NTC 6503

Aplicación web para realizar diagnósticos de sostenibilidad en establecimientos gastronómicos (NTC 6496) y establecimientos de alojamiento y hospedaje (NTC 6503).

## Componentes

- Frontend en React, TypeScript y Vite.
- Backend REST en Node.js y Express.
- Persistencia en MySQL.
- Asistencia contextual con Gemini (opcional).
- Generación de informes PDF y planes de acción.

## Desarrollo local

Requisitos: Node.js 18 o superior y MySQL.

```bash
npm install
npm run dev
```

La aplicación usa automáticamente el modo `sustainable` definido en `vite.config.ts`.

Para el backend:

```bash
cd backend
npm install
copy environment.example .env
npm start
```

Antes de iniciar el backend, cree la base de datos y ejecute `backend/migrations/001_schema.sql`. Complete las credenciales de MySQL en `backend/.env`; este archivo no debe subirse a GitHub.

## Compilación

```bash
npm run build
```

## Documentación

- [`MANUAL_DE_USO_SOSTENIBILIDAD.html`](MANUAL_DE_USO_SOSTENIBILIDAD.html): manual visual y operativo específico para NTC 6496/6503.
- `MANUAL_NTC_6496_6503.md`: manual normativo.
- `backend/README.md`: configuración de la API y la base de datos.

## Seguridad

No incluya claves Gemini, contraseñas de MySQL ni archivos `.env` privados en el repositorio. Use un archivo `.env.local` no versionado para el frontend y `backend/environment.example` como plantilla.
