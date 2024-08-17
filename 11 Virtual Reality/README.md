# Virtual Reality

## Demo

https://github.com/user-attachments/assets/5894edfa-2307-4c98-8f86-091cd344e518

## 1 Create a VR Pawn 

### 1.1 Create VR Blueprint

#### 1.1.1 Create A Character Blueprint
Since we want to use locomotion, so I choose character blueprint instead of pawn blueprint
![image](https://github.com/user-attachments/assets/ae0244b3-953d-4ba9-8cf2-f62e1521d9d8)

#### 1.1.2 Add camera component and motion controller
![image](https://github.com/user-attachments/assets/b8c572d7-1e9d-409f-9f19-14a03b27e006)

![image](https://github.com/user-attachments/assets/e8b1a342-0f79-4cfc-bb4a-3ac76aff9562)
![image](https://github.com/user-attachments/assets/7066e63a-74a3-4729-8c09-e8a716cfa6c6)


### 1.2 Add Locomotion

#### 1.2.1 Create Movement Input Action

![image](https://github.com/user-attachments/assets/9692767e-3e9d-4624-8309-667792126a1e)

![image](https://github.com/user-attachments/assets/b68a5166-2186-4fb6-b3fe-c1d8ed15e9a2)

![image](https://github.com/user-attachments/assets/dd2f124f-292e-4757-b73c-c46a168e4925)

#### 1.2.2 Mapping actions

![image](https://github.com/user-attachments/assets/f8d1e31f-74a3-4903-a576-518070cf967f)

### 1.2.3 Create locomotion blueprint 

![image](https://github.com/user-attachments/assets/1fa99dae-f1c9-4851-a3b8-823906c909e9)

## 2 Create a VR Menu

### 2.1 Create A Widget Blueprint for Menu

#### 2.1.1 Create a widget blueprint
![image](https://github.com/user-attachments/assets/5545588b-5854-47f4-8a07-096347feece6)

#### 2.1.2 Design the menu by adding buttons and texts
![image](https://github.com/user-attachments/assets/6d01fcb2-6c23-483d-b0a5-5a5cf63176d8)

#### 2.1.3 Add event on the button
![image](https://github.com/user-attachments/assets/7de40988-3ada-4fcb-85e2-9d179d67a1f5)

### 2.2 Trigger the menu in the action mapping
#### 2.2.1 Create input action for trigger the menu
![image](https://github.com/user-attachments/assets/b54576e5-e0ef-4891-8428-50652b26a219)

#### 2.2.2 Create input action for interaction with the menu
![image](https://github.com/user-attachments/assets/4c7215bf-56f2-4108-bdb0-cd9689ca3b87)

#### 2.2.3 Action mapping in the oculus
![image](https://github.com/user-attachments/assets/155b6656-94f0-4949-b691-1d8f33cc113f)


### 2.3 Create Widget Interaction for VR Pawn
#### 2.3.1 Create widget interaction left
![image](https://github.com/user-attachments/assets/f1020414-d27c-4870-85e9-5e23e112d11a)


#### 2.3.2 Create widget interaction right
![image](https://github.com/user-attachments/assets/2d2765e9-9f45-4619-be01-9b24e73d6188)

#### 2.3.3 Make the widget menu button interaction with oculus
![image](https://github.com/user-attachments/assets/dfad300c-471b-48e4-af24-44bcfd9d30cb)

### 2.4 Spawn the Menu
#### 2.4.1 Create a blueprint to spawn the widget blueprint
![image](https://github.com/user-attachments/assets/47d0fb5b-ec8b-4585-84f7-3ee313ed1498)
![image](https://github.com/user-attachments/assets/1ff14661-18af-43f4-bbed-d6caf51b13f5)

#### 2.4.2 Spawn the Menu when press Y on the left grip of oculus or press B on the right grip of oculus
![image](https://github.com/user-attachments/assets/a0deb1f8-2b50-4850-b40d-e38c69effb5f)

![image](https://github.com/user-attachments/assets/e5abbe14-21af-4f45-bd5d-ea68d7e4c4ae)

#### 2.4.3 Active the “interactive beam” when the menu is spawned
![image](https://github.com/user-attachments/assets/948d7e0b-90ca-4e99-9855-a48fa4d96d2b)

## 3 Locomotion Movement
### 3.1 Enhanced Input Mapping
#### 3.1.1 Enhanced input mapping
![image](https://github.com/user-attachments/assets/4c89fa61-f3f8-4137-a98c-5fe76659f66e)


#### 3.1.2 Movement blueprint
![image](https://github.com/user-attachments/assets/6512f3e2-7df8-4490-aa64-acbb368a3ba3)

### 3.2 Animation for VR hands
#### 3.2.1 Create animation blueprint for VR hands 
![image](https://github.com/user-attachments/assets/fee7f826-eafa-4321-b008-91a98266851b)

#### 3.2.2 Use Blend Space to make VR hands switch between open and closed
hands switch between open and closed = five figures switch between straight and curl
we use following three animation sequence from the template: 
![image](https://github.com/user-attachments/assets/dae7fbe1-acce-47b9-a459-b3b295f9fbd3)

Idle animation sequence: all the figures are straight
![image](https://github.com/user-attachments/assets/fcedf286-80d1-4f1b-bbfe-434e1351fe87)

Grasp animation sequence: four the figures curl
![image](https://github.com/user-attachments/assets/759b89d8-fad5-4441-97d6-751ce7c8da25)

Index curl animation sequence: index figure curl
![image](https://github.com/user-attachments/assets/ca5daa57-6064-4dc9-8d96-4204ec8bbab5)

Blend three animations
![image](https://github.com/user-attachments/assets/26c1d397-b5af-4ccc-be98-e490943755c4)

Mirror animation for the left hand
![image](https://github.com/user-attachments/assets/4e248d38-7082-4598-8cb2-c88a810483c9)

#### 3.2.3 Enhanced input mapping
![image](https://github.com/user-attachments/assets/e611e46d-d90e-463c-be19-e6601e1c956f)

#### 3.2.4 Add enhanced action blueprint and cast to hands animation blueprint
![image](https://github.com/user-attachments/assets/90e1ed7e-003d-4dbf-92d2-28933f4ae3d0)



