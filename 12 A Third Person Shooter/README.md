# A Third Person Shooter

## Demo

https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/5faf3913-b10b-4b11-8e10-c7b5b39e181b

## 1 Animation
Use skeleton meshes and animation assets from [Mixamo](https://www.mixamo.com/#/). Choose "swat guy" as the player and name it "Old Lee". Choose "steve" as the AI enemy and name it "Soldier".

### 1.1 Blend Space and Animation Assets
There will be three modes for both player and AI enemy. For each mode, blend space is used to combine different animation assets: walk, go left, go right, run, etc. 

#### 1.1.1 Idle Mode
Horizontal axis is direction and vertical axis is speed

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/8075f59e-ffa0-40ee-bb81-78b81a301853)

#### 1.1.2 Rifle Mode
Horizontal axis is direction and vertical axis is speed

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/5b107ec7-6c56-4059-b0e5-e932e4748469)

#### 1.1.3 Fire Mode
Horizontal axis is direction and vertical axis is speed

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/364aad4a-c70d-4eb0-b589-042fd5e84c8d)


### 1.2 Animation blueprint
Use Blend poses by bool to determine the current mode

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/422fdde0-5a2c-431b-b87a-8332a111998b)

## 2 Gameplay
Create a blueprint for weapon and add two custom event "Shoot" and "Reload"

### 2.1 Shoot
Use "Multi Line Trace" for shoot function

Start location: get the pawn current location from setting owner of the weapon 

End location: multiply the forward vector of current location with the shooting range

Ignore the weapon owner in case that it is hitted by the line

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/be1d2b88-3149-48c9-9ef5-a244cc02a446)


### 2.2 Reload
If the current ammo is smaller than the max ammo and the mag is larger than zero. The ammo can be reload

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/a2a2beb8-fdf0-4b5e-bc96-40062e813953)

### 2.3 Health


## 3 Artificial Intelligence


## 4 UI
### 4.1 Menu
Create a widget blueprint "WBP Menu" for menu

#### 4.1.1 Place the menu widget in the starter level
Make the mouse cursor can be controlled and interacted with the widget

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/3794aad9-c18f-458d-9603-54f2efef574c)

#### 4.1.2 Play
Open the main level "Ice Road" when clicking "Play" button

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/0e9f27e5-3c4e-4ebf-b9de-855133b11ed1)

### 4.2 Player Info
Create a widget blueprint "WBP Game UI" for the player info will be displayed when picking up the weapon

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/96cd944c-b561-4a1d-8bb2-faae4904aa97)

#### 4.2.1 Sight
Put the sight icon on the center of screen for aiming

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/aaf23ef0-558b-4101-9e66-9ef4bb7e2c26)

#### 4.2.2 Health Bar
![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/eb456bf7-3b51-40da-9d6d-0ae1b9759381)

#### 4.2.3 Weapon Info
![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/bbc20b4b-923e-4469-b453-d803a90ac110)

#### 4.3 Enemy Info

## 5 Environment
### 5.1 Winter Scene
Download asset "Automotive Winter Scene" from Epic Game Marketplace and use it for the starter level and main level

### 5.2 Visual Effects
Create snow particle effects in Nigra

### 5.3 Sound
#### 5.3.1 Fire 


#### 5.3.2 Background Music
Use the BGM from famous Chinese TV series "Drawing Sword".


