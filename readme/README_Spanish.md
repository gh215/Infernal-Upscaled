Este mod reemplaza las texturas originales del juego **Indiana Jones and the Infernal Machine** con texturas mejoradas creadas mediante escalado por IA (AI upscaling). El objetivo es mejorar la calidad visual del juego en pantallas modernas. **Esta guía también cubrirá la instalación** de sonidos mejorados y el motor **moderno** OpenJones3D.

## ⚠️ Descargo de Responsabilidad (Disclaimer)

*   **Derechos:** Los assets originales y el juego Indiana Jones and the Infernal Machine son propiedad de sus respectivos titulares de derechos (Lucasfilm Games / Disney, etc.). No reclamo la propiedad de los materiales originales. Este mod es una obra derivada.
*   **Uso:** Este paquete de texturas se proporciona "tal cual" (as-is) exclusivamente para uso personal y no comercial por parte de los fans del juego que posean una copia legal de Indiana Jones and the Infernal Machine.
*   **Responsabilidad:** Utilizas estas texturas bajo tu propio riesgo. El autor del mod no se hace responsable de posibles problemas con el juego o tu ordenador.
*   **Distribución:** Se prohíbe cualquier uso comercial de estas texturas mejoradas. Al distribuir el mod o sus versiones derivadas (si se permite), es obligatorio indicar el autor del **escalado** y mantener su carácter no comercial.
*   **Estado:** El autor del mod no está afiliado a los desarrolladores o editores del juego.

---

## Contenido

*   [Requisitos](#requisitos)
*   [Preparación: Desempaquetado de los Recursos del Juego](#preparacion-desempaquetado-de-los-recursos-del-juego)
*   [Instalación del Mod](#instalacion-del-mod)
    *   [Paso 1: Instalación de Texturas](#paso-1-instalacion-de-texturas)
    *   [Paso 2: Instalación del Motor OpenJones3D (Necesario)](#paso-2-instalacion-del-motor-openjones3d-necesario)
    *   [Paso 3: Parcheo del Archivo Ejecutable (Downgrade)](#paso-3-parcheo-del-archivo-ejecutable-downgrade)
    *   [Paso 4: Instalación de dgVoodoo (Recomendado)](#paso-4-instalacion-de-dgvoodoo-recomendado)
    *   [Paso 5: Instalación de Sonido 3D (Recomendado)](#paso-5-instalacion-de-sonido-3d-recomendado)
    *   [Paso 6: Instalación de Sonidos Mejorados (Recomendado)](#paso-6-instalacion-de-sonidos-mejorados-recomendado)
    *   [Paso 7: Instalación de ReShade (Opcional)](#paso-7-instalacion-de-reshade-opcional)
*   [Herramientas y Agradecimientos](#herramientas-y-agradecimientos)
*   [Enlaces Útiles](#enlaces-utiles)
*   [Adicionalmente: Compilación Preconfigurada](#adicionalmente-compilacion-preconfigurada)

---

## Requisitos

*   Una copia legal del juego **Indiana Jones and the Infernal Machine**.
*   **Recursos del juego desempaquetados.** Consulta la sección [Preparación](#preparacion-desempaquetado-de-los-recursos-del-juego) más abajo.

---

## Preparación: Desempaquetado de los Recursos del Juego

Antes de instalar cualquier mod, incluido este, necesitas extraer (desempaquetar) **el contenido de los archivos del juego (`.gob` files) de la carpeta `Resource` a sus respectivas subcarpetas dentro de ella.**

**Hay dos formas principales de hacerlo:**

1.  **Método manual:** Sigue las instrucciones detalladas en el GitHub de la comunidad Jones3D:
    [Instrucciones para desempaquetar recursos](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
    *(Este método requiere el uso de las utilidades `gobext` y `cndtool` de Urgon).*

2.  **Usando Indy3DModInstaller:** Utiliza la utilidad de the_kovic, que automatiza el proceso. Esto suele ser más rápido y cómodo.
    *   Descargar: [Indy3DModInstaller](https://github.com/thekovic/Indy3DModInstaller)
    *   Ejecuta el instalador, siguiendo sus instrucciones indicadas en el *README*.

**Importante:** Después de desempaquetar, los archivos originales `CD1.gob`, `CD2.gob` y `JONES3D.gob` ya no serán utilizados directamente por el juego. En su lugar, el juego leerá los archivos de las carpetas dentro de `Resource`.

---

## Instalación del Mod

### Paso 1: Instalación de Texturas

Una vez que los recursos del juego estén desempaquetados:

1.  **Descarga** las carpetas `main-upscaled-textures` y `bmp-upscaled-textures` con texturas reescaladas por IA desde este repositorio.
2.  **Elige un método de instalación:**
    *   **Mediante Indy3DModInstaller:** Si utilizas este instalador, indícale la ruta a las carpetas de texturas descargadas. Debería colocar los archivos correctamente.
    *   **Manualmente:** Descomprime el archivo de texturas. Copia todos los archivos del archivo en la carpeta `mat` de tu juego, aceptando reemplazar los archivos cuando se te solicite.
3.  Después de instalar correctamente las texturas, necesitas elegir un paquete de idioma de la carpeta `localizations` en **este** repositorio. Una vez seleccionada la carpeta del idioma, solo tendrás que **copiar su contenido** en la carpeta `Resource`.

---

### Paso 2: Instalación del Motor OpenJones3D (Necesario)

El inicio estándar del juego con los recursos desempaquetados solo es posible en modo desarrollador (ver Toggle Dev Mod en Indy3DModInstaller), de lo contrario, el juego pedirá el disco. Para evitar esto, se recomienda encarecidamente instalar **OpenJones3D**, un motor moderno de código abierto para el juego creado por Urgon.

1.  Ve a la página del repositorio [OpenJones3D](https://github.com/smlu/OpenJones3D).
2.  Descarga la última versión (generalmente es un archivo zip). O puedes descargar la última versión a través de `Releases`.
3.  **Extrae el contenido del archivo descargado** directamente en la carpeta `Resource`, aceptando reemplazar los archivos.

**⚠️ ¡CUIDADO! ¡BUG!:** *No copies* el archivo `gen_fadeplate.3do` del archivo en la carpeta `Resource/mat` de tu juego. Este archivo puede causar un bug en el que los bordes de la pantalla mueven a tu Jones. No estoy bromeando, en uno de los niveles podría simplemente tirarlo abajo.

### Paso 3: Parcheo del Archivo Ejecutable (Downgrade)

---

OpenJones3D requiere que el archivo ejecutable original del juego (`Indy3D.exe`) sea degradado (downgraded) a la versión 1.0.

1.  **Encuentra los archivos para el downgrade:** En los archivos de este repositorio debería haber una carpeta `downgrade-file` que contiene archivos `.bps`. **La elección del archivo `.bps` correcto** depende de dónde compraste el juego (`Steam` o `GOG`).
2.  **Ve al sitio web RomPatcher.js:** [https://www.marcrobledo.com/RomPatcher.js/](https://www.marcrobledo.com/RomPatcher.js/)
3.  En el campo "ROM file" (arriba), carga tu archivo `Indy3D.exe` **original** de la carpeta `Resource`.
4.  En el campo "Patch file" (abajo), carga el archivo de parche `.bps` **correspondiente a la versión de tu juego**.
5.  Haz clic en el botón "Apply patch". El sitio te ofrecerá descargar el archivo parcheado.
6.  **Guarda** el archivo descargado.
7.  **Renombra** el archivo parcheado descargado a `Indy3D.exe`.
8.  **Copia** este `Indy3D.exe` renombrado en la carpeta `Resource`, **reemplazando** el archivo existente allí. *El antiguo `Indy3D.exe` se puede eliminar o guardar como copia de seguridad.*

**⚠️ IMPORTANTE:** Asegúrate de que el nuevo archivo parcheado se llame exactamente `Indy3D.exe` y esté ubicado en la carpeta `Resource`. De lo contrario, OpenJones3D podría no reconocerlo. Ahora puedes ejecutar el juego a través de `Jones3D.exe` desde la carpeta `Resource`.

---

### Paso 4: Instalación de dgVoodoo (Recomendado)

Incluso con OpenJones**3D**, puedes experimentar tiempos de carga largos o congelaciones. Esto a menudo se soluciona utilizando el wrapper **dgVoodoo2**.

#### Vía A:

1.  **Descarga dgVoodoo2:** Desde el sitio web oficial de [dgVoodoo2](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/). Necesitas la versión *dgVoodoo v2.86.1* (o una más nueva, si está disponible y es compatible).
2.  **Instala:** Sigue las instrucciones de instalación de dgVoodoo para Infernal Machine. Hay una excelente guía en Steam:
    [Guía de instalación de dgVoodooCpl](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
    *   *En resumen: Copia `dgVoodooCpl.exe`, `dgVoodoo.conf` (si tienes uno preconfigurado) y los archivos de la carpeta `MS\x86` del archivo de dgVoodoo en la carpeta `Resource`.*
3.  **Configura:** Puedes usar **mi** configuración `dgVoodoo.conf`, que se encuentra en la carpeta `dgvoodoocpl-config` de **este repositorio**, y copiarla en la carpeta `Resource` reemplazando la existente, o configurar los parámetros tú mismo a través de `dgVoodooCpl.exe`.

**Resultado:** Después de completar estos pasos, el juego debería iniciarse a través de `Jones3D.exe` (en la carpeta `Resource`), usar OpenJones3D, mostrar las texturas mejoradas y funcionar significativamente más rápido y de forma más estable gracias a dgVoodoo.

**⚠️ MUY IMPORTANTE:** En la **guía de Steam**, asegúrate de descargar y **copiar** el archivo `dinput.dll` en la carpeta `Resource`, de lo contrario tendrás problemas con el botón *Guardar* (sí, es el único botón que se comporta de manera muy extraña).

#### Vía B: Descarga todos los archivos, excepto las imágenes `PNG`, de la **carpeta `dgvoodoocpl-config` de este repositorio** y **cópialos** en la carpeta `Resource`.

---

### Paso 5: Instalación de Sonido 3D (Recomendado)

1.  **Descarga:** Desde la **carpeta principal de este repositorio**, descarga la carpeta `3D-sound` y **copia de allí los archivos necesarios (por ejemplo, `dsound.dll`, `dsoal-config.ini`)** en la carpeta `Resource` de tu juego.
2.  **Instala OpenAL:** Abre/descomprime el archivo `oalinst.zip` y ejecuta el instalador de OpenAL.

---

### Paso 6: Instalación de Sonidos Mejorados (Recomendado)

1.  **Descarga:** Desde la **carpeta principal de este repositorio**, descarga la carpeta `high-quality-sounds`.
2.  **Instala:** **Copia** todos los archivos de la carpeta `high-quality-sounds` en `Resource\sound` (deberían **reemplazarse** 1540 archivos).

**⚠️ DESCARGO DE RESPONSABILIDAD:** Durante la mejora del sonido se utilizó una IA **experimental** *'versatile_audio_super_resolution'*. No todos los archivos fueron procesados debido a interferencias terribles o silencio completo. Las bandas sonoras NO fueron procesadas por el mismo problema.

---

### Paso 7: Instalación de ReShade (Opcional)

1.  **Descarga la última versión de ReShade:** Desde el sitio web oficial de [ReShade](https://www.reshade.me/#download).
2.  **Instala:** Haz clic en el archivo de instalación y selecciona el archivo `Jones3D.exe` (la ruta debería ser algo así como: `ruta-a-la-carpeta-del-juego\Resource\Jones3D.exe`). Sin embargo, también puedes instalar ReShade en `Indy3D.exe`. **No se ha notado** una diferencia **sustancial**.
3.  **Selecciona:** De las *API de renderizado* que se te ofrecen, haz clic en DirectX 10/11/12.
4.  **Siguiente:** Puedes seleccionar los `fx` **a tu gusto** y después de la instalación empezar a jugar, o después de la instalación, descargar de **este repositorio** la carpeta `reshade` con shaders funcionales **probados por mí** y **copiar** la carpeta `reshade-shaders` en la carpeta `Resource` **SOLO** después de instalar el ReShade principal.

---

## Herramientas y Agradecimientos

Este mod y su instalación han sido posibles gracias a las siguientes herramientas y personas:

*   **Escalado de texturas:**
    *   Texturas principales: [Phips/Upscaler](https://huggingface.co/spaces/Phips/Upscaler) en Hugging Face.
    *   Restauración de caras: [doevent/Face-Real-ESRGAN](https://huggingface.co/spaces/doevent/Face-Real-ESRGAN) en Hugging Face.
*   **Herramientas de modding:**
    *   `cndtool`, `matool`, `gobext`: [Urgon (smlu)](https://github.com/smlu/Urgon) — utilidades indispensables para trabajar con los recursos del juego.
    *   `Indy3DModInstaller`: [the_kovic](https://github.com/thekovic) — un instalador de mods práctico.
*   **Motor:**
    *   `OpenJones3D`: [Urgon (smlu)](https://github.com/smlu/OpenJones3D) — un motor moderno para ejecutar el juego.
*   **Gráficos y Compatibilidad:**
    *   `dgVoodoo2`: [Dege](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/) — wrapper de DirectX para mejorar la compatibilidad y el rendimiento.
*   **Sonido 3D:**
    *   `OpenAL`: [OpenAL](https://openal.org/downloads/) — interfaz de programación de aplicaciones de audio multiplataforma.

---

## Enlaces Útiles

*   [Desempaquetado de recursos del juego (Jones3D Docs)](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
*   [Indy3DModInstaller (the_kovic)](https://github.com/thekovic/Indy3DModInstaller)
*   [Utilidades de Urgon (gobext y otros)](https://github.com/smlu/Urgon)
*   [Motor OpenJones3D (Urgon)](https://github.com/smlu/OpenJones3D)
*   [RomPatcher JS (Parcheador Online)](https://www.marcrobledo.com/RomPatcher.js/)
*   [dgVoodoo2 (Sitio Web)](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/)
*   [Guía de instalación de dgVoodoo (Steam)](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
*   [Comunidad Jones3D - The Infernal Engine (Mods, Documentación)](https://github.com/Jones3D-The-Infernal-Engine)
*   [Arreglo para armas a dos manos](https://github.com/thekovic/Indy3D-TwoHandFix)
*   **[Instrucciones para restaurar el sonido 3D (solo en ruso)](https://www.ixbt.com/live/games/kak-aktivirovat-eax-dlya-staryh-igr-v-windows-10.html)**

---

**⚠️ ¿Aún tienes preguntas?** [Únete al servidor de la Comunidad Indy3D](https://discord.gg/rhQfrWB)
