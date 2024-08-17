# Rain Shader
Create a rain shader by referring to [Ben Cloward tutorial](https://www.youtube.com/watch?v=fYGOZYST-oQ&list=PL78XDi0TS4lFlOVKsNC6LR4sCQhetKJqs&index=13)

## Demo

https://github.com/user-attachments/assets/34d88267-a452-4c0c-b7c6-ec9863acce33

## 1 Rain Wetness

### 1.1 Base color
Make the base color darker by using the negative *destaturated node*

Use *saturate node* to clamp the value between 0 and 1

Add the multiplication of *wet node* and *porousness node* as the α for interporlation

![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/571022f9-7d34-4242-ab1b-842f45eea23d)

### 1.2 Specular and Roughness

Use water specular and roughness value to interporlate with the material default value

Add *wet node* as the α for interporlation
![image](https://github.com/lanwenzhang/Learn-Unreal-Engine/assets/86000552/fcac4cb0-105b-4031-8b59-1a3dc4adaa1e)

## 2 Rain Drop
