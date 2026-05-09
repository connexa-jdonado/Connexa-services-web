# REGLAS DEL PROYECTO — CONNEXA SERVICES
# Claude debe leer este archivo antes de cualquier cambio

## DESIGN SYSTEM BLOQUEADO
Estos valores no se modifican bajo ninguna circunstancia:
- Color primario: #172554
- Color secundario: #F3F4F6
- Color acento: #71B136
- Tipografía headings: Plus Jakarta Sans
- Tipografía body: Inter

## REGLAS DE MODIFICACIÓN
1. Cada prompt modifica ÚNICAMENTE lo que se indica explícitamente
2. NUNCA tocar navbar ni footer salvo que se indique expresamente
3. NUNCA cambiar colores, tipografías ni espaciados existentes
4. NUNCA reorganizar secciones existentes
5. NUNCA eliminar contenido existente
6. Antes de cada cambio: leer el archivo afectado completo
7. Después de cada cambio: verificar que solo se modificó lo solicitado

## ARCHIVOS DEL PROYECTO
- index.html — Home
- productos.html — Landing productos
- fsmtool.html — Detalle FSMTOOL
- workflow-builder.html — Detalle Workflow Builder
- css/variables.css — Design tokens (NO MODIFICAR)
- css/base.css — Estilos base (NO MODIFICAR sin indicación)
- css/components.css — Componentes compartidos
- css/animations.css — Animaciones
- js/nav.js — Navbar
- js/animations.js — Intersection Observer
- js/carousel.js — Carrusel clientes
- assets/logos/ — Logos clientes
- assets/screenshots/ — Capturas productos
- assets/videos/ — Videos casos de uso

## PROTOCOLO ANTES DE CADA CAMBIO
1. Confirmar qué archivo se va a modificar
2. Confirmar qué sección específica se toca
3. Confirmar qué NO se va a tocar
4. Hacer el cambio
5. Reportar exactamente qué se modificó


## PROTOCOLO DE GIT — CONTROL DE VERSIONES
Antes de cualquier cambio ejecutar:
  git add .
  git commit -m "backup antes de: [descripción del cambio]"

Si algo sale mal ejecutar:
  git checkout -- .
  (esto revierte todos los cambios al último commit)

## PROTOCOLO DE BACKUP POR ARCHIVO
Antes de modificar cualquier archivo hacer una copia:
  cp index.html index.html.backup
Así si algo se rompe se restaura en segundos.

## SISTEMA BILINGÜE — OBLIGATORIO EN TODOS LOS CAMBIOS

El sitio es bilingüe ES/EN. Cada vez que se agregue
o modifique texto visible en cualquier archivo HTML:

1. Todo elemento de texto DEBE tener data-es y data-en:
   <span data-es="Texto en español" data-en="English text">
     Texto en español
   </span>

2. Nunca agregar texto hardcodeado sin sus dos atributos.

3. El JS de traducción ya está implementado en cada archivo.
   Solo agregar los atributos data-es y data-en correctamente.

4. Traducciones deben ser profesionales en inglés —
   no literales, adaptadas al contexto de negocio.

5. Al crear páginas nuevas incluir el selector ES/EN
   en la navbar y el JS de traducción completo.