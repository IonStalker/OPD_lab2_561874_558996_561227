**Описание сборки проекта**

**1\. Настройки сборки**

В Build Settings добавлены две сцены: PlatformerDemo и TopDownDemo. Включены обе, но файла сцены TopDownDemo в проекте нет, поэтому её лучше убрать из списка.

Доступные платформы:

- Windows (Standalone);
- Web (WebGL).

Выбрана, скорее всего, Windows, потому что она стоит по умолчанию. Development Build и отладка отключены, то есть это обычная сборка.

Другие настройки: название проекта OPD_LAB, версия 1.0, размер окна по умолчанию 1024×768, Color Space — Gamma, используется старый Input Manager.

**2\. Пакеты в Package Manager**

Сторонних пакетов (Cinemachine, TextMeshPro и т. д.) нет. Установлены:

- com.unity.ide.rider 3.0.38;
- com.unity.ide.visualstudio 2.0.26;
- com.unity.test-framework 1.8.0;
- com.unity.ext.nunit 2.1.0.

Кроме них подключены стандартные модули Unity (physics2d, tilemap, animation, audio, ui и другие), они идут вместе с редактором.

**3\. Структура папок и ассеты**

Все ассеты лежат в папке Assets/IndieMarc/PlatformerDemo. Внутри такие папки:

- Editor — один скрипт ImportPackage;
- Materials — материалы;
- Prefabs — префабы (персонаж, трава, рычаг, фон с деревьями);
- Scripts — 9 скриптов;
- Sprites — спрайты (фон, персонаж, рычаг);
- Tilemap — тайлы для уровня.

Также в проекте есть папки Packages и ProjectSettings, а ещё служебные Library, Temp, Logs и UserSettings, которые Unity создаёт сама.

Какие ассеты есть:

- спрайты: персонаж (2 файла), фон (5), рычаг (4), ещё 3 прочих;
- тайлы: 32 картинки и 17 Tile-ассетов, плюс палитра PlatformerPalette;
- материалы: 5 штук;
- анимации: 10 (Idle, Walk, Run, Jump, Fall, Crouch и другие) и один Animator Controller;
- звуков нет, у рычага есть AudioSource, но звук ему не назначен.

**4\. Размер проекта**

Папка Assets весит около 2 МБ, ProjectSettings и Packages меньше 1 МБ. Папка Library занимает около 159 МБ, это кэш, который Unity создаёт заново сама, поэтому в Git её не загружают. Всего проект на диске занимает примерно 163 МБ, а без Library — около 2–4 МБ.