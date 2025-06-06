Этот мод заменяет оригинальные текстуры игры **Indiana Jones and the Infernal Machine** улучшенными текстурами, созданными с помощью ИИ-апскейлинга. Цель — повысить визуальное качество игры на современных дисплеях. **Также в рамках этого руководства будет рассмотрена установка** улучшенных звуков и **современного** движка OpenJones3D.

## ⚠️ Дисклеймер

*   **Права:** Оригинальные ассеты и сама игра Indiana Jones and the Infernal Machine являются собственностью их правообладателей (Lucasfilm Games / Disney и т.д.). Я не претендую на владение оригинальными материалами. Этот мод является производной работой.
*   **Использование:** Данный пакет текстур предоставляется «как есть» (as-is) исключительно для личного, некоммерческого использования фанатами игры, которые владеют легальной копией Indiana Jones and the Infernal Machine.
*   **Ответственность:** Вы используете эти текстуры на свой страх и риск. Автор мода не несет ответственности за возможные проблемы с игрой или вашим компьютером.
*   **Распространение:** Запрещается любое коммерческое использование этих улучшенных текстур. При распространении мода или его производных версий (если разрешено) обязательно указывайте автора **апскейлинга** и сохраняйте некоммерческий характер.
*   **Статус:** Автор мода не связан с разработчиками или издателями игры.

---

## Содержание

*   [Требования](#требования)
*   [Подготовка: Распаковка ресурсов игры](#подготовка-распаковка-ресурсов-игры)
*   [Установка мода](#установка-мода)
    *   [Шаг 1: Установка текстур](#шаг-1-установка-текстур)
    *   [Шаг 2: Установка движка OpenJones3D (Необходимо)](#шаг-2-установка-движка-openjones3d-необходимо)
    *   [Шаг 3: Патчинг исполняемого файла (Downgrade)](#шаг-3-патчинг-исполняемого-файла-downgrade)
    *   [Шаг 4: Установка dgVoodoo (Рекомендуется)](#шаг-4-установка-dgvoodoo-рекомендуется)
    *   [Шаг 5: Установка 3D звука (Рекомендуется)](#шаг-5-установка-3d-звука-рекомендуется)
    *   [Шаг 6: Установка улучшенных звуков (Рекомендуется)](#шаг-6-установка-улучшенных-звуков-рекомендуется)
    *   [Шаг 7: Установка ReShade (Опционально)](#шаг-7-установка-reshade-опционально)
*   [Инструменты и Благодарности](#инструменты-и-благодарности)
*   [Полезные ссылки](#полезные-ссылки)
*   [Дополнительно: Готовая сборка](#дополнительно-готовая-сборка)

---

## Требования

*   Легальная копия игры **Indiana Jones and the Infernal Machine**.
*   **Распакованные ресурсы игры.** См. раздел [Подготовка](#подготовка-распаковка-ресурсов-игры) ниже.

---

## Подготовка: Распаковка ресурсов игры

Прежде чем устанавливать какие-либо моды, включая этот, вам необходимо извлечь (распаковать) **содержимое игровых архивов (`.gob` файлы) из папки `Resource` в соответствующие подпапки внутри неё.**

**Есть два основных способа это сделать:**

1.  **Ручной способ:** Следуйте подробной инструкции на GitHub сообщества Jones3D:
    [Инструкция по распаковке ресурсов](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
    *(Этот метод требует использования утилит `gobext` и `cndtool` от Urgon).*

2.  **С помощью Indy3DModInstaller:** Используйте утилиту от the_kovic, которая автоматизирует процесс. Это обычно быстрее и удобнее.
    *   Скачать: [Indy3DModInstaller](https://github.com/thekovic/Indy3DModInstaller)
    *   Запустите программу установки, следуя её инструкциям, указанным в *README*.

**Важно:** После распаковки оригинальные файлы `CD1.gob`, `CD2.gob` и `JONES3D.gob` больше не будут использоваться игрой напрямую. Вместо них игра будет читать файлы из папок внутри `Resource`.

---

## Установка мода

### Шаг 1: Установка текстур

После того как ресурсы игры распакованы:

1.  **Скачайте** папку `main-upscaled-textures` и `bmp-upscaled-textures` с AI-апскейленными текстурами из этого репозитория.
2.  **Выберите способ установки:**
    *   **Через Indy3DModInstaller:** Если вы используете этот инсталлятор, укажите ему путь к скачанным папкам с текстурами. Он должен корректно разместить файлы.
    *   **Вручную:** Распакуйте архив с текстурами. Скопируйте все файлы из архива в папку `mat` вашей игры, соглашаясь на замену файлов при появлении запроса.
3.  После успешной установки текстур вам нужно выбрать языковой пакет из папки `localizations` в **этом** репозитории. Выбрав папку с языком, вам останется только **скопировать её содержимое** в папку `Resource`.

---

### Шаг 2: Установка движка OpenJones3D (Необходимо)

Стандартный запуск игры с распакованными ресурсами возможен только в режиме разработчика (см. Toggle Dev Mod в Indy3DModInstaller), иначе игра будет просить диск. Чтобы обойти это, настоятельно рекомендуется установить **OpenJones3D** — современный открытый движок для игры от Urgon.

1.  Перейдите на страницу репозитория [OpenJones3D](https://github.com/smlu/OpenJones3D).
2.  Загрузите последнюю версию (обычно это zip-архив). Или вы можете скачать последнюю версию через `Releases`.
3.  **Извлеките содержимое скачанного архива** прямо в папку `Resource`, соглашаясь на замену файлов.

**⚠️ ОСТОРОЖНО! БАГ!:** *Не копируйте* файл `gen_fadeplate.3do` из архива в папку `Resource/mat` вашей игры. Этот файл может вызывать баг, при котором границы экрана двигают вашего Джонса. Я не шучу - на одном из уровней его может просто скинуть вниз.

### Шаг 3: Патчинг исполняемого файла (Downgrade)

---

OpenJones3D требует, чтобы оригинальный исполняемый файл игры (`Indy3D.exe`) был понижен (downgraded) до версии 1.0.

1.  **Найдите файлы для даунгрейда:** В файлах этого репозитория должна быть папка `downgrade-file`, содержащая файлы `.bps`. **Выбор нужного `.bps` файла** зависит от того, где вы купили игру (`Steam` или `GOG`).
2.  **Перейдите на сайт RomPatcher.js:** [https://www.marcrobledo.com/RomPatcher.js/](https://www.marcrobledo.com/RomPatcher.js/)
3.  В поле «ROM file» (сверху) загрузите ваш **оригинальный** файл `Indy3D.exe` из папки `Resource`.
4.  В поле «Patch file» (снизу) загрузите **соответствующий вашей версии игры** `.bps` файл патча.
5.  Нажмите кнопку «Apply patch». Сайт предложит скачать пропатченный файл.
6.  **Сохраните** скачанный файл.
7.  **Переименуйте** скачанный пропатченный файл в `Indy3D.exe`.
8.  **Скопируйте** этот переименованный `Indy3D.exe` в папку `Resource`, **заменив** существующий там файл. *Старый `Indy3D.exe` можно удалить или сохранить как бэкап.*

**⚠️ ВАЖНО:** Убедитесь, что новый, пропатченный файл называется именно `Indy3D.exe` и находится в папке `Resource`. Иначе OpenJones3D может его не распознать. Теперь вы можете запускать игру через `Jones3D.exe` из папки `Resource`.

---

### Шаг 4: Установка dgVoodoo (Рекомендуется)

Даже с OpenJones**3D** вы можете столкнуться с долгими загрузками или фризами. Это часто решается использованием враппера **dgVoodoo2**.

#### Путь А:

1.  **Скачайте dgVoodoo2:** С официального сайта [dgVoodoo2](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/). Вам нужна версия *dgVoodoo v2.86.1* (или более новая, если доступна и совместима).
2.  **Установите:** Следуйте инструкции по установке dgVoodoo для Infernal Machine. Отличное руководство есть в Steam:
    [Руководство по установке dgVoodooCpl](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
    *   *Кратко: Скопируйте `dgVoodooCpl.exe`, `dgVoodoo.conf` (если есть готовый) и файлы из папки `MS\x86` архива dgVoodoo в папку `Resource`.*
3.  **Настройте:** Вы можете использовать **мою** конфигурацию `dgVoodoo.conf`, которая расположена в папке `dgvoodoocpl-config` **этого репозитория**, и скопировать ее в папку `Resource` с заменой, или настроить параметры самостоятельно через `dgVoodooCpl.exe`.

**Результат:** После выполнения этих шагов игра должна запускаться через `Jones3D.exe` (в папке `Resource`), использовать OpenJones3D, отображать улучшенные текстуры и работать значительно быстрее и стабильнее благодаря dgVoodoo.

**⚠️ ОЧЕНЬ ВАЖНО:** В **стимовской инструкции** обязательно скачайте и **скопируйте** в папку `Resource` файл `dinput.dll`, иначе у вас будет проблема с кнопкой *Сохранить* (да, это единственная кнопка, которая ведёт себя очень странно).

#### Путь Б: Скачайте все файлы, кроме `PNG` картинок, из **папки `dgvoodoocpl-config` этого репозитория** и **скопируйте** их в папку `Resource`.

---

### Шаг 5: Установка 3D звука (Рекомендуется)

1.  **Скачайте:** Из **главной папки этого репозитория** скачайте папку `3D-sound` и **скопируйте оттуда необходимые файлы (например, `dsound.dll`, `dsoal-config.ini`)** в папку `Resource` вашей игры. `[Уточните, какие именно файлы или всё содержимое папки 3D-sound нужно копировать. Фраза "два файла Resource" неясна. Если oalinst.zip там же, то укажите это.]`
2.  **Установите OpenAL:** Откройте/распакуйте архив `oalinst.zip и запустите установщик OpenAL.

---

### Шаг 6: Установка улучшенных звуков (Рекомендуется)

1.  **Скачайте:** Из **главной папки этого репозитория** скачайте папку `high-quality-sounds`.
2.  **Установите:** Все файлы из папки `high-quality-sounds` **скопируйте** в `Resource\sound` (должно **замениться** 1540 файлов).

**⚠️ ДИСКЛЕЙМЕР:** Во время улучшения звука использовался **экспериментальный** ИИ *'versatile_audio_super_resolution'*. Не все файлы были обработаны из-за ужасных помех или полной тишины. Саундтреки НЕ были обработаны из-за той же проблемы.

---

### Шаг 7: Установка ReShade (Опционально)

1.  **Скачайте последнюю версию ReShade:** С официального сайта [ReShade](https://www.reshade.me/#download).
2.  **Установите:** Кликните на установочный файл и выберите файл `Jones3D.exe` (путь к нему должен быть примерно такой: `путь-к-папке-с-игрой\Resource\Jones3D.exe`). Однако, можно поставить ReShade и на `Indy3D.exe`. **Существенной** разницы **не замечено**.
3.  **Выберите:** Из предложенных вам *rendering API* кликните на DirectX 10/11/12.
4.  **Дальше:** Вы можете выбрать `fx` **по вкусу** и после установки начать играть, либо после установки скачать из **этого репозитория** папку `reshade` с оттестированными **мной** рабочими шейдерами и **скопировать** папку `reshade-shaders` в папку `Resource` **ТОЛЬКО** после установки основного ReShade.

---

## Инструменты и Благодарности

Этот мод и его установка стали возможны благодаря следующим инструментам и людям:

*   **Апскейлинг текстур:**
    *   Основные текстуры: [Phips/Upscaler](https://huggingface.co/spaces/Phips/Upscaler) на Hugging Face.
    *   Восстановление лиц: [doevent/Face-Real-ESRGAN](https://huggingface.co/spaces/doevent/Face-Real-ESRGAN) на Hugging Face.
*   **Инструменты для моддинга:**
    *   `cndtool`, `matool`, `gobext`: [Urgon (smlu)](https://github.com/smlu/Urgon) — незаменимые утилиты для работы с ресурсами игры.
    *   `Indy3DModInstaller`: [the_kovic](https://github.com/thekovic) — удобный установщик модов.
*   **Движок:**
    *   `OpenJones3D`: [Urgon (smlu)](https://github.com/smlu/OpenJones3D) — современный движок для запуска игры.
*   **Графика и Совместимость:**
    *   `dgVoodoo2`: [Dege](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/) — враппер DirectX для улучшения совместимости и производительности.
*   **3D звук:**
    *   `OpenAL`: [OpenAL](https://openal.org/downloads/) — кроссплатформенный интерфейс программирования приложений для работы с аудиоданными.

---

## Полезные ссылки

*   [Распаковка ресурсов игры (Jones3D Docs)](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
*   [Indy3DModInstaller (the_kovic)](https://github.com/thekovic/Indy3DModInstaller)
*   [Утилиты Urgon (gobext и др.)](https://github.com/smlu/Urgon)
*   [OpenJones3D Engine (Urgon)](https://github.com/smlu/OpenJones3D)
*   [RomPatcher JS (Онлайн-патчер)](https://www.marcrobledo.com/RomPatcher.js/)
*   [dgVoodoo2 (Сайт)](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/)
*   [Руководство по установке dgVoodoo (Steam)](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
*   [Сообщество Jones3D - The Infernal Engine (Моды, Документация)](https://github.com/Jones3D-The-Infernal-Engine)
*   [Фикс для двуручного оружия](https://github.com/thekovic/Indy3D-TwoHandFix)
*   **[Инструкция для возвращения 3D звука (только на русском)](https://www.ixbt.com/live/games/kak-aktivirovat-eax-dlya-staryh-igr-v-windows-10.html)** `[Добавил квадратные скобки для корректного форматирования ссылки]`

---

**⚠️ Остались вопросы?** [Заходите на сервер Indy3D Community](https://discord.gg/rhQfrWB)

---

## Дополнительно: Готовая сборка

Для тех, кто хочет получить полностью настроенную игру с этим модом, русской локализацией, ReShade и улучшенным HD-шрифтом, я подготовил готовую конфигурацию папки `Resource`.

**Ссылка:** [Google Drive Папка](https://drive.google.com/drive/folders/1aJIOP9-TznFZM4WOWVmuPFvCxx4Twzz2?usp=sharing)

**⚠️ ВАЖНО:** На Google Drive находятся две папки:
1.  `Апск. текст. + рус. лок. + улуч. звук + 3D звук DSOAL + Доп. Уровень`: Содержит **всё, что** указано в названии + дополнительный кастомный уровень от сообщества ([Оригинал уровня](https://github.com/Jones3D-The-Infernal-Engine/Mods)).
2.  `Апск. текст. + рус. лок. + улуч. звук + 3D звук DSOAL`: Содержит всё вышеперечисленное без дополнительного уровня.

**Инструкция для готовой сборки:**
**⚠️ ВАЖНО:** Игра модифицировалась на платформе GOG: я не могу предсказать, как поведёт себя игра в Steam. Будьте осторожны и делайте бэкапы.
1.  **(Рекомендуется) Сделайте резервную копию вашей оригинальной папки `Resource`.**
2.  Удалите **существующую** папку `Resource` из корневой папки **игры**.
3.  Скачайте содержимое одной из папок с Google Drive. **Это будет папка `Resource` (или архив, содержащий её).**
4.  **Скопируйте скачанную папку `Resource`** в корневую папку игры.
