# 🚀 X-Code Chat — Registro de Mejoras (Entorno DEV)

## 🧠 Objetivo
Este documento registra todas las **mejoras, correcciones y pruebas** realizadas en el entorno de desarrollo (`dev-chat.x-code.es`), antes de su validación final para producción.

---

## 🧩 Mejora 1 — Ajuste visual general del chat
**Estado:** ✅ Implementado  
**Fecha:** [Pendiente de commit]

### Descripción:
- Se reducen los espacios inferiores del área de chat (modelo visual estilo WhatsApp / ChatGPT).
- Se mantiene la estética **negro y dorado** oficial de X-Code Chat.

### Resultado esperado:
- Interfaz más compacta y funcional en dispositivos móviles y escritorio.

---

## 🧩 Mejora 2 — Notificación visual de mensajes
**Estado:** ⚙️ En desarrollo

### Descripción:
- Implementar notificación visual o sonora al recibir un nuevo mensaje.
- Compatible con salas privadas y chat general.
- Opción de activar/desactivar en configuración del usuario.

### Requisitos:
- Firebase listener activo sobre `rooms/<sala>/messages`.
- Evento visual tipo "flash" o contador dorado en la pestaña.

---

## 🧩 Mejora 3 — Panel de organizador
**Estado:** 🧪 En pruebas

### Descripción:
- Reorganización completa del panel de organizador.  
- Cada botón (crear, eliminar, editar salas) encapsulado en un rectángulo.  
- Visual adaptable y escalable según el tamaño de pantalla.

### Adicional:
- El organizador **decide qué sala permanece activa**, desactivando el modo automático.
- Persistencia guardada en Firebase (`roomsMeta/activeRoom`).

---

## 🧩 Mejora 4 — Proporción entre lista de usuarios y área del chat
**Estado:** 🧩 Implementado (en pruebas)

### Descripción:
- Ajuste dinámico de ancho y altura de las columnas laterales.  
- Mejora visual de equilibrio entre panel izquierdo (usuarios/salas) y el chat principal.

---

## 🧩 Mejora 5 — Gestión de usuarios activos/inactivos
**Estado:** 🧪 En desarrollo

### Descripción:
- Cuando un usuario se desactiva, desaparece temporalmente de la lista de usuarios y sala.  
- Si vuelve a iniciar sesión con el mismo número/PIN → se reactiva automáticamente.

---

## 🧩 Mejora 6 — Persistencia de sesión
**Estado:** ⚠️ Pendiente de corrección

### Descripción:
- Error actual: al refrescar la página, se pierde la sesión y se solicita de nuevo el PIN.  
- Objetivo: mantener la sesión activa (almacenamiento local o Firebase Auth temporal).

---

## 🔧 Notas técnicas
- Todas las pruebas deben realizarse en la rama `dev` antes del merge a `main`.
- Cada mejora implementada debe confirmarse visualmente en el entorno:  
  👉 https://dev-chat.x-code.es  
- Commit final validado por el desarrollador principal antes del despliegue.

---

✍️ **Desarrollador:** X-Code Systems  
📅 **Última actualización:** _(agregar fecha actual del commit)_
