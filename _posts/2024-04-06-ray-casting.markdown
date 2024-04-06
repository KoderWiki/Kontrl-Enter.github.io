---
layout: post
title: Raycasting
image: 8.jpg
date: 2024-04-06 11:16:20 +0200
tags: [coding,programming]
categories: game
---
Ray casting(광선 투사) 은 2차원의 맵에서 3차원의 원근감을 구현하기 위한 **렌더링 기법**이다. [WIKIPEDIA](https://en.wikipedia.org/wiki/Ray_casting)에서는 다음과 같이 적혀있다.
> Ray casting is the methodological basis for 3D CAD/CAM solid modeling and image rendering. It is essentially the same as ray tracing for computer graphics where virtual light rays are "cast" or "traced" on their path from the focal point of a camera through each pixel in the camera sensor to determine what is visible along the ray in the 3D scene.

[Ray tracing](https://en.wikipedia.org/wiki/Ray_tracing_(graphics))과는 비슷하지만 다르다. Ray tracing은 빛이 해당 물체의 표면에 닿은 후, 현실처럼 빛이 다시 반사되어 렌더링하는 방식인 반면, Ray casting은 해당 물체에 닿으면 일회성으로 사용되고 연산을 추가적으로 수행하지 않는다.

Ray casting의 원리를 이해하고 구현해보자.
***
### 개요1
Ray casting이 게임에 처음 활용된 곳이 바로 FPS게임이다. 90년대 초에 큰 인기를 끌었던 `Wolfenstein 3D`이 Ray casting을 이용한 가장 유명한 게임이다. 당시 컴퓨터성능으로는 3D게미을 상상조차 할수 없었기에 수학적 계산을 줄이기 위해 게임 공간은 2D로 구성되었고, 여기에 3D 같은 사실감을 주기 위해 Ray casting 기법을 사용했다.

###### Youtube

<iframe src="https://www.youtube.com/embed/iWowJBRMtpc" frameborder="0" allowfullscreen></iframe>
