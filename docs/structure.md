\# Структура проекта



\## 1. Сцены

\- SampleScene - пустая сцена, в ней только камера и свет

\- PlatformerDemo - сцена платформера: персонаж, платформы, трава, деревья на фоне



\## 2. Основная игровая сцена (PlatformerDemo)

Объекты на сцене:

\- Main Camera - камера

\- Managers - служебный объект

\- Lights - свет

&#x20; - Directional light - общий источник света

\- CharacterPlatformer - игрок

\- Scene - всё окружение уровня

&#x20; - TilemapGrid / Tilemap - сетка, из которой собраны платформы

&#x20; - TreeBackground - фон из деревьев (Tree1, Tree2, Tree3)

&#x20; - Grass - группа травы (11 штук: Grass, Grass (1) ... Grass (10))



Префабы:

\- CharacterPlatformer

\- TreeBackground

\- Grass (все 11 штук - копии одного префаба)



\## 3. Игрок (CharacterPlatformer)

Тег: Player. Это префаб.



Компоненты:

\- Transform - положение, поворот и размер объекта

\- Sprite Renderer - рисует картинку персонажа (спрайт Character\_0)

\- Animator - запускает анимации (контроллер CharacterAnimator)

\- Rigidbody 2D - физика: масса, гравитация, торможение (Body Type: Dynamic, Mass: 10)

\- Capsule Collider 2D - невидимая форма для столкновений (размер 0.4 x 1.3)

\- Player Character (Script) - главный скрипт игрока: движение, прыжок, здоровье

\- Character Anim (Script) - управляет анимациями персонажа

\- Character Hold Item (Script) - позволяет держать предметы в руке (объект Hand)



Что можно менять в Inspector (в Player Character):

\- Max\_hp - максимум здоровья (100)

\- Invulnerable - бессмертие (галочка)

\- Move\_accel, Move\_deccel, Move\_max - разгон, торможение и максимальная скорость

\- Can\_jump, Double\_jump - можно ли прыгать и двойной прыжок

\- Jump\_strength - сила прыжка (7)

\- Jump\_gravity, Jump\_fall\_gravity - гравитация при прыжке и падении

\- Can\_crouch - можно ли приседать

\- Reset\_when\_fall, Fall\_pos\_y, Fall\_damage\_percent - что будет, если упасть за уровень



\## 4. Скрипты

\- CarryItem.cs - позволяет переносить предметы (брать и бросать). Прикреплён к предметам, которые можно взять.

\- CharacterAnim.cs - включает нужную анимацию персонажа (бег, прыжок, приседание). Прикреплён к CharacterPlatformer.

\- CharacterHoldItem.cs - позволяет игроку держать предмет в руке. Прикреплён к CharacterPlatformer.

\- FollowCamera.cs - камера следует за игроком. Прикреплён к Main Camera.

\- Lever.cs - рычаг, который можно переключать (влево, вправо, выключен). Прикреплён к объекту-рычагу.

\- ParallaxBackground.cs - двигает фон (деревья) медленнее, чем игрока, чтобы получилась глубина. Прикреплён к фону.

\- PlayerCharacter.cs - главный скрипт игрока: бег, прыжок, приседание, здоровье, падение за уровень. Прикреплён к CharacterPlatformer.

\- PlayerControls.cs - хранит кнопки управления игроком (какие клавиши что делают).

\- TheAudio.cs - главный скрипт звука: запускает музыку и звуки. Прикреплён к служебному объекту.

