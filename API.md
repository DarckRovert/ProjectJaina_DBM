# 🔌 Especificación Técnica y API — WoWPeru_DBM

[![GitHub](https://img.shields.io/badge/GitHub-DarckRovert%2FWoWPeru_DBM-black?logo=github)](https://github.com/DarckRovert/WoWPeru_DBM)
[![Ecosistema](https://img.shields.io/badge/Ecosistema-WoW%20Per%C3%BA%203.3.5a-gold.svg)](https://wow-peru.lat/)

## 📌 Resumen Arquitectónico
Monorepositorio unificado de Deadly Boss Mods con 13 módulos completos para todas las bandas y mazmorras de WotLK, desanidado, estabilizado y con advertencias de sonido sincronizadas.

- **Rol en el Ecosistema:** Suite Comunitaria Monorepo — Alertas de Banda DBM
- **Archivo Principal TOC:** `DBM-Core.toc`
- **Compatibilidad del Motor:** World of Warcraft 3.3.5a (Build 12340)

---

## ⌨️ Comandos de Consola (Slash Commands)
- `/dbm`: Acceso principal o comando del addon.
- `/range`: Acceso principal o comando del addon.
- `/distance`: Acceso principal o comando del addon.

---

## 📡 Protocolo de Red y Eventos
- `DBMv4-CombatInfo`: Prefijo registrado para sincronización de datos.
- `DBMv4-RequestTimers`: Prefijo registrado para sincronización de datos.
- `DBMv4-TimerInfo`: Prefijo registrado para sincronización de datos.
- `DBMv4-Ver`: Prefijo registrado para sincronización de datos.

### Eventos del Motor 3.3.5a Gestionados
- `PLAYER_LOGIN` / `ADDON_LOADED`: Inicialización atómica de tablas de configuración y hooks.
- `PLAYER_ENTERING_WORLD`: Sincronización de estado tras transiciones de pantalla o mapa.
- `PLAYER_LOGOUT`: Guardado seguro en disco de las variables locales.

---

## 💾 Persistencia de Datos (SavedVariables)
- `DBM_SavedOptions`: Almacenamiento estructurado de configuración y estado persistente.
- `DBT_SavedOptions`: Almacenamiento estructurado de configuración y estado persistente.

---

## 🛠️ Buenas Prácticas de Integración
1. Toda invocación a funciones públicas debe verificar previamente la existencia del espacio de nombres en `_G`.
2. Las tablas de configuración deben consultarse en modo lectura sin sobreescribir valores por omisión no validados.
3. El intercambio de datos con otros addons debe efectuarse a través del bus oficial `WoWPeru_Companion` o hooks de eventos estándar.
