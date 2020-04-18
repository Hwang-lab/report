# report 5-2
## 17학번 황근원

```
void setup() {
  size(700, 700);
}

float f;

void draw() {
  background(100);
  translate(mouseX, mouseY);
  scale (0.7);  // 축소
  rotate (270);  // 회전
  
  stroke(255);
  strokeWeight(3);  // 선 굵기
  
  fill(0, 0, 15);  // 봉 만들기
  beginShape();
  vertex(-3, 25);
  vertex(3, 25);
  vertex(3, 100);
  vertex(-3, 100);
  endShape(CLOSE);

  rotate(sin(f));  // 별 회전시키기
  f = f + 0.15;
  
  fill(255, 255, 15);  // 별 만들기
  beginShape();
  vertex(0, -50);
  vertex(14, -20);
  vertex(47, -15);
  vertex(23, 7);
  vertex(29, 40);
  vertex(0, 25);
  vertex(-29, 40);
  vertex(-23, 7);
  vertex(-47, -15);
  vertex(-14, -20);
  endShape(CLOSE);

 
}

```
#### comment
* PShape 예제 하나를 선택하고, 내용 중에 2개 이상을 변경하시오.
* 교수님과 똑같은 예제를 사용했습니다.
*
