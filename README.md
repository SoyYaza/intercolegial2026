# 🏆 Intercolegial de Baile 2026
### Colegio de Bachilleres del Estado de BCS — Plantel 11

Sistema web oficial de captura y visualización de puntajes para el **Intercolegial de Baile COBACH BCS 2026**.

---

## ✨ Funciones principales

- 🔐 **Login por roles** — Administrador, 5 jueces independientes y modo visitante
- ✏️ **Captura de puntajes** — Cada juez evalúa desde su propio dispositivo
- 📊 **Concentrado en tiempo real** — Promedio automático de los 5 jueces, refresco cada 10 segundos
- 🏆 **Clasificación en vivo** — Resultado final actualizado automáticamente
- 📄 **Exportar reporte PDF** — Reporte completo con clasificación, concentrado y detalle por juez
- 💾 **Respaldo de datos** — Exportar e importar datos en formato JSON
- 🗑️ **Reinicio de captura** — El admin puede limpiar todos los puntajes para empezar de nuevo
- 👁️ **Modo visitante** — Vista pública de resultados sin necesidad de contraseña

---

## 🗂️ Estructura del proyecto

```
/
└── index.html       # Aplicación completa (una sola página)
└── README.md        # Este archivo
```

---

## ⚙️ Tecnologías utilizadas

| Componente | Tecnología |
|---|---|
| Frontend | HTML + CSS + JavaScript (vanilla) |
| Hosting | GitHub Pages (gratuito) |
| Base de datos | Google Sheets |
| Backend | Google Apps Script (Web App) |
| Tipografía | Barlow + Barlow Condensed (Google Fonts) |

---

## 👥 Roles y accesos

| Usuario | Contraseña | Acceso |
|---|---|---|
| `admin` | *(definida por el administrador)* | Panel completo + administración |
| `juez1` al `juez5` | *(definidas por el administrador)* | Captura de puntajes propios |
| *(sin usuario)* | — | Modo visitante — solo resultados |

> ⚠️ Las contraseñas se gestionan desde el panel de administración y se almacenan en Google Sheets.

---

## 📋 Criterios de evaluación

Cada juez evalúa **5 categorías** por grupo:

| Categoría | Campos |
|---|---|
| Proyección | Interacción con el público · Presencia escénica · Proyección juvenil |
| Vestuario | Colorimetría · Representación · Accesorios · Maquillaje |
| Adaptación al tema | Mezcla musical · Adapt. vestuario · Integración de elementos |
| Escenografía | Escenografía al tema · Ambientación · Creatividad · Originalidad |
| Presentación del baile | Coreografía · Coordinación grupal · Desplazamiento · Limpieza · Originalidad |

---

## 🏫 Grupos participantes

**2° Semestre**
- II A — La Mil y Una Noches
- II B — Circo
- II B T.V — Disco
- II C — Fiesta Deportiva
- II D — Festival Latino
- II E — Piratas

**4° Semestre**
- IV A — Retro
- IV B — Carnaval
- IV C — Playero
- IV E — Festival Bollywood

---

## 🚀 Configuración del proyecto

### 1. Google Sheets

Crear una hoja de cálculo con 3 pestañas:

**`puntajes`** — encabezados en fila 1:
```
timestamp | juez | grupo | campo | valor
```

**`jueces`** — encabezados en fila 1:
```
juez | nombre | contraseña
```
Filas 2–6: `1`, `2`, `3`, `4`, `5` en columna A.

**`config`** — reservada para uso futuro.

### 2. Google Apps Script

1. En la hoja → **Extensiones → Apps Script**
2. Pegar el contenido de `Code.gs` (ver sección siguiente)
3. **Implementar → Nueva implementación → Aplicación web**
   - Ejecutar como: `Yo`
   - Acceso: `Cualquier usuario`
4. Copiar la URL generada

### 3. GitHub Pages

1. Subir `index.html` a este repositorio
2. **Settings → Pages → Branch: main → Save**
3. El sitio estará disponible en:
   ```
   https://<tu-usuario>.github.io/<nombre-del-repo>
   ```

---

## 🔧 Mantenimiento

- **Cambiar contraseñas:** Panel Admin → sección "Contraseñas de jueces"
- **Cambiar nombres de jueces:** Panel Admin → sección "Nombres de los jueces"
- **Reiniciar captura:** Panel Admin → botón "Reiniciar captura" (pide confirmación)
- **Respaldo:** Panel Admin → "Exportar datos" antes de cualquier reinicio
- **Restaurar respaldo:** Panel Admin → "Importar datos" → seleccionar archivo `.json`

---

## 📄 Licencia

Uso interno institucional — **COBACH BCS Plantel 11** · Ciclo escolar 2025–2026.
Por **Yazahel Bustos**
---

<p align="center">
  Desarrollado para el <strong>Intercolegial de Baile COBACH BCS 2026</strong><br>
  Plantel 11 — La Paz, Baja California Sur
</p>
