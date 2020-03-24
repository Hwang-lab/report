# Report 2-2
## 안동대학교 황근원

```
PFont f;
int h;
int a=1;
int dir=1;

void setup(){
  size(700,300);
  textSize(50);
  f = createFont("굴림",50);
  textFont(f);
}

void draw() {
  background(0,255,255);
  fill(0);
  text("안동대 컴공 사랑합니다♡", 70, h=h+a); 
  if(h>300) h=0;
  if(h>width) dir=-1;
  if(h<0) dir=1;
  h = h+dir;
}

void keyPressed(){
  a = key-'0';
}

```
### comment
* 처음엔 아니 좌우에서 상하로??? 어떻게 하지?? 라고 생각했지만 text 괄로 안의 숫자들의 역할을 안다면 누구나 할 수 있는 쉬운 문제였습니다!
* 잠시나마 고민했던 제가 바보처럼 느껴집니다ㅋㅋ. 좋은 수업 감사드리며 다음부터는 화상으로도 하면 좋겠습니다.!
* 화상에서 대답드리고 싶은데 옆에 세탁기 돌아가고 뒤에는 동생이 이상하게 쳐다봐서 못했습니다. 웃픈? 마음만은 알아주세요!
