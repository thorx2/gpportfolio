---
title: "Cheat Sheet for UPROPERTY"
date: 2023-10-19T19:53:33+05:30
draft: false
author: "Gaudham"
tags:
  - Unreal Engine
  - C++
  - example
image: /images/ue-aspec.png
description: ""
toc: false
mathjax: false
---

#### UPROPERTY macro simplified

How about a quick cheat sheet for the [UPROPERTY](https://docs.unrealengine.com/5.3/en-US/unreal-engine-uproperties/) macro to help you quickly figure out
which one to use.

|            |     Default      |      Instance      |      Event Graph    |
|------------|------------------|--------------------|---------------------|
| Read Only  |VisibleAnywhere    |VisibleAnywhere      |   BluePrintReadOnly |
| Read Only  |VisibleDefaultOnly |VisibleInstanceOnly  |   BluePrintReadOnly |
|------------------|------------------------------|-----------------------------------|---------------------------------|
| Read Write |EditAnywhere      |EditAnywhere        |   BluePrintReadWrite|
| Read Write |EditDefaultsOnly  |EditInstanceOnly    |   BluePrintReadWrite|


Checkout the following code snippets for a quicker breakdown:

```C++
private:
  UPROPERTY(EditDefaultsOnly, BlueprintReadOnly, Category = "Tank Parameters", meta = (AllowPrivateAccess = "true"))
  float TankSpeed = 5.0f;
```
Breakdown:
  * TankSpeed is a float variable which should be the same for all the tanks in the game, hence use __`EditDefaultsOnly`__
  * It is __`BlueprintReadOnly`__ since it should not be manipulated via Blueprints.
  * `meta` Allows access to the variable as it was initial declared in the __`private`__ section.
