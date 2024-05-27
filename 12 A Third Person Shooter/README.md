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

Link the weapon with character animation: If the character pick up the weapon, the rifle mode will be triggered. Besides, the weapon is attached to the character.

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/848c93b2-3464-4cfb-80f8-d50b421cebc1)


If the character shoot, the fire mode will be triggered. After 3 seconds, it goes back to the rifle mode.

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/7d62dc52-6f5b-4587-a6d8-d66b129480c4)

### 2.2 Reload
If the current ammo is smaller than the max ammo and the mag is larger than zero. The ammo can be reload

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/a2a2beb8-fdf0-4b5e-bc96-40062e813953)


### 2.3 Health
Each ammo that hits on the character can cause ten decrements on the health. 

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/fa757adb-903d-44ec-8984-b3bc01817095)


The maximum health is 100. If the health is equal to zero, the character will die.

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/9370cb8b-5483-4805-aad1-02232b51be99)


## 3 Artificial Intelligence
Enemy character is controlled by AI controller. With the behavior tree, they are able to wander, chase and shoot the player.

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/797a1e8a-9988-4545-89c6-5a478c9fe7bd)

### 3.1 Wander

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/bd3362fd-e7c1-4d91-8bbe-f6ef47373f0a)

### 3.2 Chase

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/7e10414a-10da-4b48-8e7b-b4fc558dfd38)


### 3.3 Shoot

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/abb175cd-b0c6-44e8-8959-10e0f305a7c3)


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

Set the text as a variable and link it with the character blueprint

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/c46c4d14-4342-44dd-a77a-f8b987b021c5)

#### 4.2.3 Weapon Info
![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/bbc20b4b-923e-4469-b453-d803a90ac110)

Set the text as a varaiable and link it with weapon blueprint

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/aa66c480-f3c9-4e1d-be73-67db02c3b82c)

#### 4.3 Enemy Info
Create another widget blueprint for enemy health bar

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/73c5ddb0-8bd6-4941-8ba4-bf45fe5a315d)

Link it with the character blueprint

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/1fd71e4c-6fe6-4a29-83a0-912a65b63e94)


## 5 Environment
### 5.1 Winter Scene
Download asset "Automotive Winter Scene" from Epic Game Marketplace and use it for the starter level and main level

### 5.2 Visual Effects
#### 5.2.1 Snow
Create snow effects by using the "fountain particle effect". The parameter is as follows:

Make it falling by using negative values

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/a01bb3a6-b025-4932-b2a1-5b39873003f5)

Increase the spawn rate

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/929cf920-65ff-435b-95d8-106ff9f5e446)

Increase the lifecyle

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/a8721eb3-2521-46ab-b77f-8bd6899b7448)

### 5.2.2 Fire Effect
![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/873d8f7b-75e7-4198-8180-5bb34ce08a85)

### 5.3 Sound
#### 5.3.1 Fire Sound
![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/59316147-3e6c-4a06-a1b5-3693aec1dfbb)

#### 5.3.2 Background Music
Use the BGM from famous Chinese TV series "Drawing Sword".

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/150f8c4b-72fa-4f42-94aa-1f545cc1b134)


