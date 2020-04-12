# report 4-1
## 17학번 황근원

```
void setup(){
  size(500,500);
  background(255, 255, 255);  // 배경, 흰색
  translate(50,50);
  
  fill(251,206,177);  //  얼굴 색, 살색
  ellipse(200, 200, 200, 200); //  얼굴 크기
  
  fill(255);
  ellipse(160, 180, 40, 27); //  눈, 왼쪽
  ellipse(240, 180, 40, 27); //  눈, 오른쪽
  
  fill(0);
  ellipse(160, 180, 15, 15); //  눈동자, 왼쪽 
  ellipse(240, 180, 15, 15); //  눈동자, 오른쪽
  
  fill(255,0,0);
  arc(200, 250, 50, 40, 0, PI); //  입
  
  fill(0);
  arc(200, 160, 188, 160, radians(180), radians(360));  //  머리카락
  
  fill(251,206,177);
  arc(105, 190, 50, 50, radians(90), radians(270));  //귀, 왼쪽
  
  fill(251,206,177);
  arc(295, 190, 50, 50, radians(270), radians(450));  //귀, 오른쪽
  
  fill(255,170,140);  // 코
  beginShape();  // 좌표를 이어 만든 도형
  vertex(200, 200);
  vertex(190, 220);
  vertex(210, 220);
  endShape(CLOSE);
  
  fill(0);  //넥타이
  beginShape();  // 좌표를 이어 만든 도형
  vertex(200, 300);
  vertex(170, 290);
  vertex(170, 310);
  vertex(200, 300);
  vertex(230, 290);
  vertex(230, 310);
  endShape(CLOSE);
  
}

```

### comment
*저의 얼굴을 만들어 보았습니다! 
*조금 더 배워서 팔 다리를 만들어 자유롭게 걷는 것을 만들어 보고 싶습니다.
