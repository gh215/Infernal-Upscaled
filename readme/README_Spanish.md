Este mod reemplaza las texturas originales del juego **Indiana Jones and the Infernal Machine** con versiones mejoradas creadas mediante escalado por IA. El objetivo es mejorar la calidad visual del juego en pantallas modernas.

## ⚠️ Descargo de Responsabilidad / Aviso Importante

*   **Derechos:** Los activos originales y el juego Indiana Jones and the Infernal Machine son propiedad de sus respectivos titulares de derechos (Lucasfilm Games / Disney, etc.). No reclamo la propiedad de los materiales originales. Este mod es una obra derivada.
*   **Uso:** Este paquete de texturas se proporciona "tal cual" únicamente para uso personal y no comercial por parte de los fans del juego que posean una copia legal de Indiana Jones and the Infernal Machine.
*   **Responsabilidad:** Usas estas texturas bajo tu propio riesgo. El autor del mod no es responsable de ningún problema potencial con el juego o tu computadora.
*   **Distribución:** Cualquier uso comercial de estas texturas mejoradas está prohibido. Al distribuir el mod o sus versiones derivadas (si está permitido), debes acreditar al autor del escalado y mantener su naturaleza no comercial.
*   **Estado:** El autor del mod no está afiliado a los desarrolladores ni a los editores del juego.

---

## Contenido

*   [Requisitos](#requisitos)
*   [Preparación: Desempaquetar Recursos del Juego](#preparación-desempaquetar-recursos-del-juego)
*   [Instalación del Mod](#instalación-del-mod)
    *   [Paso 1: Instalando Texturas](#paso-1-instalando-texturas)
    *   [Paso 2: Instalando el Motor OpenJones3D (Requerido)](#paso-2-instalando-el-motor-openjones3d-requerido)
    *   [Paso 3: Parchando el Ejecutable (Downgrade)](#paso-3-parchando-el-ejecutable-downgrade)
    *   [Paso 4: Instalando dgVoodoo (Recomendado)](#paso-4-instalando-dgvoodoo-recomendado)
*   [Herramientas y Agradecimientos](#herramientas-y-agradecimientos)
*   [Enlaces Útiles](#enlaces-útiles)
*   [Opcional: Compilación Lista para Usar](#opcional-compilación-lista-para-usar)

---

## Requisitos

*   Una copia legal del juego **Indiana Jones and the Infernal Machine**.
*   **Recursos del juego desempaquetados.** Consulta la sección [Preparación](#preparación-desempaquetar-recursos-del-juego) a continuación.

---

## Preparación: Desempaquetar Recursos del Juego

Antes de instalar cualquier mod, incluido este, necesitas extraer (desempaquetar) los archivos del juego (archivos `.gob`) en la carpeta `Resource`.

**Hay dos formas principales de hacerlo:**

1.  **Método Manual:** Sigue las instrucciones detalladas en el GitHub de la comunidad Jones3D:
    [Instrucciones para Desempaquetar Recursos](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
    *(Este método requiere usar las utilidades `gobext` y `cndtool` de Urgon).*

2.  **Usando Indy3DModInstaller:** Usa la utilidad de the_kovic, que automatiza el proceso. Generalmente es más rápido y conveniente.
    *   Descarga: [Indy3DModInstaller](https://github.com/thekovic/Indy3DModInstaller)
    *   Ejecuta el instalador y sigue sus instrucciones para desempaquetar los recursos, como se describe en el *README* dentro del archivo descargado.

**Importante:** Después de desempaquetar, los archivos originales `CD1.gob`, `CD2.gob` y `JONES3D.gob` ya no serán utilizados directamente por el juego. En su lugar, el juego leerá archivos desde las carpetas dentro de `Resource`.

---

## Instalación del Mod

### Paso 1: Instalando Texturas

Una vez que los recursos del juego estén desempaquetados:

1.  **Descarga** el archivo comprimido que contiene mis texturas escaladas por IA desde este repositorio.
2.  **Elige un método de instalación:**
    *   **A través de Indy3DModInstaller:** Si estás usando este instalador, indícale la ruta del archivo de texturas descargado. Debería colocar los archivos correctamente.
    *   **Manualmente:** Extrae el archivo comprimido de texturas. Copia la carpeta `mat` del archivo comprimido en la carpeta `Resource` de tu juego, aceptando reemplazar los archivos cuando se te solicite.
3.  Una vez que hayas instalado con éxito las texturas, necesitas seleccionar un paquete de idioma de la carpeta `localizations` en el repositorio. Una vez que hayas elegido tu carpeta de idioma, todo lo que necesitas hacer es arrastrar y soltar todos los archivos en tu carpeta `Resource`.

### Paso 2: Instalando el Motor OpenJones3D (Requerido)

Lanzar el juego con recursos desempaquetados normalmente requiere el modo desarrollador (consulta "Toggle Dev Mod" en Indy3DModInstaller); de lo contrario, el juego pedirá el CD. Para evitar esto y obtener otras mejoras, es muy recomendable instalar **OpenJones3D**, un motor moderno de código abierto para el juego creado por Urgon.

1.  Ve a la página del repositorio de [OpenJones3D](https://github.com/smlu/OpenJones3D).
2.  Descarga la última versión (generalmente un archivo zip). O puedes descargar la última versión a través de `Releases`.
3.  **Extrae el contenido del archivo descargado** directamente en la carpeta `Resource` de tu juego, aceptando reemplazar los archivos.

### Paso 3: Parchando el Ejecutable (Downgrade)

OpenJones3D requiere que el ejecutable original del juego (`Indy3D.exe`) sea degradado a la versión 1.0.

1.  **Encuentra los archivos de downgrade:** Dentro de los archivos de este repositorio, debería haber una carpeta llamada `downgrade-file` que contiene archivos `.bps`. Descargarlos depende de dónde compraste el juego (`Steam` o `GOG`).
2.  **Ve al sitio web RomPatcher.js:** [https://www.marcrobledo.com/RomPatcher.js/](https://www.marcrobledo.com/RomPatcher.js/)
3.  En el campo "ROM file" (arriba), sube tu archivo **original** `Indy3D.exe` desde la carpeta `Resource` de tu juego.
4.  En el campo "Patch file" (abajo), sube el archivo de parche `.bps` descargado.
5.  Haz clic en el botón "Apply patch". El sitio te pedirá que descargues el archivo parcheado.
6.  **Guarda** el archivo descargado.
7.  **Renombra** el archivo parcheado descargado a `Indy3D.exe`.
8.  **Copia** este `Indy3D.exe` renombrado en la carpeta `Resource` de tu juego, **reemplazando** el archivo existente allí. *Puedes eliminar el antiguo `Indy3D.exe` o conservarlo como copia de seguridad.*

**⚠️ IMPORTANTE:** Asegúrate de que el archivo nuevo y parcheado se llame exactamente `Indy3D.exe` y esté ubicado en la carpeta **`Resource`**. De lo contrario, OpenJones podría no reconocerlo. Ahora deberías lanzar el juego a través de `Jones3D.exe` ubicado en la carpeta `Resource`.

### Paso 4: Instalando dgVoodoo (Recomendado)

Incluso con OpenJones, podrías experimentar largos tiempos de carga o congelaciones. Esto a menudo se resuelve usando el wrapper **dgVoodoo2**.

1.  **Descarga dgVoodoo2:** Desde el [sitio web oficial de dgVoodoo2](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/). Necesitas *dgVoodoo v2.86.1*.
2.  **Instala:** Sigue las instrucciones para instalar dgVoodoo para Infernal Machine. Hay una excelente guía disponible en la Comunidad de Steam:
    [Guía de Instalación de dgVoodooCpl](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
    *   *Brevemente: Copia `dgVoodooCpl.exe`, `dgVoodoo.conf` y los archivos de la carpeta `MS\x86` del archivo de dgVoodoo en la carpeta `Resource`.*
3.  **Configura:** Puedes usar mi archivo de configuración `dgVoodoo.conf`, que está incluido en la carpeta `dgvoodoocpl-config`; cópialo a la carpeta `Resource`, reemplazando el existente, o configura los ajustes tú mismo usando `dgVoodooCpl.exe`.

**Resultado:** Después de completar estos pasos, el juego debería lanzarse a través de `Jones3D.exe` (en la carpeta `Resource`), utilizará OpenJones3D, mostrará las texturas mejoradas y funcionará significativamente más rápido y de forma más estable gracias a dgVoodoo.

---

**⚠️ MUY IMPORTANTE:** Por favor, revisa la carpeta `ndy` en `Resource`, y si todavía hay archivos `.cnd`, tu mod solo funcionará al 0.1%, ya que el juego sigue usando las texturas antiguas de los archivos `.cnd`. Indy3DModInstaller desde la versión 2.2 permite extraer de forma segura y correcta los archivos `.cnd` a `.ndy`.

---

## Herramientas y Agradecimientos

Este mod y su instalación fueron posibles gracias a las siguientes herramientas y personas:

*   **Escalado:**
    *   Texturas Principales: [Phips/Upscaler](https://huggingface.co/spaces/Phips/Upscaler) en Hugging Face.
    *   Restauración Facial: [doevent/Face-Real-ESRGAN](https://huggingface.co/spaces/doevent/Face-Real-ESRGAN) en Hugging Face.
*   **Herramientas de Modding:**
    *   `cndtool`, `matool`, `gobext`: [Urgon (smlu)](https://github.com/smlu/Urgon) - utilidades indispensables para trabajar con los recursos del juego.
    *   `Indy3DModInstaller`: [the_kovic](https://github.com/thekovic) - un conveniente instalador de mods.
*   **Motor:**
    *   `OpenJones3D`: [Urgon (smlu)](https://github.com/smlu/OpenJones3D) - un motor moderno para ejecutar el juego.
*   **Gráficos y Compatibilidad:**
    *   `dgVoodoo2`: [Dege](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/) - un wrapper de DirectX para mejorar la compatibilidad y el rendimiento.

---

## Enlaces Útiles

*   [Desempaquetar Recursos del Juego (Docs Jones3D)](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
*   [Indy3DModInstaller (the_kovic)](https://github.com/thekovic/Indy3DModInstaller)
*   [Utilidades de Urgon (gobext, etc.)](https://github.com/smlu/Urgon)
*   [Motor OpenJones3D (Urgon)](https://github.com/smlu/OpenJones3D)
*   [RomPatcher JS (Parchador Online)](https://www.marcrobledo.com/RomPatcher.js/)
*   [dgVoodoo2 (Sitio Web)](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/)
*   [Guía de Instalación de dgVoodoo (Steam)](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
*   [Comunidad Jones3D - The Infernal Engine (Mods, Documentación)](https://github.com/Jones3D-The-Infernal-Engine)
*   [Corrección Arma a Dos Manos (Two Handed Weapon Fix)](https://github.com/thekovic/Indy3D-TwoHandFix)
*   [Recreación Fuentes HD (HD Fonts Recreation)](https://github.com/Jones3D-The-Infernal-Engine/Fonts-HD-recreation)

---

## Opcional: Compilación Lista para Usar

Para aquellos que quieran un juego completamente configurado con este mod, localización rusa, ReShade y una fuente HD mejorada, he preparado una configuración lista para usar de la carpeta `Resource`.

**Enlace:** [Carpeta Google Drive](https://drive.google.com/drive/folders/1aJIOP9-TznFZM4WOWVmuPFvCxx4Twzz2?usp=sharing)

**⚠️ IMPORTANTE:** La carpeta de Google Drive contiene dos subcarpetas:
1.  **`Resource_With_Custom_Level`**: Contiene todo lo mencionado anteriormente + un nivel personalizado adicional de la comunidad ([Nivel Original](https://github.com/Jones3D-The-Infernal-Engine/Mods)).
2.  **`Resource_Base`**: Contiene todo lo mencionado anteriormente sin el nivel extra.

**Instrucciones para la Compilación Lista para Usar:**
1.  Asegúrate de haber completado los pasos de [Preparación](#preparación-desempaquetar-recursos-del-juego) (desempaquetado de recursos) y [Parchado del EXE](#paso-3-parchando-el-ejecutable-downgrade).
2.  Descarga el contenido de una de las carpetas de Google Drive.
3.  Copia el contenido de la carpeta `Resource` descargada en la carpeta `Resource` existente de tu juego, reemplazando los archivos cuando se te solicite.