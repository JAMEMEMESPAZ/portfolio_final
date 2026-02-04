# 📚 GUÍA COMPLETA: Cómo Agregar Proyectos a Tu Portafolio

## 🗂️ PASO 0: ENTENDER LA ESTRUCTURA DE CARPETAS

### ¿Dónde van los archivos?

Todo vive en **tu computadora** (o en GitHub) en carpetas normales. NO es código dentro del HTML.

```
📁 Mi-Portafolio/                          ← Carpeta raíz (donde está todo)
│
├── portfolio-james-paz.html               ← Página principal (EN LA RAÍZ)
│
├── 📁 projects/                           ← Carpeta de proyectos (CREAR ESTA)
│   │
│   ├── PLANTILLA-proyecto.html            ← Plantilla para copiar
│   ├── proyecto-dashboard-rrhh.html       ← Ejemplo completo
│   ├── proyecto-analisis-ventas.html      ← Tus proyectos nuevos
│   ├── proyecto-prediccion-churn.html     ← Más proyectos...
│   │
│   └── 📁 imagenes/                       ← Todas las imágenes aquí
│       │
│       ├── 📁 dashboard-rrhh/             ← Carpeta por proyecto
│       │   ├── dashboard-principal.png
│       │   ├── analisis-rotacion.png
│       │   └── resultados-kpi.png
│       │
│       ├── 📁 analisis-ventas/
│       │   ├── dashboard-ventas.png
│       │   └── tendencias-mensual.png
│       │
│       └── 📁 prediccion-churn/
│           ├── modelo-prediccion.png
│           └── metricas-performance.png
```

---

## 🛠️ PASO 1: CREAR LAS CARPETAS

### Opción A: En Windows

1. **Crea la carpeta principal:**
   - Clic derecho en tu Escritorio o Documentos
   - Nuevo → Carpeta
   - Nómbrala: `Mi-Portafolio`

2. **Dentro de Mi-Portafolio, crea la carpeta projects:**
   - Entra a `Mi-Portafolio`
   - Clic derecho → Nueva carpeta
   - Nómbrala: `projects`

3. **Dentro de projects, crea la carpeta imagenes:**
   - Entra a `projects`
   - Clic derecho → Nueva carpeta
   - Nómbrala: `imagenes`

4. **Guarda los archivos descargados:**
   - `portfolio-james-paz.html` → En `Mi-Portafolio` (raíz)
   - `PLANTILLA-proyecto.html` → En `Mi-Portafolio/projects/`
   - `proyecto-dashboard-rrhh.html` → En `Mi-Portafolio/projects/`

### Opción B: En Mac

1. Abre Finder
2. Crea carpeta `Mi-Portafolio`
3. Dentro crea carpeta `projects`
4. Dentro de projects crea carpeta `imagenes`
5. Coloca los archivos como se indica arriba

### Opción C: En la Terminal (Windows/Mac/Linux)

```bash
# Crear estructura completa
mkdir Mi-Portafolio
cd Mi-Portafolio
mkdir projects
cd projects
mkdir imagenes
cd ..

# Ahora mueve los archivos descargados:
# - portfolio-james-paz.html va en Mi-Portafolio/
# - Los demás archivos van en Mi-Portafolio/projects/
```

---

## 📸 PASO 2: AGREGAR IMÁGENES A TUS PROYECTOS

### Dónde guardar las imágenes:

**REGLA DE ORO:** Una carpeta por proyecto dentro de `projects/imagenes/`

**Ejemplo práctico:**

Si vas a crear un proyecto llamado "Dashboard de Ventas", haz esto:

1. Entra a `Mi-Portafolio/projects/imagenes/`
2. Crea una nueva carpeta: `dashboard-ventas`
3. Guarda TODAS las imágenes de ese proyecto ahí

```
📁 projects/imagenes/dashboard-ventas/
    ├── captura-dashboard-principal.png
    ├── grafico-ventas-mensuales.png
    ├── analisis-por-region.png
    └── kpis-resumen.png
```

### Cómo referenciar las imágenes en el HTML:

Cuando estés editando tu archivo `proyecto-dashboard-ventas.html` (que está en `projects/`), usa esta ruta:

```html
<!-- Estructura de carpetas:
Mi-Portafolio/
  └── projects/
      ├── proyecto-dashboard-ventas.html  ← Estás editando este archivo
      └── imagenes/
          └── dashboard-ventas/
              └── captura-dashboard.png  ← Quieres mostrar esta imagen
-->

<!-- En el HTML, la ruta es: -->
<div class="image-container">
    <img src="imagenes/dashboard-ventas/captura-dashboard.png" alt="Dashboard principal">
</div>
<p class="image-caption">Figura 1: Dashboard principal de ventas</p>
```

**Explicación de la ruta:**
- `imagenes/` = Desde `projects/` entra a la carpeta `imagenes`
- `dashboard-ventas/` = Entra a la subcarpeta de tu proyecto
- `captura-dashboard.png` = El nombre de tu imagen

---

## 🚀 PASO 3: CREAR UN NUEVO PROYECTO

### A. Copiar la plantilla

1. Ve a `Mi-Portafolio/projects/`
2. Copia el archivo `PLANTILLA-proyecto.html`
3. Pégalo en la misma carpeta
4. Renómbralo: `proyecto-mi-nuevo-proyecto.html`

### B. Crear carpeta para imágenes del proyecto

1. Ve a `Mi-Portafolio/projects/imagenes/`
2. Crea una carpeta nueva: `mi-nuevo-proyecto`
3. Guarda ahí todas las capturas de pantalla, gráficos, etc.

### C. Editar el contenido

Abre `proyecto-mi-nuevo-proyecto.html` y busca todo lo que está entre `[corchetes]`:

```html
<!-- BUSCA ESTO: -->
<h1>[TÍTULO DEL PROYECTO]</h1>

<!-- REEMPLÁZALO CON ESTO: -->
<h1>Dashboard de Análisis de Ventas</h1>
```

### D. Agregar las imágenes

Busca en el HTML donde dice:

```html
<div class="image-container">
    <img src="ruta-a-tu-imagen.png" alt="Descripción">
</div>
```

Reemplázalo con:

```html
<div class="image-container">
    <img src="imagenes/mi-nuevo-proyecto/dashboard.png" alt="Dashboard principal">
</div>
<p class="image-caption">Figura 1: Vista general del dashboard de ventas</p>
```

---

## 🔗 PASO 4: AGREGAR EL PROYECTO A LA PÁGINA PRINCIPAL

1. Abre `portfolio-james-paz.html` (el que está en la raíz)
2. Busca esta sección (está cerca del final):

```html
<section id="projects">
    <div class="container">
        <!-- ... -->
        <div class="projects-grid">
            
            <!-- Proyecto existente -->
            <a href="projects/proyecto-dashboard-rrhh.html" class="project-card fade-in">
                <!-- ... -->
            </a>

            <!-- AQUÍ ABAJO PEGA TU NUEVO PROYECTO -->
            
        </div>
    </div>
</section>
```

3. **Justo debajo del último `</a>`, PEGA ESTO:**

```html
<a href="projects/proyecto-mi-nuevo-proyecto.html" class="project-card fade-in">
    <div class="project-header">
        <h3 class="project-title">Dashboard de Análisis de Ventas</h3>
        <p class="project-objective">
            Sistema de BI que identificó patrones de compra y permitió estrategias 
            de cross-selling que incrementaron las ventas en 32% en el primer trimestre.
        </p>
    </div>
    <div class="project-tools">
        <span class="tools-label">Herramientas Utilizadas</span>
        <div class="tools-list">
            <span class="tool-tag">Power BI</span>
            <span class="tool-tag">SQL</span>
            <span class="tool-tag">Python</span>
        </div>
    </div>
</a>
```

4. **Personaliza:**
   - Cambia `proyecto-mi-nuevo-proyecto.html` por el nombre real de tu archivo
   - Cambia el título, descripción y herramientas

---

## 🌐 PASO 5: SUBIR A GITHUB PAGES (Para publicar online)

### A. Preparar los archivos

Tu estructura debe verse así antes de subir:

```
Mi-Portafolio/
├── portfolio-james-paz.html
└── projects/
    ├── PLANTILLA-proyecto.html
    ├── proyecto-dashboard-rrhh.html
    ├── proyecto-analisis-ventas.html
    └── imagenes/
        ├── dashboard-rrhh/
        │   └── (tus imágenes)
        └── analisis-ventas/
            └── (tus imágenes)
```

### B. Subir a GitHub

1. **Crear repositorio en GitHub:**
   - Ve a github.com y crea un nuevo repositorio
   - Nómbralo: `mi-portafolio` (o como quieras)
   - Márcalo como "Public"

2. **Subir archivos:**
   - Opción 1: Arrastra toda la carpeta `Mi-Portafolio` a GitHub
   - Opción 2: Usa GitHub Desktop (más fácil para principiantes)
   - Opción 3: Usa Git desde terminal

3. **Activar GitHub Pages:**
   - En tu repositorio, ve a Settings
   - Busca "Pages" en el menú lateral
   - En "Source", selecciona la rama `main`
   - Guarda

4. **Tu portafolio estará en:**
   ```
   https://tu-usuario.github.io/mi-portafolio/portfolio-james-paz.html
   ```

### C. IMPORTANTE: Renombrar archivo principal

Para que tu URL sea más corta, renombra:
- `portfolio-james-paz.html` → `index.html`

Así tu portafolio será:
```
https://tu-usuario.github.io/mi-portafolio/
```

Y GitHub automáticamente abrirá `index.html`

---

## ❓ PREGUNTAS FRECUENTES

### ¿Por qué mis imágenes no se ven?

**Problema común:** Ruta incorrecta

**Solución:**
1. Verifica que la imagen esté en la carpeta correcta
2. La ruta debe ser relativa desde el archivo HTML

Ejemplo:
```
Si tu archivo es: projects/proyecto-ventas.html
Y tu imagen es: projects/imagenes/ventas/dashboard.png

Entonces la ruta es: imagenes/ventas/dashboard.png
```

**Tip:** Los nombres de carpetas e imágenes NO deben tener:
- ❌ Espacios: `mi imagen.png`
- ❌ Tildes: `análisis.png`
- ❌ Ñ: `diseño.png`
- ✅ Usa: `mi-imagen.png`, `analisis.png`, `diseno.png`

### ¿Puedo organizar las imágenes de otra forma?

**Sí**, pero mantén la consistencia. Si prefieres:

```
📁 Mi-Portafolio/
├── portfolio-james-paz.html
├── 📁 projects/
│   ├── proyecto-1.html
│   └── proyecto-2.html
└── 📁 imagenes/              ← Fuera de projects
    ├── proyecto-1/
    └── proyecto-2/
```

Entonces las rutas en el HTML cambian:

```html
<!-- Desde projects/proyecto-1.html -->
<img src="../imagenes/proyecto-1/dashboard.png">
```

El `..` significa "sube un nivel" (sal de `projects/`)

---

## 📋 CHECKLIST ANTES DE PUBLICAR

- [ ] Carpeta `Mi-Portafolio` creada
- [ ] Subcarpeta `projects` creada
- [ ] Subcarpeta `projects/imagenes` creada
- [ ] `portfolio-james-paz.html` en la raíz
- [ ] Archivos de proyectos en `projects/`
- [ ] Imágenes organizadas en `projects/imagenes/nombre-proyecto/`
- [ ] Rutas de imágenes correctas en el HTML
- [ ] Proyecto agregado a `portfolio-james-paz.html`
- [ ] Probado localmente (abrir HTML en navegador)
- [ ] Todas las imágenes se ven correctamente
- [ ] Enlaces funcionan (clic en tarjeta de proyecto)

---

## 🎯 EJEMPLO COMPLETO PASO A PASO

Vamos a crear un proyecto real desde cero:

**Proyecto:** "Análisis de Rotación de Personal"

### Paso 1: Crear estructura
```
1. En Mi-Portafolio/projects/, crea: imagenes/rotacion-personal/
2. Guarda tus capturas ahí: 
   - dashboard-principal.png
   - tendencias-rotacion.png
   - causas-principales.png
```

### Paso 2: Copiar plantilla
```
1. Copia PLANTILLA-proyecto.html
2. Pégala en projects/
3. Renómbrala: proyecto-rotacion-personal.html
```

### Paso 3: Editar contenido
```html
<!-- Abre proyecto-rotacion-personal.html -->

<!-- Cambiar título -->
<h1>Análisis de Rotación de Personal</h1>

<!-- Cambiar herramientas -->
<span class="tool-badge">Power BI</span>
<span class="tool-badge">Python</span>
<span class="tool-badge">Excel</span>

<!-- Agregar imágenes -->
<div class="image-container">
    <img src="imagenes/rotacion-personal/dashboard-principal.png" alt="Dashboard">
</div>
<p class="image-caption">Dashboard principal de rotación</p>
```

### Paso 4: Agregar a página principal
```html
<!-- Abre portfolio-james-paz.html -->

<!-- Busca la sección de proyectos y agrega: -->
<a href="projects/proyecto-rotacion-personal.html" class="project-card fade-in">
    <div class="project-header">
        <h3 class="project-title">Análisis de Rotación de Personal</h3>
        <p class="project-objective">
            Dashboard que identificó las 5 causas principales de rotación, 
            permitiendo reducir la tasa de salida en un 28% en 6 meses.
        </p>
    </div>
    <div class="project-tools">
        <span class="tools-label">Herramientas Utilizadas</span>
        <div class="tools-list">
            <span class="tool-tag">Power BI</span>
            <span class="tool-tag">Python</span>
            <span class="tool-tag">Excel</span>
        </div>
    </div>
</a>
```

### Paso 5: Probar
```
1. Abre portfolio-james-paz.html en tu navegador
2. Verifica que aparezca la nueva tarjeta
3. Haz clic en la tarjeta
4. Debe abrir proyecto-rotacion-personal.html
5. Verifica que las imágenes se vean
```

---

## 🆘 SOLUCIÓN DE PROBLEMAS

### Problema: "El enlace no funciona cuando hago clic"

**Causa:** Ruta incorrecta en `href`

**Solución:** Verifica que en `portfolio-james-paz.html` el enlace sea:
```html
<a href="projects/proyecto-nombre.html" ...>
```

NO:
```html
<a href="proyecto-nombre.html" ...>  ❌
<a href="/projects/proyecto-nombre.html" ...>  ❌
```

### Problema: "Las imágenes no se ven"

**Causa 1:** Nombre de archivo incorrecto
- Verifica mayúsculas/minúsculas
- `Dashboard.PNG` ≠ `dashboard.png`

**Causa 2:** Ruta incorrecta
```html
<!-- Si el archivo está en: projects/proyecto-1.html -->
<!-- Y la imagen está en: projects/imagenes/proyecto-1/foto.png -->

<!-- Correcto: -->
<img src="imagenes/proyecto-1/foto.png">

<!-- Incorrecto: -->
<img src="projects/imagenes/proyecto-1/foto.png">  ❌
<img src="../imagenes/proyecto-1/foto.png">  ❌
```

### Problema: "GitHub Pages no muestra las imágenes"

**Causa:** Rutas absolutas en vez de relativas

**Solución:** NUNCA uses rutas como:
```html
<img src="C:/Users/James/Mi-Portafolio/projects/imagenes/foto.png">  ❌
```

SIEMPRE usa rutas relativas:
```html
<img src="imagenes/proyecto-1/foto.png">  ✅
```

---

## 💡 TIPS PROFESIONALES

1. **Nombres descriptivos:**
   - ✅ `dashboard-ventas-2024.png`
   - ❌ `imagen1.png`

2. **Optimiza las imágenes:**
   - Usa PNG para capturas de pantalla
   - Máximo 1920px de ancho
   - Comprime con tinypng.com

3. **Consistencia:**
   - Si un proyecto usa `dashboard-principal.png`
   - Otros deberían usar el mismo patrón
   - No mezcles `DashboardPrincipal.PNG` y `dashboard_main.jpg`

4. **Backup:**
   - Mantén todas tus imágenes originales en otra carpeta
   - Por si necesitas regenerarlas o editarlas

---

## 🎓 RESUMEN RÁPIDO

1. **Estructura de carpetas:**
   ```
   Mi-Portafolio/
   ├── portfolio-james-paz.html
   └── projects/
       ├── [tus proyectos].html
       └── imagenes/
           └── [nombre-proyecto]/
               └── [tus capturas].png
   ```

2. **Crear proyecto nuevo:**
   - Copia `PLANTILLA-proyecto.html`
   - Renómbrala
   - Crea carpeta en `imagenes/`
   - Edita contenido
   - Agrega a página principal

3. **Rutas de imágenes:**
   ```html
   <img src="imagenes/nombre-proyecto/imagen.png">
   ```

4. **Publicar:**
   - Sube todo a GitHub
   - Activa GitHub Pages
   - Listo!

---

**¿Necesitas ayuda con algo específico? ¡Pregúntame!**

**Versión:** 2.0  
**Fecha:** Febrero 2026  
**Creado para:** James Paz
