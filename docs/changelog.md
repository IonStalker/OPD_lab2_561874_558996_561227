\## Изменения Сеньора

Я захотел изменить время на закат, для этого поменял цвета деревьев, изменил угол падения света, его интенсивность и цвет, так же добавил два объекта солнце и его ареол, привязанные к камере чтобы не двигались при движении игрока.

Список изменений:

&#x09;Деревья:

&#x09;	Sprites/Background/Trees1.mat (Color / Tint Color)(0.23, 0.12, 0.26)-тёмно-фиолетовый

&#x09;	Sprites/Background/Trees2.mat (Color / Tint Color)(0.45, 0.22, 0.36)-сливовый

&#x09;	Sprites/Background/Trees3.mat (Color / Tint Color)(0.70, 0.36, 0.42)-розово-красный

&#x09;	Градация цвета по дальности от солнца

&#x09;Освещение:

&#x09;	Lights/Directional light(Color)(1, 0.75, 0.53)- изменение цвета света

&#x09;	Lights/Directional light(Intensity)(1.3) - более сильный

&#x09;	Lights/Directional light(Rotation(X, Y, Z)(40, −60, 0) - меньше угол так как солнце заходит

&#x09;	Environment(Ambient Color)(0.36, 0.26, 0.38) - сиреневый по краям хз красиво

&#x09;Солнце:

&#x09;	Main Camera/Sun/Sprites/Circle.png(position (5.5, 3, 30), scale 2.2, light yellow color, Order in Layer −30) - создание солнца и его характеристики

&#x09;	Main Camera/SunGlow/Sprites/CircleBlur.png(position (5.5, 3, 31), scale 7, orange, semi-transparent (a = 0.55), Order in Layer −31) - создание ареола солнца и его характеристики



&#x09;камера:

&#x09;	Main Camera(Clear Flags)(Solid Color)-назначил скайбокс

&#x09;	Main Camera(Background)(0.98, 0.64, 0.45)-сменил цвет на закатный

&#x09;	Main Camera(Size (orthographic)(6)-отдалил камеру

&#x09;	

&#x09;	



