# Rastreo GPS de técnicos

Panel web para ver en tiempo real la ubicación de los técnicos, sus recorridos, visitas a clientes (geocercas) y exportar reportes a Excel.

- **Panel (supervisores):** `index.html`, con ingreso por usuario o correo y contraseña.
- **Página del técnico:** `t.html#CODIGO`. El técnico pulsa *Iniciar jornada* y comparte su ubicación.
- **Base de datos y tiempo real:** Supabase.

La clave de `config.js` es la clave *publishable* de Supabase, pública por diseño. Los datos están protegidos por permisos (RLS): solo los usuarios de la tabla `supervisores` pueden verlos.

## Agregar un supervisor
1. Supabase → Authentication → Users → *Add user* (usuario@rastreo.app o un correo, y contraseña).
2. Supabase → SQL Editor: `insert into supervisores values ('usuario@rastreo.app');`
