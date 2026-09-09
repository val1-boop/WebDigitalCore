# Sistema de Gestión de Recursos Universitarios

Panel web para administrar la reservación de espacios y equipo dentro de una institución educativa, con control de accesos por rol y bitácora de auditoría.

## Qué hace

- **Autenticación** — inicio de sesión, recuperación de contraseña y rutas protegidas por sesión
- **Usuarios** — alta, edición y listado de usuarios del sistema
- **Recursos** — catálogo de espacios y equipo disponible
- **Solicitudes** — registro de nuevas solicitudes e historial por usuario
- **Reservaciones** — asignación de recursos en fechas y horarios
- **Auditoría** — historial de acciones realizadas en el sistema

## Estructura

```
src/
├── pages/
│   ├── auth/          # Login, ForgotPassword
│   ├── users/         # UserList, UserForm
│   ├── resources/     # Spaces, Equipment
│   ├── requests/      # NewRequest, RequestHistory
│   ├── reservations/  # Reservations
│   └── audit/         # AuditHistory
├── services/          # Cliente HTTP y servicios por dominio (api, auth, requests)
├── context/           # AuthContext: sesión global
├── hooks/             # useAuth
├── layout/            # DashboardLayout
└── routes/            # AppRoutes
```

La lógica de red está aislada en `services/`, de modo que las pantallas no hacen peticiones directamente.

## Tecnologías

React · Vite · React Router · Context API · ESLint

## Cómo ejecutarlo

```bash
npm install
npm run dev
```

La aplicación queda disponible en `http://localhost:5173`.
