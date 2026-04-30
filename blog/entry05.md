# Entry 5
##### 4/17/26

### What Have I Done So Far?

I was able to get the minimal game into place. It is very barebones and isnt much of a game, but it does technically work. Over a few days I was able to make way more progress than I thought I would be able to because of the amount of free time I had along with a little bit of time pressure. I think the biggest part of the game is the destroy function
```js
this.physics.add.overlap(player, enemy, function() {
        enemy.destroy()
        }, null, this);
```
It is pretty self explanatory, it destroys the enemey when it detects an overlap between the player hitbox and the enemy hitbox. I can put this into an if statement so that when the player presses the attack key, the enemy will be destroyed if there is an overlap. This allows the whole game idea to work. I was struggling to find a way to do this because I wasnt sure how to add the overlap. A lot of the tutorials/forums that I found looked very complicated and I didnt understand or have the time to understand it, so I was very confused. One of the places where I didnt look was the original [tutorial](https://phaser.io/tutorials/making-your-first-phaser-3-game/part8). It has a simalair mechanic where the player has to collect stars (Which disappear when the player hitbox overlaps with the star hitbox), and it included the `.overlap` code, which I used in my own code.

I also created a new animation that runs when the attack key (Z) is pressed down to show when the attack is happening. This wasnt too difficult and I was able to find it in the Phaser docs. `this.attackKey = this.input.keyboard.addKey("Z")` I had already made movement keys with CursorKeys (arrow keys), but this needed .addKey("key"). I put in an if statement saying: When this key is pressed, play the new attack animation and check for an overlap with the enemy (And destroy if true). 
``` js
if(this.attackKey.isDown){
    player.anims.play('attack', true);
    this.physics.add.overlap(player, enemy, function() {
    enemy.destroy()
    }, null, this);
        }
```
This works fine for what I need it to do. All of the other code was taken from my previous experimentation code with some different values/file paths so it didnt take too long and wasnt a challenge. 

I also finally got the animations in for both the player and the enemy. I got the file from craftpix.net and imported it into a spritesheet [generator](https://spritesheetgenerator.online), which packs it into a png I can use. This has been missing and I think it looks a lot better like this. I also adjusted the hitboxes to make more sense, because previously the sprite would be standing on air. It is much smaller now and is less clunky. I changed it with the same method: `sprite/image.body.setSize(400, 400)`. When I do this, the hitbox might not be in the right place, so I found an offset command: `player.body.setOffset(792, 300)`. This centers it on the player so that it isnt in some random place anymore. To get the spritesheet to work and display properly, I needed to change the `frameWidth/Height`, otherwise it would sort of sidescroll through the sprites and display all the blank space. I didnt know about this and I think it wouldve taken way too long to figure out so I asked an ai about it, and it helped me with the new values. Once I got the animation working, I realized that the running animation only went in one direction. [Phaser](https://docs.phaser.io/phaser/concepts/gameobjects/components#flip-vs-scale) can flip a spritesheet using `flipX`, and this fixed it. I remembered this from one of the LowPolyPrincess tutorials I saw. The tricky thing with this is that I originally wrote `player.flipX`, which doesnt do anything on its own but I didnt know because I saw it a while ago. In the docs it said that it was actually a boolean value, so `player.flipX = true` was what I actually needed. Some stuff might still be a little bit off but everything should be functional now. 

### EDP

For the Engineering Design Process, I think I am at stage 6. I am testing out the functionality of everything I wrote, and I understand the code a lot better. It is more or less ready to play, it just needs some more enemies and a few things in the beyond MVP list and it should be ready.

### Skills I Learned 

I think I learned how to properly use AI during the last few weeks. Previously I was a bit hesitant to use it and I still try hard not to use it. However I think it is good to ask so that you can understand the code and to get inspiration. I used it to check the feasability of my ideas such as having the player destroy the enemy when Z is pressed. It said it is possible and gave me some random code: 
``` js
// In create(), add an animation complete listener:
player.on('animationcomplete', function(anim) {
    if (anim.key === 'attack') {
        isAttacking = false;
        attackCooldown = false;
    }
});
```
I didnt understand it and it didnt make any sense, and definitley wouldnt of worked in my code so I tried to do it my own way, which is what is being used now. I knew that there would be other ways to achieve the same thing so I tried not to listen to it or follow its message. 

I think it is also good to help out with repetitive tasks that you dont fully understand. For example, when I was doing the frame widths for the spritesheets, I had no idea what to do with it. I had only done it a few times before since I took it from the tutorial, and it didnt look very good. When I first wrote the new spritesheet in, it wouldnt show at all so I asked Claude why it happened. It said the frameWidth/Height needed to be a specific number, and it did the math (Takes columns/width = frameWidth and rows/height = frameHeight). I took the math and kept redoing it until I had all of my spritesheets in. This wouldve taken hours on my own but it took a few minutes here. I dont think this is unethical AI usage and these two examples were one of the very few times I actually used and implemented what the AI said. 

[Project Preview](https://gabrielm7281.github.io/sep11-freedom-project/)

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)