# Entry 2
##### 12/16/25

### What Have I Done So Far?

Since the last blog, I have started up another "tutorial". I am kinda following the instructions on the official website, but I am trying to figure out what everything does and what the values mean
as I go, instead of just blindly copying it in. I try to work a little on it each day, and I really try to understand what is going on, especially with the erros which means progress is slow. For example, I was struggling with making the spritesheets and images appear properly, and it took me a while to figure what was happening.

```
     function preload ()
    {
        this.load.image('sky', 'assets/sky.png' { frameWidth: 32, frameHeight: 48 });
    }
     function create () {
        this.add.image(400, 300, 'sky');
     }
```
Here, the preload function loads everything in. The `this.load.image()` makes an image, which in this case is the background sky. I copied this from the tutorial and just replaced the name and filepaths to match what I had, but it still didnt work. This was because the `{ frameWidth: 32, frameHeight: 48 }` was messing it up. I figured this out when I [looked it up](https://stackoverflow.com/questions/72784307/how-to-set-character-frame-of-spritesheet-in-phaser-js) here. Sites like this and other forums have been very helpful into figuring things out. I have also been trying to comment the uses of everything so I can reference it again later when I start my real project. For example, on the `function preload ()` I have its function explained here:
```
// this.add.image is creating a new Image Game Object and adding it to the current Scenes display list. This list is where all of your Game Objects live. The 'sky' is the key (which can be named anything), and the following path is the access to actually load in the correct asset.
```
I actually used this to explain my issue earlier and once I restart, I know I will forget how to use it so comments like these will be very useful to me.

### Engineering Design Process

For my EDP stage, I think I am at a stage 2 right now. Since there arent really any problems I am solving (except bordeom maybe), I can just replace it with the development process. I am still only practicing and learning Phaser, and I havent really started to plan anything major except the basic concept since I am so focused on figuring out how I can use the framework. I think this will be the longest part of the early stages but I am trying to do it as quickly as I can without properly rushing so I have time to build something good.

### Skills I Learned

I think I learned that I am going to need a lot more patience than I did last year. Phaser is a lot more complicated and has plenty more places where I can go wrong than HTML frameworks such as Foundation did. It is also earlier in the year so I dont have the same amount of skill relative to what I did last year with HTML, so I need to take that into account. Rushing things wont help me at all despite its time benefits and I am struggling to realize that. I am often getting fustrated at my slow progress and I want to speed up, but whenever I do something always goes wrong and I cant figure it out. I think reading about it on the official Phaser Docs site or finding answers online definitley helps, but I also need to slow down and understand what I am writing and where I am writing it(since that seems to matter a lot now). I think this will be an ongoing thing throughout the year, especially since I dont approach other classes in this way.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
