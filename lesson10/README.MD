# Оформлення сторінки
## Газета (декілька блоків)
Технології розвиваються по сходинках. І даже часто нові технології, спираються на нові. Наприклад, верстка інформації більше 200 років робилася в газетах.
<img src = "img/newspaper02.webp">  
По суті - сайт - це така собі інтерактивна газета.  
Технологія позиціонування елементів flexbox дозволяє розставити колонки.

<img src = "img/newspaper03.jpg">  

**index.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <div class="wrapper">
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
    </div>
</body>
</html>
```
**style.css**

```css
.wrapper{
    display: flex;
}
```

#### Завдання
1. Створіть сторінку з 2-х колонок.
2. Створіть сторінку з 4-х колонок.
3. Створіть сторінку з 5-х колонок.

### Вирівнювання по ширині.
В газеті ми бамичо, що текст вирівняний по ширині (ліва та права границі тексту будуть вериткальними лініями )
<img src = "img/newspaper05.jpg">  

Давайте реалізуємо це в нашій сторінці.  Змінемо лише файл **style.css**.
<img src = "img/newspaper04.jpg">  

```css
.wrapper{
    display: flex;
}
.d{
    text-align: justify;
}
```
Ми бачимо, що для нормального сприйняття тексту необхідний відступ від внутрішніх границь (від лівої та від правої).

<img src = "img/newspaper06.jpg">  

```css
.wrapper{
    display: flex;
}
.d{
    text-align: justify;
    padding-left: 10px;
    padding-right: 10px;
}
```

## Газета із заголовком
<img src = "img/newspaper07.jpg">  

Додамо заголовок. А також під заголовком проставимо дати виходу газети. Заголовок зробимо за допомогою тегу h1. А підзаголовок - розтягнемо по елементах за допомогою властивості **justify-content** зі значенням **space-around**.

**index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <div class="logo">
        <h1>New-York Times</h1>
    </div>
    <div class="underlogo">
        <div class="ul">VOL X....NO 2990.</div>
        <div class="ul">New-York Sanday, April 21, 1861</div>
        <div class="ul">Price two cents</div>
    </div>
    <div class="maintext">
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
    </div>
</body>
</html>
```

**style.css**
```css
.maintext, .underlogo, .logo{
    display: flex;
}
.logo{
    justify-content: center;
}
.underlogo{
    justify-content:space-around;
}
.maintext{

}
.d{
    text-align: justify;
    padding-left: 10px;
    padding-right: 10px;
}
```

### Властивості шрифту
Змінимо розмір заголовку, також зробимо текст із датою та номером газети заглавними літерами та жирним шрифтом.

<img src = "img/newspaper09.jpg">  

**style.css**
```css
.maintext, .underlogo, .logo{
    display: flex;
}
.logo{
    justify-content: center;
    font-size: 30px;
}
.underlogo{
    justify-content:space-around;
    text-transform: uppercase;
    font-weight: bold;
}
.maintext{

}
.d{
    text-align: justify;
    padding-left: 10px;
    padding-right: 10px;

}
```

## Границі та відступи.
<img src = "img/newspaper10.jpg">  
Додамо також границі (border) та відступи внутрішні (padding) та зовнішні (margin)

**style.css**
```css
.maintext, .underlogo, .logo{
    display: flex;
}
.logo{
    justify-content: center;
    border-bottom: 1px solid;
    font-size: 30px;
}
.underlogo{
    justify-content:space-around;
    text-transform: uppercase;
    font-weight: bold;
    margin-top: 2px;
    margin-bottom: 2px;
    border-top: 1px solid;
    border-bottom: 1px solid;
}
.maintext{
    border-top: 3px solid;
    padding-top: 5px;
}
.d{
    text-align: justify;
    padding-left: 10px;
    padding-right: 10px;
}
```
#### Додаткові завданя
Оберіть одну з газет та реалізуйте аналогічну структуру наступних газет:  
<img src = "img/newspaper.png">
<img src = "img/newspaper02.jpg">  

<img src = "img/newspaper12.jpg">  
<img src = "img/newspaper13.jpg">  
<img src = "img/newspaper14.jpg">  
<img src = "img/newspaper15.jpg">  
<img src = "img/newspaper16.jpg">  
<img src = "img/newspaper17.jpg">  
<img src = "img/newspaper18.jpg">  
<img src = "img/newspaper19.jpg">  
<img src = "img/newspaper20.jpg">  


## Додавання зображень
<img src = "img/newspaper11.jpg">  

Часто на газетних шпальтах можна побачити зображення.   


<img src = "img/newspaper21.jpg">  

**index.html**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <div class="logo">
        <h1>New-York Times</h1>
    </div>
    <div class="underlogo">
        <div class="ul">VOL X....NO 2990.</div>
        <div class="ul">New-York Sanday, April 21, 1861</div>
        <div class="ul">Price two cents</div>
    </div>
    <div class="maintext">
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. <img src = "img/newspaper21.png"> Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
        <div class="d">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam dolore quibusdam dicta nemo velit ratione officiis rem eligendi perferendis eveniet dolor tempore, quis ea nostrum odio eaque soluta sequi cupiditate.</div>
    </div>
</body>
</html>
```

```css
.maintext, .underlogo, .logo{
    display: flex;
}
.logo{
    justify-content: center;
    border-bottom: 1px solid;
    font-size: 30px;
}
.underlogo{
    justify-content:space-around;
    text-transform: uppercase;
    font-weight: bold;
    margin-top: 2px;
    margin-bottom: 2px;
    border-top: 1px solid;
    border-bottom: 1px solid;
}
.maintext{
    border-top: 3px solid;
    padding-top: 5px;
}
.d{
    text-align: justify;
    padding-left: 10px;
    padding-right: 10px;

}

```

## Загальне творче завдання
1. Створіть газету нашої освітньої групи (вигадайте заголовок разом).
2. Зробіть газету про свою сім'ю.
3. Зробіть газету про себе.
