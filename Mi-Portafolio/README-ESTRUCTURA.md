# 📁 ESTRUCTURA DE TU PORTAFOLIO

## ¿Cómo están organizadas las carpetas?

```
📁 Mi-Portafolio/                           ← CARPETA PRINCIPAL
│
├── 📄 portfolio-james-paz.html             ← Página principal (abre esta)
├── 📄 GUIA-COMPLETA-proyectos.md           ← Guía completa paso a paso
├── 📄 README-ESTRUCTURA.md                 ← Este archivo
│
└── 📁 projects/                            ← Carpeta de proyectos
    │
    ├── 📄 PLANTILLA-proyecto.html          ← Copia esto para nuevos proyectos
    ├── 📄 proyecto-dashboard-rrhh.html     ← Ejemplo completo de proyecto
    │
    └── 📁 imagenes/                        ← Todas las imágenes de proyectos
        │
        ├── 📁 dashboard-rrhh/              ← Imágenes del proyecto RRHH
        │   ├── 🖼️ dashboard-principal.png
        │   ├── 🖼️ analisis-rotacion.png
        │   └── 🖼️ metricas-kpi.png
        │
        ├── 📁 [tu-proyecto-1]/             ← Crea carpetas así para tus proyectos
        │   ├── 🖼️ imagen1.png
        │   └── 🖼️ imagen2.png
        │
        └── 📁 [tu-proyecto-2]/
            └── 🖼️ imagenes...
```

---

## 🎯 LO MÁS IMPORTANTE

### 1. ¿Dónde está cada cosa?

| Archivo/Carpeta | Ubicación | Qué es |
|----------------|-----------|---------|
| `portfolio-james-paz.html` | Raíz | Tu página principal |
| `projects/` | Dentro de raíz | Carpeta con todos tus proyectos |
| `projects/PLANTILLA-proyecto.html` | Dentro de projects | Plantilla para copiar |
| `projects/imagenes/` | Dentro de projects | Todas las imágenes |
| `projects/imagenes/mi-proyecto/` | Dentro de imagenes | Imágenes de UN proyecto |

### 2. ¿Cómo agregar imágenes?

**PASO 1:** Crea una carpeta para tu proyecto
```
projects/imagenes/[nombre-de-tu-proyecto]/
```

**PASO 2:** Guarda tus imágenes ahí
```
projects/imagenes/analisis-ventas/dashboard.png
projects/imagenes/analisis-ventas/graficos.png
```

**PASO 3:** Usa esta ruta en el HTML
```html
<img src="imagenes/analisis-ventas/dashboard.png">
```

---

## 🚀 INICIO RÁPIDO

### Para ver tu portafolio:
1. Abre `portfolio-james-paz.html` en tu navegador
2. Haz clic en la tarjeta de un proyecto
3. ¡Listo!

### Para crear un nuevo proyecto:
1. Ve a `projects/`
2. Copia `PLANTILLA-proyecto.html`
3. Renómbralo: `proyecto-mi-analisis.html`
4. Edita el contenido
5. Crea carpeta en `imagenes/mi-analisis/`
6. Agrega tus imágenes
7. Actualiza `portfolio-james-paz.html`

---

## 📸 RUTAS DE IMÁGENES - EJEMPLOS REALES

### ❌ INCORRECTO
```html
<!-- NO hagas esto: -->
<img src="C:/Users/James/Mi-Portafolio/projects/imagenes/foto.png">
<img src="projects/imagenes/mi-proyecto/foto.png">
<img src="../imagenes/mi-proyecto/foto.png">
```

### ✅ CORRECTO
```html
<!-- Haz esto: -->
<img src="imagenes/mi-proyecto/foto.png">
```

**¿Por qué?**
Porque el archivo HTML del proyecto (`proyecto-mi-analisis.html`) está en `projects/`, entonces desde ahí la ruta correcta es `imagenes/[tu-carpeta]/imagen.png`

---

## 🗂️ EJEMPLO COMPLETO

Imagina que vas a crear un proyecto llamado "Análisis de Ventas"

### 1. Estructura de carpetas
```
Mi-Portafolio/
├── portfolio-james-paz.html
└── projects/
    ├── proyecto-analisis-ventas.html     ← Tu nuevo archivo
    └── imagenes/
        └── analisis-ventas/              ← Tu nueva carpeta
            ├── dashboard-ventas.png
            ├── grafico-tendencias.png
            └── tabla-resultados.png
```

### 2. En tu HTML (`proyecto-analisis-ventas.html`)
```html
<div class="image-container">
    <img src="imagenes/analisis-ventas/dashboard-ventas.png" alt="Dashboard">
</div>
<p class="image-caption">Dashboard principal de ventas</p>

<div class="image-container">
    <img src="imagenes/analisis-ventas/grafico-tendencias.png" alt="Gráficos">
</div>
<p class="image-caption">Análisis de tendencias mensuales</p>
```

### 3. En `portfolio-james-paz.html`
```html
<a href="projects/proyecto-analisis-ventas.html" class="project-card fade-in">
    <div class="project-header">
        <h3 class="project-title">Análisis de Ventas</h3>
        <p class="project-objective">
            Dashboard que incrementó las ventas en 32% mediante 
            identificación de oportunidades de cross-selling
        </p>
    </div>
    <div class="project-tools">
        <span class="tools-label">Herramientas</span>
        <div class="tools-list">
            <span class="tool-tag">Power BI</span>
            <span class="tool-tag">SQL</span>
        </div>
    </div>
</a>
```

---

## 💡 TIPS IMPORTANTES

### ✅ BUENAS PRÁCTICAS

1. **Nombres de archivos:**
   - Usa minúsculas: `dashboard.png` ✅
   - Sin espacios: `mi-imagen.png` ✅ (`mi imagen.png` ❌)
   - Sin tildes: `analisis.png` ✅ (`análisis.png` ❌)
   - Sin caracteres especiales: `grafico-1.png` ✅ (`gráfico_#1.png` ❌)

2. **Organización:**
   - Una carpeta por proyecto en `imagenes/`
   - Nombres descriptivos: `dashboard-principal.png` mejor que `img1.png`
   - Numera si es necesario: `paso-1.png`, `paso-2.png`

3. **Tamaño de imágenes:**
   - Máximo 1920px de ancho
   - Formato PNG para capturas de pantalla
   - Comprime tus imágenes (usa tinypng.com)

---

## 🌐 PARA PUBLICAR EN INTERNET

### Opción 1: GitHub Pages (Recomendado)

1. Sube toda la carpeta `Mi-Portafolio` a GitHub
2. La estructura se mantiene igual
3. GitHub Pages funciona automáticamente
4. Tu portafolio será: `tu-usuario.github.io/mi-portafolio/portfolio-james-paz.html`

**TIP:** Renombra `portfolio-james-paz.html` a `index.html` para tener una URL más corta:
`tu-usuario.github.io/mi-portafolio/`

### Opción 2: Netlify

1. Arrastra toda la carpeta a Netlify
2. ¡Listo!

---

## ❓ PREGUNTAS FRECUENTES

**P: ¿Puedo cambiar los nombres de las carpetas?**
R: Sí, pero tendrías que actualizar todas las rutas en el HTML.

**P: ¿Puedo poner las imágenes fuera de `projects`?**
R: Sí, pero las rutas cambiarían. Es más fácil mantener todo en `projects/imagenes/`.

**P: ¿Cómo sé si la ruta de mi imagen es correcta?**
R: Abre tu proyecto en el navegador. Si la imagen se ve, la ruta es correcta.

**P: ¿Qué hago si mi imagen no aparece?**
R: Verifica:
   1. El archivo existe en la carpeta correcta
   2. El nombre del archivo coincide exactamente (mayúsculas/minúsculas)
   3. La ruta en el HTML es `imagenes/tu-proyecto/imagen.png`

---

## 📞 ¿NECESITAS AYUDA?

Si algo no funciona:

1. Revisa la **GUIA-COMPLETA-proyectos.md**
2. Verifica que tu estructura de carpetas coincida con este README
3. Comprueba que las rutas de imágenes sean correctas
4. Abre el navegador con F12 para ver errores en la consola

---

**Última actualización:** Febrero 2026  
**Creado para:** James Paz - Analytics Portfolio
