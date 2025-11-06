# Entry 1
##### 11/3/25

### What am I doing this year?
For this years Freedom Project, I am using [Phaser](Phaser.io) to create a Hollow Knight style game. I got this idea around the release of Silksong, which was really popular. I liked the idea of it and its gameplay and I wanted to recreate it on my own, but with changes such as certain gameplay elements and make it much easier than the regular series.

In the beginning of the year, there isnt much progress on the game itself, and it is more about expirementing with the different framworks that were availible to us. I decided on Phaser for its large platform and game focused code. I saw that there had also been multiple popular Steam games made with Phaser(at least Partially), and I found that really cool. Last year, I feel like my idea and my Framework was kinda easy for the most part, so I decided to try and challenge myself this year. Phaser has a higher starting level, and making a quality game that I can really enjoy made it much more difficult for me and I think it will give me the challenge I want.

### What have I done so far?
Since it is still pretty early in the project, not much has happened. I experimented with a few other JS framworks such as React and Kaboom, but I decided on using Phaser for this project. To learn the basics of it, I followed the inbuilt [tutorial](https://phaser.io/tutorials/making-your-first-phaser-3-game/part1) that they have. They had me create a simple platformer where you can collect stars and earn points. I found the startup a little confusing and it wasnt explained very well, however I think I understand it well enough.

``` js
var config = {
    type: Phaser.AUTO,
    width: 800,
    height: 600,
    physics: {
        default: 'arcade',
        arcade: {
            gravity: { y: 300 },
            debug: false
        }
    },
```
The config enables everything to work and I think the type tag tells the system that it is a basic Phaser website. The width and height are self explanatory and I think the physics part sets it to an automatic arcade setting. Everything else was fairly straightforward and I was able to understand what the tutorial was saying. 

### Engineering Design Process
The engineering design process is a structure to follow that could help guide me through the year. It has 8 stages, from just thinking about a topic, to building it out, and finally sharing it to the world. I think I am just at stage 2 right now, which is Reasearching the topic. Since I am still just playing around with Phaser and trying to figure it out, I think that counts as reasearching.

### Skills I Learned
Since there wasnt really much happening in the early stages, I didnt learn too much. I think I understand the importance of practicing code so that I understand what I am writing. This is especially important since I will be using this tool all year and I need to make a whole game out of it. Doing this well help me out a lot later on since I have to start from scratch. 


[Next](entry02.md)

[Home](../README.md)
