[< Назад на главную страницу](/)
# GUI Анимации

В этом туториале я тебя научу как создавать анимации для игрового интерфейса

**Важно!** *Эта статья не до конца дописана.*

**Видео-Туториал:**

[Скоро](/luarbxstudio/guianims)

**Полная документация на английском:**

[https://developer.roblox.com/en-us/articles/GUI-Animations](https://developer.roblox.com/en-us/articles/GUI-Animations)

## Вступление

:TweenPosition и *:TweenSize (+ еще и *:TweenPositionAndSize) нужен для создания красивых анимаций

## Пример для *:TweenPosition
````lua
local object = script.Parent
object.AnchorPoint = Vector2.new(0.5, 0.5)
object.Position = UDim2.new(0.1, 0, 0.5, 0)
 
wait(2)
 
object:TweenPosition(UDim2.new(0.5, 0, 0.5, 0))
````

Выглядить это будет примерно так:

![tweenpos.png](/images/tweenpos.png)

## Пример для *:TweenSize
````lua
local object = script.Parent
object.AnchorPoint = Vector2.new(0.5, 0.5)
object.Position = UDim2.new(0.5, 0, 0.5, 0)
 
wait(2)
 
object:TweenSize(UDim2.new(0, 400, 0, 100))
````

Выглядить это будет примерно так:

![tweensize.png](/images/tweensize.png)

## Пример для *:TweenPositionAndSize
````lua
local object = script.Parent
object.AnchorPoint = Vector2.new(0.5, 0.5)
object.Position = UDim2.new(0.5, 0, 0.5, 0)
 
wait(2)
 
object:TweenSize(UDim2.new(0, 400, 0, 100))
````

## Дополнительная кастомизация

### Настройка анимации

| Direction | Description |
|---------|-----------|
| In | The tween will have less speed at its beginning and more speed toward its end. |
| Out | The tween will have more speed at its beginning and less speed toward its end. |
| InOut | In and Out on the same tween, with In at the beginning and Out taking effect halfway through. |
