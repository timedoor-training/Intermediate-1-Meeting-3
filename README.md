# Timedoor Training Teen
## Intermediate A - Meeting 3

Pertemuan 3 mempelajari input/output dan juga bagaimana event listener dapat digunakan untuk menerima inputan, contoh aplikasi yang akan dibuat:

>timedoor-event-keyboard.netlify.app

untuk memulai pembuatan aplikasi download terlebih dahulu di dalam repo
>https://github.com/timedoorAcademy-smp/int1-3-eventKeyboard



###  HTML Code Basic

```html
<body>
    <h2>Event in Javascript</h2>
    <br>

    <input type="text" id="field" placeholder="Type here">
    <p id="status"></p>

    <img width="60%" src="img/keyboard.PNG" id="key">

    <p>Game key: <br>
        w for move up <br>
        a for move left<br>
        s for move down<br>
        d for move right<br>
        space for shoot the enemy</p>
</body>
```

### Javascript Basic
```html
<script>
    var key_pressed = document.getElementById('field');
    var keyid = document.getElementById('key')

    key_pressed.addEventListener("keydown", onKeyDown)
    key_pressed.addEventListener("keyup", onKeyUp)
    key_pressed.addEventListener("keypress", onKeyPress)

    function onKeyPress(event) {
        if (event.code == "Space") {
            document.getElementById("status").innerHTML = 'Sprite shoot the enemy';
            keyid.src = 'img/hitEnemy.PNG'
        }
    }

    function onKeyDown() {
        if (event.key == "w" || event.key == "W") {
            document.getElementById("status").innerHTML =
                'Sprite move up';
            keyid.src = 'img/up.PNG'
        } else if (event.key == "s" || event.key == "S") {
            document.getElementById("status").innerHTML =
                'Sprite move down';
            keyid.src = 'img/down.PNG'
        } else if (event.key == "d" || event.key == "D") {
            document.getElementById("status").innerHTML =
                'Sprite move right';
            keyid.src = 'img/right.PNG'
        } else if (event.key == "a" || event.key == "A") {
            document.getElementById("status").innerHTML =
                'Sprite move left';
            keyid.src = 'img/left.PNG'
        } else {
            document.getElementById("status").innerHTML =
                'Sprite doesnt move'
            keyid.src = 'img/keyboard.PNG'
        }
    }

</script>
```

## Do it Your Self!



### Javascript Challenge
```html
<script>
    function onKeyUp(event) {
        if (event.key == "w" || event.key == "W") {
            document.getElementById("status").innerHTML =
                'Sprite stops move up';
            keyid.src = 'img/keyboard.PNG';
        } else if (event.key == "s" || event.key == "S") {
            document.getElementById("status").innerHTML =
                'Sprite stops move down';
            keyid.src = 'img/keyboard.PNG';
        } else if (event.key == "d" || event.key == "D") {
            document.getElementById("status").innerHTML =
                'Sprite stops move right';
            keyid.src = 'img/keyboard.PNG';
        } else if (event.key == "a" || event.key == "A") {
            document.getElementById("status").innerHTML =
                'Sprite stops move left';
            keyid.src = 'img/keyboard.PNG';
        } else {
            document.getElementById("status").innerHTML =
                'Sprite doesnt move'
            keyid.src = 'img/keyboard.PNG'
        }
        // key s or S
        // key a or A
        // ky d or D
        // Else
    }
```