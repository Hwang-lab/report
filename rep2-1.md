#report 2-1
##안동대학교 황근원

``` 
void setup() {
  size(800, 300);
  textSize(100);
  fill(0);
  
}

int i;
int a=1;
int dir=1;

void draw() {
  background(0,255,255);
  text("Graphics", i=i+a, 200);
  if(i>300) i=0;
  if(i>width) dir=-1;
  if(i<0) dir=1;
  i = i+dir;
}
void keyPressed(){
  a = key-'0';
}
```
###comment
*처음 하는 건데 생각보다 잘 돼서 기분이 좋습니다!
*그래픽스 화이팅입니다~~!!
