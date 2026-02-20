# 🚀 Clase 09: Deploy del Proyecto

[🏠 Volver al índice](../README.md) [⬅️ Clase anterior](../Clase_08_Buenas_Practicas/Clase_08_Buenas_Practicas.md) |
[➡️ Siguiente clase](../Clase_10_Proyecto_Final/Clase_10_Proyecto_Final.md)

## 🎯 Tema

Publicación del proyecto Django en la nube.

## 🧭 Objetivo general

Publicar la aplicación Django en un entorno cloud con configuración estable, variables seguras y validación funcional
completa.

## 🎯 Objetivos específicos

Al finalizar la clase, el estudiante podrá:

1. Versionar y subir correctamente el proyecto a un repositorio remoto.
2. Configurar despliegue en una plataforma cloud.
3. Definir variables de entorno para producción.
4. Ejecutar migraciones y preparar estáticos en entorno remoto.
5. Validar la aplicación en una URL pública y depurar con logs.

## 🧠 Explicación

Deploy significa pasar de tu máquina local a un servidor accesible por internet. Para esto debes versionar el proyecto,
declarar dependencias y configurar variables del entorno remoto.

Esta clase conecta todo lo construido hasta ahora con un entorno real de operación.

## 🧱 Estructura de la clase

- **Objetivo:** desplegar la app en una URL pública.
- **Conceptos clave:** Git, repositorio remoto, dependencias, `Procfile`, variables de entorno.
- **Práctica guiada:** despliegue en plataforma cloud.
- **Reto:** validar flujo completo online.

## 🗂️ Contenido enriquecido de la Clase 9

- [📚 Glosario de deploy en Django](01_Glosario_Deploy_Django.md)
- [🧰 Guía de deploy paso a paso](02_Guia_Deploy_Paso_a_Paso.md)
- [🧪 Ejemplos paso a paso](03_Ejemplos_Paso_a_Paso_Clase_09.md)
- [🧩 Banco amplio de ejercicios](04_Ejercicios_Clase_09.md)
- [✅ Ejercicios resueltos (selección)](05_Ejercicios_Resueltos_Clase_09.md)
- [🧠 Reto guiado de clase](06_Reto_Guiado_Clase_09.md)
- [✅ Checklist técnico](07_Checklist_Tecnico_Clase_09.md)

## 📊 Gráfico conceptual

```mermaid
flowchart LR
    A[Proyecto local] --> B[GitHub]
    B --> C[Plataforma Cloud]
    C --> D[URL pública 🌍]
```

## 💻 Código de ejemplo

```bash
git init
git add .
git commit -m "Primer deploy Django"
git branch -M main
git remote add origin <URL_DEL_REPO>
git push -u origin main
```

```txt
# Procfile (ejemplo)
web: gunicorn proyecto.wsgi
```

## 🧩 Definiciones rápidas (resumen)

- **Deploy:** publicación de la app para acceso en internet.
- **Build:** proceso de instalación y preparación de ejecución.
- **Runtime:** entorno donde corre la app.
- **Logs:** registro técnico para detectar errores.
- **URL pública:** dirección final accesible por usuarios.

> Puedes ampliar estos conceptos en el [glosario](01_Glosario_Deploy_Django.md).

## 🛠️ Práctica sugerida

1. Subir repositorio a GitHub.
2. Conectar repositorio con la plataforma.
3. Configurar variables y base de datos.
4. Verificar URL final.

## 🏋️ Práctica ampliada recomendada

- Resolver ejercicios **1 al 15** del [banco de ejercicios](04_Ejercicios_Clase_09.md).
- Resolver **8 ejercicios** del bloque intermedio.
- Resolver **4 ejercicios** del bloque desafío.
- Completar el [reto guiado](06_Reto_Guiado_Clase_09.md).
- Validar entrega con el [checklist técnico](07_Checklist_Tecnico_Clase_09.md).

## ⏱️ Sugerencia de ritmo para 2 horas

- 25 min: preparación técnica pre-deploy.
- 30 min: flujo Git + conexión cloud.
- 35 min: variables, DB, migraciones y estáticos.
- 30 min: validación online + análisis de logs.

## 🧪 Criterios de evaluación rápida

- **Deploy exitoso y estable (35%)**
- **Configuración de entorno segura (25%)**
- **Operación post-deploy (20%)**
- **Documentación técnica del proceso (20%)**

## ✅ Checklist

- [ ] App desplegada.
- [ ] Variables configuradas.
- [ ] Migraciones ejecutadas en producción.
- [ ] Sitio responde en URL pública.
- [ ] Logs revisados sin errores críticos.
- [ ] Entrega validada con checklist técnico.

---

## 🚀 Entregable de la Clase 9

Subir evidencia de despliegue con:

1. URL pública funcional.
2. Repositorio remoto actualizado.
3. Variables de entorno configuradas.
4. Migraciones y estáticos aplicados.
5. README con guía breve de despliegue.
