# 🇵🇪 Project Jaina — Deadly Boss Mods (DBM Suite WotLK 3.3.5a)

**Versión de DBM:** 4.52 Release (Rev 4442)  
**Autores Originales:** Tandanu & Nitram (DBM Development Team)  
**Empaquetado y Hardening:** DarckRovert & Project Jaina Staff  
**Servidor Destino:** [Project Jaina](https://darckrovert.github.io/ProjectJaina_Web/) — Theramore  
**Entorno de Ejecución:** World of Warcraft 3.3.5a (Build 12340) | Lua 5.1  
**Repositorio Oficial:** [DarckRovert/ProjectJaina_DBM](https://github.com/DarckRovert/ProjectJaina_DBM)  

---

[![WoW Client](https://img.shields.io/badge/WoW%20Client-3.3.5a%20(Build%2012340)-blue.svg)](https://darckrovert.github.io/ProjectJaina_Web/)
[![Servidor](https://img.shields.io/badge/Servidor-WoW%20Perú-gold.svg)](https://darckrovert.github.io/ProjectJaina_Web/)
[![Version](https://img.shields.io/badge/version-4.52--WP-brightgreen.svg)](https://github.com/DarckRovert/ProjectJaina_DBM/releases)
[![License: CC BY-NC-SA 3.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%203.0-orange.svg)](LICENSE)

---

## 🌟 Descripción General

Este monorepositorio centraliza la suite completa y verificada de **Deadly Boss Mods (DBM)** para el cliente 3.3.5a de Project Jaina. Agrupa en una sola unidad de versionado los 13 módulos requeridos para todas las bandas, mazmorras y encuentros de WotLK.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   SUITE DEADLY BOSS MODS (13 MÓDULOS)                  │
├────────────────────────┬──────────────────────┬────────────────────────┤
│ ⏱️ TEMPORIZADORES RAID │ 🛡️ CORONA DE HIELO   │ ⚡ MAZMORRAS Y PVP     │
│ Barras dinámicas,      │ Halion, ICC, Ulduar, │ Módulos completos para │
│ avisos sonoros y rango │ Naxxramas y Coliseo  │ party WotLK y arenas/BG│
└────────────────────────┴──────────────────────┴────────────────────────┘
```

---

## 🛠️ Correcciones y Hardening Realizado por Project Jaina

1. **Reparación Estructural de `DBM-Naxx`:**
   - Se eliminó la estructura redundante anidada (`DBM-Naxx/DBM-Naxx/DBM-Naxx.toc`) que causaba fallos de carga en clientes estándar al no detectar el archivo `.toc` en la raíz de la carpeta del addon.
2. **Validación de Assets y Sonidos:**
   - Todos los archivos `.ogg`, `.mp3` y texturas `.tga`/`.blp` fueron verificados contra el pipeline de streaming del motor 3.3.5a.
3. **Inmunidad a Taint:**
   - Sin llamadas a funciones protegidas; sincronización limpia con el registro de combate.

---

## 📦 Catálogo de Módulos Incluidos

| Carpeta de Addon | Contenido / Alcance |
|---|---|
| `DBM-Core` | Motor central, cálculo de timers, sync raid y avisos de audio |
| `DBM-GUI` | Panel de opciones visuales y configuración `/dbm` |
| `DBM-ChamberOfAspects` | Sagrario Obsidiana (Sartharion) y Sagrario Rubí (Halion) |
| `DBM-Coliseum` | Prueba del Cruzado (ToC) y Prueba del Gran Cruzado (ToGC) |
| `DBM-EyeOfEternity` | El Ojo de la Eternidad (Malygos) |
| `DBM-Icecrown` | Ciudadela de la Corona de Hielo (ICC) y Rey Exánime |
| `DBM-Naxx` | Naxxramas (10 y 25 jugadores) |
| `DBM-Onyxia` | Guarida de Onyxia (60 / 80) |
| `DBM-Party-WotLK` | Mazmorras heroicas de Wrath of the Lich King |
| `DBM-PvP` | Campos de batalla (WSG, AB, EotS, AV, IoC) |
| `DBM-Ulduar` | Ulduar completo (Normal y Hard Modes) |
| `DBM-VoA` | Cámara de Archavon |
| `DBM-WorldEvents` | Jefes de festividades del mundo |

---

## 💻 Comandos de Barra (Slash Commands)

| Comando | Acción |
|---|---|
| `/dbm` | Abre el panel gráfico de configuración de Deadly Boss Mods. |
| `/dbm ver` | Comprueba y lista las versiones de DBM instaladas por los miembros de la banda. |
| `/dbm pull <segundos>` | Inicia una cuenta regresiva oficial visible para toda la banda antes de iniciar el combate. |
| `/dbm break <minutos>` | Inicia un temporizador de descanso o pausa para la banda. |
| `/dbm broadcast timer <seg> <texto>` | Transmite una barra de temporizador personalizada a toda la banda. |

---

## 📥 Instalación en el Cliente WoW

Para instalar la suite en tu cliente Project Jaina:
1. Descarga el repositorio o release comprimido en `.zip`.
2. Extrae las 13 carpetas directamente dentro del directorio:
   ```
   World of Warcraft/Interface/AddOns/
   ```
3. Verifica que cada carpeta (`DBM-Core`, `DBM-Icecrown`, etc.) quede como carpeta hermana dentro de `Interface/AddOns/`.
4. Inicia el juego y asegúrate de marcar la casilla *"Cargar accesorios antiguos"* en la pantalla de selección de personajes.

---

## 📜 Licencia y Atribución

Distribuido bajo la licencia [Creative Commons BY-NC-SA 3.0](LICENSE).  
Para consultar los detalles de autoría original de Tandanu y Nitram, consulta el archivo [NOTICE.md](NOTICE.md).
