# Entry 4
##### 3/9/25

### What Have I Done So Far?

The month in between this blog and the last blog has seen a lot of improvements the code. I am
still trying to learn Phaser because of its complexity and lack of explanations I can understand, but I think I have made good progress. My main issue from the last blog was the movement. I have figured this out and I dont think its something I need to worry about anymore. I have also figured out how to stretch the background image to fit the full screen. I used [this]
(https://phaser.discourse.group/t/how-to-stretch-background-image-on-full-screen/1839) thread to change my code from what I previously had. Ryan showed me his code and explained it to me, this was just the last piece I needed to make it work. Heres what I have written for this:
``` js
background.setPosition(this.sys.game.canvas.width/2 - 400,this.sys.game.canvas.height/ 2)
     const scaleX = 4 * this.sys.game.canvas.width/background.width
     const scaleY = this.sys.game.canvas.height/background.height
     const scale = (scaleX,scaleY)
    background.setScale(scale)  
```
The first line of code, `background.setPosition(this.sys.game.canvas.width/2 - 400,this.sys.game.canvas.height/ 2)` puts the background picture in the center of the canvas. For the x value, I subtracted 400 from the width of the canvas to align it better with the spawn-in area. Since the image isnt large enough to cover the whole canvas(despite the stretch), I think I have to put another picture next to it to continue the illusion. 
The scale variables set the scale for the background image. Without the `setScale`, the picture would only cover a small corner of the screen, and wouldnt extend past what I can see. Using this and combining it with another picture would fill up the whole canvas, giving me a background for the first scene. 

The camera has been a little bit tricky, and it has slowed my progress for the last week. Using the following code works, but it limits what I can see since the camera size is only the size of the original background picture.
``` js
this.cameras.main.setSize(background.width, background.height);
        this.cameras.main.startFollow(player);
        this.cameras.main.setZoom(1)
```
I have tried multiplying the x value by 2, but that only offsets the camera so that the player isnt in the middle anymore. I think I would still try to find more tutorials, but a lot of the popular ones are a little hard to follow. It could be something wrong with the way I set up my background images, so hopefully this issue will go away as I understand Phaser better.

### EDP

The Engineering Design process is a way to track your progress throughout a project. It goes from planning and testing, to building and improving upon a prototype. I am definitley still learning and experimenting with Phaser, but I am approaching the stage where I feel like I can make a proper game. Once I figure out how to use the camera and how to code attacks and enemies, I think I will be ready. 

### Skills I Learned

Over this month I feel like I have learned that I need to take multiple approaches to coding. If one thing doesnt work, I need to step back and try it again in a different way. Every thread I find about a certain topic may have a different method of achieving the same thing, especially since Phaser has so many complex ways to do things. A lot of it comes down to personal preference. I think I also need to understand the code that I find. For example, the [Phaser example page](https://phaser.io/examples/v3.85.0/camera/view/follow-offset) often shows the entire file instead of a specific chunk with an explantion. This leaves me with a vauge idea of how to use certain lines, such as the camera lines above, and I have to search places like Stack Overflow to figure out what it does. 

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)