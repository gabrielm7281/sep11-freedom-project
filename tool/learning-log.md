# Tool Learning Log

## Tool: **Phaser**

## Project: **Hollow Knight Style Game**

---

### X/X/XX:
* Looked through Phaser documents
* Played a few games to get a sense for the style that I would need to use to make a game
* I started the tutorial that Phaser has, its a simple platformer where you collect starts

### 11/17/25:
* Monday:
    * Tried figuring out spritesheets using Craftpix.net
    * Imported a few spritesheets and tried to remake the config and setup fromt the Phaser tutorial (made a starter template file as well so that I dont forget how to do it)
* Tuesday:
    * I finally figured out how to display the background image. I had the correct preloading and image creation code, but for somereason there was a single line that messed everything up

    ```
     function preload ()
    {
        this.load.image('sky', 'assets/sky.png' { frameWidth: 32, frameHeight: 48 });
    }
     function create () {
        this.add.image(400, 300, 'sky');
     }
    ```
    Since I copied and pasted this section of code from the complete tutorial, it came with the `frameWidth/frameHeight`, and it turns out that this is for the [spritesheet  only](https://stackoverflow.com/questions/72784307/how-to-set-character-frame-of-spritesheet-in-phaser-js), which is why it was breking the image

* Thursday:
    * I am now trying to make platfirns and the ground, like in the tutorial. It seems a little complex, but I eventually figured it out. To make these solid platforms that I can later stand on, I have to add the Physics to make it solid, otherwise it is just a picture on the screen, which is what I now think `this.add.image` is. The [tutorial](https://phaser.io/tutorials/making-your-first-phaser-3-game/part3) wasnt very clear, and I noticed that it is not included in the later stages so I guess we just need to make it in a static body. You can do this by making a variable/group using: `var platforms = this.physics.add.staticGroup();` Since the `var platforms` is there, I can just write `platforms.create(x, y, key)` and it will make a solid platform to stand on.
    * Figuring this out was a bit tricky because the tutorial wasnt very clear about it, and I think it isnt really meant to be run, so there would be important stuff missing. If I just copied and pasted the code, it wouldnt work without a little bit of tweaking. For example, the key in `platform.create` was ground, but it needed to be `platforms`, at least for me. There were a bunch more small things like this where I got stuck
    * Next I want to try and get the spritesheet in so that there I can start jumping around. I dont think it should be too hard, but I think I would need to restructure a lot of stuff because the ZIP file is quite large.
* Friday: I tried to figure out the spritesheet, but for some reason I was getting even more errors using `{ frameWidth: 32, frameHeight: 48 }`. I think it might just be in the wrong place, and it is kinda hard to find things in the documentation
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
