# 선 밑에서 위로
```
int y = 100;

void setup() {
  size(640, 360);  
  stroke(255);    
  frameRate(30);
}


void draw() { 
  background(0);  
  y = y - 1; 
  if (y < 0) { 
    y = height; 
  } 
  line(0, y, width, y);  
} 
```
# 초록 펜 만들기
```
void setup(){
  size(500,500);
  stroke(0,255,0);
  strokeWeight(16);
}
void draw(){
  if(mousePressed)
      line(pmouseX,pmouseY,mouseX,mouseY);  
}
```
# 영상 불러와서 회전시키기
```
PImage img;
void setup(){
size(500,500);
imageMode(CENTER);
img = loadImage("https://i.pinimg.com/originals/6b/5a/8c/6b5a8cc63ce660cd4dd0bc7752f31a98.png");
}
float f;
void draw(){
translate(mouseX, mouseY);
rotate(f); f+=0.1;
image(img,0,0, img.width>>2,
img.height>>2);
}
```
#
```
``` 
