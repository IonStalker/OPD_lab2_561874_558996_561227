Физические параметры:

&#x09;Глобальные настройки:

&#x09;	Гравитация (0, -9.81)

&#x09;	Velocity Iterations = 8

&#x09;	Position Iterations = 3

&#x09;	Fixed Timestep = 0.02

&#x09;Игрок:

&#x09;	Rigidbody2D: Dynamic, Mass = 10, Linear Drag = 1, Angular Drag = 1, Gravity Scale = 0, по z заморожена

&#x09;	CapsuleCollider2D(размером 0.4 ? 1.3)

&#x09;	Глобальная гравитация по игроку не работает. Для этого используется функция записывающая в rigid.linearVelocity:

&#x09;		jump\_gravity = 5 (подъём)

&#x09;		jump\_fall\_gravity = 20 (падение)

&#x09;		move\_max ? 2 (ограничение скорости)



Префабы:

&#x09;CharacterPlatformer(игрок):

&#x09;	Transform - положение, поворот и размер объекта

&#x09;	Sprite Renderer - рисует картинку персонажа (спрайт Character\\\_0)

&#x09;	Animator - запускает анимации (контроллер CharacterAnimator)

&#x09;	Rigidbody 2D - физика: масса, гравитация, торможение (Body Type: Dynamic, Mass: 10)

&#x09;	Capsule Collider 2D - невидимая форма для столкновений (размер 0.4 x 1.3)

&#x09;	Player Character (Script) - главный скрипт игрока: движение, прыжок, здоровье

&#x09;	Character Anim (Script) - управляет анимациями персонажа

&#x09;	Character Hold Item (Script) - позволяет держать предметы в руке (объект Hand)

&#x09;Grass(декор) - SpriteRenderer

&#x09;TreeBackground(фон с паралаксом) - MeshRenderer + ParallaxBackground.cs

&#x09;Lever(интерактивный объект (рычаг)) - BoxCollider2D (Is Trigger), AudioSource, Lever.cs



Опасности:

&#x09;Единственная реальная опасность — падение ниже fall\_pos\_y = -5. Тогда игрок теряет max\_hp ? fall\_damage\_percent (25 HP) и телепортируется на последнюю точку, где стоял на земле.

&#x09;В PlayerCharacter есть методы TakeDamage(), Kill() и событие onDeath. Враг или шипы делаются так: на объект вешают коллайдер-триггер и скрипт, который вызывает TakeDamage().

&#x09;Препятствия — это коллайдер тайлмапа на слое Platforms.



Интерфейса нет.



Что можно менять в Inspector:

&#x09;max\_hp (100), invulnerable.

&#x09;Движение: move\_accel (15), move\_deccel (20), move\_max (4).

&#x09;Прыжок: can\_jump, double\_jump, jump\_strength (7), jump\_time\_min (0.25) / jump\_time\_max (0.5), jump\_gravity (5), jump\_fall\_gravity (20), jump\_move\_percent (0.75, управляемость ввоздухе), ground\_layer, 	ground\_raycast\_dist (0.04).

&#x09;Присед: can\_crouch, crouch\_coll\_percent (0.65).

&#x09;Падение: reset\_when\_fall, fall\_pos\_y (-5), fall\_damage\_percent (0.25).

&#x09;PlayerControls - Поменять раскладку клавиш

&#x09;Запустить гравитацию для игрока

&#x09;(камера)FollowCamera: camera\_speed (3), target\_offset, границы уровня level\_left (-10) / level\_right (100) / level\_bottom (-5).

&#x09;(паралакс задника)ParallaxBackground: speed

&#x09;(весь проект)Project Settings: Gravity, Fixed Timestep, Time Scale

