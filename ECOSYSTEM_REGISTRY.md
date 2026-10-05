# 🌐 Registro de Ecosistema — WoWPeru_DBM

Ficha técnica oficial de registro en la infraestructura multi-addon de **WoW Perú - Reino Andino**.

---

## 1. Identidad de la Suite

| Campo | Valor |
|---|---|
| **Nombre Técnico** | `Deadly Boss Mods (DBM Suite)` |
| **Título en Cliente** | `|cffffd200Deadly Boss Mods|r` |
| **Versión** | `4.52-WP` (Rev 4442) |
| **Tipo de Sistema** | Temporizadores y Avisos Tácticos de Banda / Mazmorra |
| **Repositorio GitHub** | [DarckRovert/WoWPeru_DBM](https://github.com/DarckRovert/WoWPeru_DBM) |
| **Directorios de Instalación** | 13 carpetas individuales en `Interface\AddOns\` |

---

## 2. Persistencia de Datos

| Variable Global | Tipo | Ámbito | Propósito |
|---|---|---|---|
| `DBM_SavedVars` | Tabla Lua (`SavedVariables`) | Por Cuenta | Configuración del motor central, posición de barras y audio |
| `DBM_SavedVars_PerChar` | Tabla Lua (`SavedVariablesPerCharacter`) | Por Personaje | Opciones específicas por personaje |

---

## 3. Matriz de Integración

| Sistema Coexistente | Modo de Interacción | Flujo de Datos |
|---|---|---|
| **`WoWPeru_RaidSuite`** | Coexistencia de Bandas | Coordinación de combate sin solapamiento de combat log |
| **`WoWPeru_DragonflightUI`** | Interfaz Visual | Anclajes de barras de temporizador compatibles con UI moderna |
| **`WoWPeru_Companion`** | Telemetría | Detección pasiva en auditoría de addons |
