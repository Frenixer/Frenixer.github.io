[< Назад на главную страницу](/)
# GUI Анимации

В этом туториале я тебя научу как создавать анимации для игрового интерфейса

**Видео-Туториал:**

[Скоро](/luarbxstudio/guianims)

**Полная документация на английском:**

[https://developer.roblox.com/en-us/articles/GUI-Animations](https://developer.roblox.com/en-us/articles/GUI-Animations)

## Вступление

*:TweenPosition и *:TweenSize (еще и *:TweenPositionAndSize) нужен для создания красивых анимаций

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
| Linear | Двигается с одной и той же скоростью. |
| Sine | Скорость движения определяется синусоидой. |
| Back | Движение анимации возвращается на свое место или выходит из него. |
| Quad | Облегчает вход или выход с помощью квадратичной интерполяции. |
| Quart | Подобно Quad, но с более подчеркнутым началом и / или финишем. |
| Quint | Подобно Quad, но с еще более подчеркнутым началом и / или финишем. |
| Bounce | Движется так, как если бы начальное или конечное положение анимации было как мячик. |
| Elastic | Двигается так, как будто объект прикреплен к резинке. |


![styles](https://dk135eecbplh9.cloudfront.net/assets/blt164bc3fd53630e3a/Easingstyle.gif)

````lua
local object = script.Parent
object.AnchorPoint = Vector2.new(0.5, 0.5)
object.Position = UDim2.new(0.1, 0, 0.5, 0)
 
wait(2)
 
object:TweenPosition(UDim2.new(0.5, 0, 0.5, 0), "Out","Quint")
````

### Время

Обычно, оно длиться ``1`` секунду, но можно добавить число и будет оно длиться сколько вы задали

````lua
local object = script.Parent
object.AnchorPoint = Vector2.new(0.5, 0.5)
object.Position = UDim2.new(0.1, 0, 0.5, 0)
 
wait(2)
 
object:TweenPosition(UDim2.new(0.5, 0, 0.5, 0), "Out","Quint",3)
````

### прерывание анимации

По умолчанию оно стоит на ``false``, но можно изменить на ``true``, и тогда если уже tween выполняется, то можно будет ее прервать

````lua
local object = script.Parent
object.AnchorPoint = Vector2.new(0.5, 0.5)
object.Position = UDim2.new(0.1, 0, 0.5, 0)
 
wait(2)
 
object:TweenPosition(UDim2.new(0.5, 0, 0.5, 0), "Out","Quint",3, true)
````
