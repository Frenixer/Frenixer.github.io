# Ник игрока и его аватар

В этом туториале я тебя научу как создавать текст с ником игрока или с его аватаром

**Видео:**

{% youtube /ZeB1yXo0BVY %}

## Ник игрока
Тут все легко, просто создаем **Local Script** в TextLabel пишем туда этот скрипт:
````lua
name = game.Players.LocalPlayer.Name
script.Parent.Text = name
````
**Name** обозначает то, что у локального (у игрока, у которого берется имя) скрипт спрашивает, какое значение стоит в переменной Name и после этого выводит значение переменной в значение Text, которое в TextLabel
## Аватар игрока
Пока что здесь ничего не написано, но можно посмотреть [это видео](https://youtu.be/ZeB1yXo0BVY) или посмотреть по ней документацию можно [здесь](https://developer.roblox.com/en-us/api-reference/function/Players/GetUserThumbnailAsync)
