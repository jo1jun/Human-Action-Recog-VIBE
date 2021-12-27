# Human-Mesh-Action-Recognition(HMAR)


## Result video

https://user-images.githubusercontent.com/68524289/147467981-70d723c4-bacd-4023-87bc-2f2a0624a105.mp4

(The person in the video is me!)

## Dataset

some dataset have GT bboxes, the others have no GT boxes.
If GT bboxes exists, I used it.
Otherwise, I used estimated bbox by yolo-v3

1. UCF101, UCF Sports Action
https://www.crcv.ucf.edu/data/UCF101.php

2. KTH
https://www.csc.kth.se/cvap/actions/

3. Youtube Videos

## Class
Run / Punch / Squat

## Overall architecture

![image](https://user-images.githubusercontent.com/68524289/147469249-f6315345-72e4-4405-a3ba-0fe6dcdbf79f.png)

## Mesh sequence generator

VIBE : https://github.com/mkocabas/VIBE

VIBE can output pose&shape parameter (=SMPL parameter).

![image](https://user-images.githubusercontent.com/68524289/147469989-f7971b9c-e1f0-40d3-bf73-0911cf73755f.png)

If SMPL parameter feedforward to SMPL, Human mesh is generated.

## MLP architecture using pose sequence

![image](https://user-images.githubusercontent.com/68524289/147470242-38daf7d9-cd6e-490f-a545-969f6f3e8338.png)

Hyperparameters

Tensorboard

## Vision Transformer architecture using pose sequence

![image](https://user-images.githubusercontent.com/68524289/147470375-b9e64220-e2f4-4cee-986d-6014af8d3ce0.png)

Hyperparameters

Tensorboard

## Fatness Module

![image](https://user-images.githubusercontent.com/68524289/147470440-d14a669a-ea90-4e36-8362-d0f1a4bdfe32.png)

From the visualization, it seems that the first component explains for the change in height and the second represents the change in weight among human meshes.

(reference : https://khanhha.github.io/posts/SMPL-model-introduction/)

![image](https://user-images.githubusercontent.com/68524289/147470533-a6967be7-d93b-4fe3-b74e-9ea200a802ee.png)

The more thin, The bigger beta's second value. So, We can estimate fatness very roughly.

## Kcal Calc Module

This module calculate kcal using action per frame and fatness per video very roughly.
