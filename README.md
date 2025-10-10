#  X-Code Chat — Estructura General

## 📌 Descripción  
Este proyecto gestiona el ecosistema de **X-Code Chat**, incluyendo:
- Entorno de desarrollo (Dev) → pruebas, mejoras y validaciones.  
- Entorno de producción (Prod) → versión oficial pública y estable.  
- Sincronización completa entre **Firebase**, **GitHub** y **Vercel**.

---

## 🔹 Estructura de entornos

| Entorno | Dominio | Propósito |
|----------|----------|-----------|
| **Dev** | https://dev-chat.x-code.es | Pruebas, desarrollo de nuevas funciones y validación. |
| **Producción** | https://chat.x-code.es | Versión final estable y pública. |

---

## 🔹 Archivos principales

| Archivo | Descripción |
|----------|--------------|
| `index_chat_dev.html` | Código principal del chat en entorno de desarrollo. |
| `index_chat.html` | Código de la versión oficial estable (producción). |
| `MEJORAS_DEV.md` | Registro de mejoras, tareas y pruebas en entorno Dev. |
| `MEJORAS_PROD.md` | Registro de implementaciones validadas listas para producción. |
| `vercel.json` | Configuración de despliegue para Vercel (rutas, rewrites, etc.). |

---

## 🔹 Flujo de trabajo

1. **Desarrollo inicial**
   - Se actualiza y prueba el código en `index_chat_dev.html`.
   - Las pruebas se despliegan automáticamente en **Vercel (Dev)**.

2. **Validación**
   - Se testean las nuevas funciones (salas, usuarios, login, persistencia, etc.).
   - Cuando la versión pasa todas las pruebas → se documenta en `MEJORAS_PROD.md`.

3. **Despliegue a producción**
   - Se copia el archivo estable a `index_chat.html`.
   - Se actualiza el branch principal en GitHub.
   - Vercel actualiza automáticamente el dominio de producción.

---

## 🔹 Integración con Firebase

Cada entorno usa su propio **proyecto de Firebase**:

| Entorno | Proyecto | URL Realtime Database |
|----------|-----------|------------------------|
| **DEV** | `x-code-chat-dev` | `https://x-code-chat-dev-default-rtdb.europe-west1.firebasedatabase.app` |
| **PROD** | `x-code-chat` | `https://x-code-chat-default-rtdb.europe-west1.firebasedatabase.app` |

✅ Ambos comparten estructura de datos:

---

## 🔹 Estilo visual
- Diseño **negro y dorado**, inspirado en la versión “X-Code Chat — Official”.  
- Interfaz **responsiva** y minimalista.  
- Mantiene coherencia estética entre entornos Dev y Prod.

---

## 🔹 Mantenimiento
- Cada commit en Dev se despliega automáticamente en `https://dev-chat.x-code.es`.
- La rama de producción se actualiza solo tras validación final.
- Se recomienda crear **backups locales** de los archivos HTML y configuraciones Firebase antes de cada deploy.

---

## 🔹 Créditos
**Proyecto:** X-Code Chat  
**Desarrollador principal:** Fabio de Pina
**Infraestructura:** Firebase + GitHub + Vercel  
**Diseño:** Identidad visual X-Code Official  

