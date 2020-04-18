# report 5-1
## 17학번 황근원

```
PGraphics pg;

void setup(){
  size(700,700);
  pg = createGraphics(700,700);
}

void draw(){
  background(250);
  drawa(pg, color(150,3,50));
  image(pg, 0,0);
}

void drawa(PGraphics pg, color col) {
  pg.beginDraw();
  pg.fill(col);
  pg. noStroke();
  if (mousePressed) pg.ellipse(mouseX, mouseY, 50, 50);
  pg.endDraw();

}
```
### comment
* PGraphics 의 예제 하나를 선택하고, 내용 중에 2개 이상을 변경하시오.
* 제가 못찾은 것일 수도 있으나 PGraphics 의 예제를 못찾곘습니다 ㅠㅜㅠㅜ
* 그래서 뭘 할까 생각하다 처음에 배운 펜그리기가 생각나서 PGraphics pg; 을 만들어 안에 그림을 그리는 것을 만들어 보았습니다.
* 그래픽스 수업 너무 재미있습니다! 하지만 제가 만들고자하는 것을을 만들기에 제 실력이 부족하다는 것을 매번 깨닫습니다ㅠㅜ 앞으로도 잘 부탁드립니다!
