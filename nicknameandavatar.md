[Назад на главную страницу](Frenixer.github.io)
# Ник игрока и его аватар

В этом туториале я тебя научу как создавать текст с ником игрока или с его аватаром

**Видео-Туториал:**

[https://youtu.be/ZeB1yXo0BVY](https://youtu.be/ZeB1yXo0BVY)

**Полная документация на английском:**

[https://developer.roblox.com/en-us/api-reference/function/Players/GetUserThumbnailAsync](https://developer.roblox.com/en-us/api-reference/function/Players/GetUserThumbnailAsync)

## Ник игрока
Тут все легко, просто создаем **Local Script** в TextLabel пишем туда этот скрипт:
````lua
name = game.Players.LocalPlayer.Name
script.Parent.Text = name
````
**Name** обозначает то, что у локального (у игрока, у которого берется имя) скрипт спрашивает, какое значение стоит в переменной Name и после этого выводит значение переменной в значение Text, которое в TextLabel
## Аватар игрока
Тут все тоже легко, просто также создаем **Local Script** в ImageLabel пишем туда этот скрипт:
````lua
local player = game.Players.LocalPlayer
 
local userId = player.UserId -- Достает из переменной значение ID игрока
local thumbType = Enum.ThumbnailType.HeadShot -- Здесь можно указать другой тип
local thumbSize = Enum.ThumbnailSize.Size420x420 -- Можно изменить размер картинки на другой, а именно на: 48x48, 60x60, 100x100, 150x150, 180x180, 353x353, 420x420
local content, isReady = Players:GetUserThumbnailAsync(userId, thumbType, thumbSize) -- если все готово
 
local imageLabel = script.Parent
imageLabel.Image = content -- Изменяет обычную картинку на аватар игрока
imageLabel.Size = UDim2.new(0, 420, 0, 420) -- Изменять в зависимости от того, какой параметр выбран в ThubnailSize
````
**Все типы картинок 'Enum.ThumbnailType':**
- 'AvatarBust' - Голова и чуть-чуть туловище

- 'AvatarThumbnail' - Аватар полным размером

- 'HeadShot' - Только голова и лицо

Все разрешения картинок 'Enum.ThumbnailSize':
 - Маленькие: 48x48, 60x60

 - Средние: 100x100, 150x150, 180x180
 
 - Большие: 353x353, 420x420
