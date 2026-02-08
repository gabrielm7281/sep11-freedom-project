# Entry 3
##### 2/6/25

### What Have I Done So Far?

Progress has been a little bit slow recently. For a very long time I was stuck on character movement. I tried multiple different ways of doing it, but many were complicated. Each time I looked at an online tutorial, such as [this one](https://youtu.be/KQ2FhPKBOHI?si=Tp-nnu_xiPjcpDQN), their method of making movement was different. In this one, he uses `this.cursorKeys = this.input.keyboard.createCursorKeys()` which records what button on the keyboard you press. He puts it into an if statement, which runs an animation and applies a set velocity to the sprite when it is pressed. This worked the best for me. The [Phaser tutorial](https://docs.phaser.io/phaser/getting-started/making-your-first-phaser-game#animations) also does it in a simalair way. However I still had issues with the code even though it *looked* correct. I noticed that neither the Phaser code or the Youtube tutorial code was written as `cursorsKeys`, which I was doing. Since it wasnt a variable, I needed to spell it exactly as it was on there, which fixed some of it. Then I changed the animation name but forgot to change it in the if statement. This caused a bunch of errors to pop up and I wasnt able to figure it out. After trying to fix the issue for a little while, I gave up and asked Mr. Mueller, who recommended to use an AI called Claude to spot the issue for me. It saw the two previous problems and I was able to fix it and have a moving character
, and using these tutorials I was able to mostly get there with:
``` js
this.cursorKeys = this.input.keyboard.createCursorKeys();

 this.anims.create({
        key: 'move',
        frames: this.anims.generateFrameNumbers("guy", { start: 0, end: 4 }),
        frameRate: 14,
        repeat: 0
    });

 if (this.cursorKeys.left.isDown)
        {
             player.setVelocityX(-160);

             player.anims.play('move', true);

        }
```
The first line of code gets the input. The second chunk is the animation. It runs 5 seperate frames at a rate of 14FPS which is what is needed for an animation to have a smooth look to it. The `repeat: 0` just means that the animation wont contiue after the "left" key is pressed. For some reason, Phaser set this at -1 in their example code. This makes it loop infinitley, which is not what I need. The third chunk checks if the left arrow key is down using Phaser syntax. If it is true, the player moves left and the "move" animation plays. The if statements will be repeated with each horizantal and vertical direction using the arrow keys.
Since I have got the movement down, I think I am going to try and create actual gameplay elements. I need to do this before we start making the actual game so I dont have to learn this on the fly. If possible, I would also like to figure out how to make different "scenes". This has been mentioned a few times throughout the docs  while I was trying to figure out movement, but I had always ignored it. I think it would be a good idea to incorporate it with the gameplay since I am limited with time and how much I can do in one "scene"

### EDP

In the Engineering Design Process, I am still reasearching and figuring out how to use Phaser. This will probably be the longest stage during the year since there needs to be a lot of experimentation and learning since its an entirely new platform. As mentioned previously, I still have a lot of important things to learn so it is a good idea to keep researching and practicing Phaser code. I already have a rough idea of what I want my actual game to be, but I need to learn how to get that idea onto a screen first.

### Skills I Learned

Since I spent so long on one thing, I learned how to use and look for anything to help me. I had used the Phaser documents, multiple different tutorials and I even dug through several different StackedOverflow forums. It has given me a lot of help with the smaller mistakes that I made, since a few of them were common beginner mistakes. I think this will also help me out in regular JS as well. I noticed it is getting a little more complex, and sites like [W3 Schools](https://www.w3schools.com/jsref/dom_obj_event.asp) have pretty detailed explanations and examples of almost everything. It is a good resource to have and use. I think this experience may improve my future Phaser experience as well. I think I will check spelling much more than I was previously, and I think I will also take my time and have several different approaches(case depending) in my head to figure out a specific problem.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
