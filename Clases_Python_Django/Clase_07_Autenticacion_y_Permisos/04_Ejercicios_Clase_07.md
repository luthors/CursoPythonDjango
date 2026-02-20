# 🧩 Clase 07 · Repertorio Amplio de Ejercicios

[⬅️ Volver a la clase](Clase_07_Autenticacion_y_Permisos.md) | [📦 Módulo](README.md) |
[🗺️ Mapa modular](../MAPA_MODULAR_COMPLETO.md) | [🏠 Índice general](../README.md)

## 🟢 Nivel Básico (1–15)

1. Configurar rutas de login/logout.
2. Crear template de login.
3. Implementar `login_view` con `AuthenticationForm`.
4. Implementar `logout_view`.
5. Configurar `LOGIN_URL` en `settings.py`.
6. Proteger una vista con `@login_required`.
7. Verificar redirección de usuario anónimo.
8. Crear template de registro.
9. Implementar `register_view`.
10. Iniciar sesión automática tras registro.
11. Mostrar usuario autenticado en navbar.
12. Mostrar botón logout solo si está logueado.
13. Mostrar links login/registro si está anónimo.
14. Añadir mensaje de error en login inválido.
15. Añadir mensaje de éxito en login exitoso.

## 🟡 Nivel Intermedio (16–30)

1. Restringir creación de productos a autenticados.
2. Asignar `creado_por = request.user` al crear producto.
3. Restringir edición al usuario creador.
4. Restringir eliminación al usuario creador.
5. Mostrar mensaje de permiso denegado.
6. Evitar mostrar botones editar/eliminar a no propietarios.
7. Crear grupo `editores` y asignar permisos básicos.
8. Restringir acceso por grupo en una vista.
9. Permitir solo staff en una sección admin custom.
10. Registrar intentos fallidos de login (simple logging).
11. Redirigir a página previa después de login.
12. Bloquear vista si usuario inactivo.
13. Agregar recuperación de contraseña (estructura base).
14. Mejorar UX de formularios de auth con estilos.
15. Documentar política de permisos del proyecto.

## 🔵 Nivel Desafío (31–45)

1. Sistema completo de roles: admin, editor, lector.
2. Permisos por objeto (owner-based) en todo el CRUD.
3. Middleware simple de auditoría de accesos.
4. Panel de perfil de usuario con edición básica.
5. Historial de acciones por usuario.
6. Límite básico de intentos de login (simulado).
7. Ocultar rutas sensibles en navegación según rol.
8. Crear decorador personalizado de permiso.
9. Aplicar pruebas manuales de seguridad.
10. Rediseñar flujo auth para UX profesional.
11. Integrar mensajes globales para seguridad.
12. Documentar amenazas comunes y mitigación básica.
13. Preparar settings para producción en auth.
14. Integrar política de contraseñas más fuerte.
15. Entregar módulo auth+permisos listo para producción inicial.

## 🏁 Proyecto de cierre de clase

Integrar autenticación completa y permisos por propietario sobre el CRUD de productos.
