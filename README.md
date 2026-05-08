
# My First Tutorial - Titherley

## Introduction
<div style="font-size:20px;">
Welcome to this Smartbots Tutorial!

In this game you will:
- Create your first **sprite**
- Learn how to **move** it with the controller
- Stop the sprite from leaving the screen

**Controls**
Use the arrow keys to move your sprite.

👉 Click **Next** to begin.
</div>

## Step 1
<div style="font-size:16px;">
Firstly, we are going to create a Sprite Character.

1. Drag a ``||variables:set mySprite to ||`` block from ``||Sprites:Sprites||``.

2. Click on the grey square to open the editor.

3. Draw your sprite
```blocks
let mySprite = sprites.create(img`
    5 3 3 5 3 3 3 3 3 3 3 3 5 5 3 5 
    3 5 5 5 3 3 3 3 3 3 3 3 3 5 5 3 
    3 5 5 3 3 3 3 3 3 3 3 3 3 5 5 3 
    5 5 3 5 3 3 3 3 3 3 3 3 5 3 5 5 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 5 5 5 5 5 5 5 5 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 5 5 5 3 3 3 
    3 3 3 3 5 5 5 5 5 5 5 5 5 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    `, SpriteKind.Player)
```
</div>

## Step 2
<div style="font-size:16px;">
Now we are going to make a way to control our Player

1. From the ``||controller:controller||`` menu place a ``||controller:controller.moveSprite(mySprite)||`` block to the bottom of the ``||loops:onstart||`` block.
```blocks
let mySprite = sprites.create(img`
    5 3 3 5 3 3 3 3 3 3 3 3 5 5 3 5 
    3 5 5 5 3 3 3 3 3 3 3 3 3 5 5 3 
    3 5 5 3 3 3 3 3 3 3 3 3 3 5 5 3 
    5 5 3 5 3 3 3 3 3 3 3 3 5 3 5 5 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 5 5 5 5 5 5 5 5 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 5 5 5 3 3 3 
    3 3 3 3 5 5 5 5 5 5 5 5 5 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
```
</div>

## Step 3
<div style="font-size:16px;">
Play the Game. You should now be able to move your sprite around the screen using the arrow keys. 

- Try going off the screen. Your character will disappear

- This is a bit frustrating. In the next step we will look at fixing this problem. 

</div>

## Step 4
<div style="font-size:16px;">
Let's make sure our player can't leave the screen. 

1. From the ``||Sprites:Sprites||`` menu place a ``||Sprites:mySprite.setStayInScreen(true)||`` block. 

2. Toggle the button to on. 

Your sprite will now stay inside the screen. 
```blocks
let mySprite = sprites.create(img`
    5 3 3 5 3 3 3 3 3 3 3 3 5 5 3 5 
    3 5 5 5 3 3 3 3 3 3 3 3 3 5 5 3 
    3 5 5 3 3 3 3 3 3 3 3 3 3 5 5 3 
    5 5 3 5 3 3 3 3 3 3 3 3 5 3 5 5 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 5 5 5 5 5 5 5 5 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 3 3 5 3 3 3 
    3 3 3 3 5 3 3 3 3 3 5 5 5 3 3 3 
    3 3 3 3 5 5 5 5 5 5 5 5 5 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    `, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setStayInScreen(true)
```
</div>

## Complete
<div style="font-size:18px;">
That's it. You now have a sprite that you can control with buttons, that stays in the screen. 
</div>

