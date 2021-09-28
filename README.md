# Human-Action-Recog-VIBE

VIBE : https://github.com/mkocabas/VIBE

video -> VIBE -> mesh sequence -> each person's action classification

## Dataset
UCF11, UCF Sports Action
https://www.crcv.ucf.edu/data/UCF101.php

### GT bboxes are changed for VIBE input.


Using UCF GT bbox (bad case)

https://user-images.githubusercontent.com/68524289/135082198-4b14430a-b920-4fa8-a305-4e65cfe7151d.mp4


Changed UCF GT bbox (same middle, max(height, width)

https://user-images.githubusercontent.com/68524289/135082220-54b2cbe4-db84-4032-aca9-89e4fa9fd4d3.mp4


Yolo-v3 GT bbox (estimated)

https://user-images.githubusercontent.com/68524289/135082158-c3bf540d-c8c9-4e3b-b252-10420425fdac.mp4


Using UCF GT bbox (bad case)

https://user-images.githubusercontent.com/68524289/135082364-7d38e930-db5e-4c1f-9a8d-5aa3cc6c3e2e.mp4


Changed UCF GT bbox (same middle, max(height, width)

https://user-images.githubusercontent.com/68524289/135082371-f58e133c-2fd4-4407-955d-ce29f221fae8.mp4


Yolo-v3 GT bbox (estimated)

https://user-images.githubusercontent.com/68524289/135082396-0aa1e45f-7a01-4e83-994f-da2a935ad375.mp4


addtional youtube video

## Class
stop / walk / run (classes can be added..)

stop class is trained by not only image sequence, but also single image.
