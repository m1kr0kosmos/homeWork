<head>
    <style>
        .resBg {
            padding: 30px;
            background: url(image-asset.jpeg) no-repeat center center fixed; 
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
        }
    </style>
</head>
<body>
    <div class="resBg">GET EXCITED AND MAKE SOMETHING</div>
</body>


# -whoami 
#Will Boos


### AI21 Jurassic 1 Beta Test 0

<iframe width="560" height="315" src="https://www.youtube.com/embed/3I5qr1ej1Xs" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### Introduction to AI21

<iframe width="560" height="315" src="https://www.youtube.com/embed/RD0a7BCXgOQ" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>



### Quad Boot

<iframe width="560" height="315" src="https://www.youtube.com/embed/X3cLAE7X10Q" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe> 



### BSD Ricing

<iframe width="560" height="315" src="https://www.youtube.com/embed/F79bFRoAGpg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe> 



### Short paper on the Quake III Fast Inverse Square Root Algorithm


[fastInvSqRtAlgDynProg(3).pdf](https://github.com/mannequinSkywalker/projects-github.io/files/6651848/fastInvSqRtAlgDynProg.3.pdf)


### witchSLAM toy project (twitchSLAM-George Hotz)
```markdown
#!/usr/bin/env python3
import time
import cv2
import sdl2
import sdl2.ext
sdl2.ext.init()

W = 1920//2
H= 1080//2

window = sdl2.ext.Window("witch SLAM", size=(W,H), position=(-500,-500))
window.show()



def process_frame(img):
    img = cv2.resize(img, (W,H))

    events = sdl2.ext.get_events()
    for event in events:
        if event.type == sdl2.SDL_QUIT:
            exit(0)

    surf = sdl2.ext.pixels2d(window.get_surface())
    surf[:] = img.swapaxes(0,1)[:, :, 0]
    window.refresh()

if __name__ == "__main__":
    cap = cv2.VideoCapture("test1.mp4")

    while cap.isOpened():
        ret, frame = cap.read()
        if ret == True:
            process_frame(frame)
        else:
            break
```


#display.py


import sdl2
import sdl2.ext
sdl2.ext.init()

class Display(object):
    def __init__(self, W, H):
      sdl2.ext.init()

      self.W, self.H = W, H
      self.window = sdl2.ext.Window("witch SLAM", size=(W, H), position=(-500,-500))
      self.window.show()
      
    def paint(self, img):
    # junk
      events = sdl2.ext.get_events()
      for event in events:
        if event.type == sdl2.SDL_QUIT:
            exit(0)
    # draw
    surf = sdl2.ext.pixels3d(self.window.get_surface())
    surf[:, :, 0:3] = img.swapaxes(0,1) 
    
    # blit
    self.window.refresh()

```

![Github logo](78800556.png "Github logo")

(https://jekyllrb.com/)

