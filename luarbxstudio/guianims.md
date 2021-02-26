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

| Направление | Описание |
|---------|-----------|
| In | Анимация будет иметь меньшую скорость в начале и большую скорость в конце. |
| Out | Анимация будет иметь большую скорость в начале и меньшую скорость в конце. |
| InOut | In и Out для одной и той же анимации, с In в начале и Out, вступающими в силу в середине. |


| Стиль | Описание |
|-----|-----------|
| Linear | Moves at a constant speed. |
| Sine | Movement speed is determined by a sine wave. |
| Back | Tween movement backs into or out of place. |
| Quad | Eases in or out with quadratic interpolation. |
| Quart | Similar to Quad but with a more emphasized start and/or finish. |
| Quint | Similar to Quad but with an even more emphasized start and/or finish. |
| Bounce | Moves as if the start or end position of the tween is bouncy. |
| Elastic | Moves as if the object is attached to a rubber band. |
