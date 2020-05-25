#지형 만들기1

```
int cols, rows;
int scl = 20;
int w = 2000; 
int h = 1500;
float flying = 0;
float[][] terrain;

void setup(){
  size(600, 600, P3D);
  cols = w / scl;
  rows = h / scl;
  terrain = new float[cols][rows];
}

void draw(){
  flying -= 0.1;  // -= 는 반대로 흘러감, 안 쪽의 숫자는 흘러가는 속도
  float yoff = flying;
  for (int y = 0; y < rows; y++){
    float xoff = 0;
    for (int x = 0; x < cols; x++){
      terrain[x][y] = map(noise(xoff, yoff), 0, 1, -100, 100);
      xoff += 0.2;  // 산 높이
    }
    yoff += 0.2;
  }
  
  background(0);
  stroke(255);  // 테두리 색
  noFill();
  
  translate(width/2, height/2+50);
  rotateX(PI/3);  // 경사 높을 수록 위에서 봄
  translate(-w/2, -h/2);
  for (int y = 0; y < rows-1; y++){
    beginShape(TRIANGLE_STRIP);
     for (int x = 0; x < cols; x++){
       fill(105+terrain[x][y],128-terrain[x][y], 255+terrain[x][y]);  // 색 넣기
       vertex(x*scl, y*scl, terrain[x][y]);
       vertex(x*scl, (y+1)*scl, terrain[x][y+1]);

   // rect(x*scl, y*scl, scl, scl);
    }
    endShape();
  }
}
```
#지형 만들기2
```
int cols, rows;
int scl = 20;
int w = 2000;
int h = 1500;
float flying = 0;
float[][] terrain;



void setup(){
  size(700, 700, P3D);
  cols = w / scl;
  rows = h / scl;
  terrain = new float[cols][rows];
}

void draw(){
 
  flying -= 0.1;  // -= 는 반대로 흘러감,
  float yoff = flying;
  for (int y = 0; y < rows; y++){
    float xoff = 0;
    for (int x = 0; x < cols*0.45; x++){
      terrain[x][y] = map(noise(xoff, yoff), 0, 1, -100, 100);
      xoff += 0.2;
    }
    for (int x = 55; x < cols; x++){
      terrain[x][y] = map(noise(xoff, yoff), 0, 1, -100, 100);
      xoff += 0.2;
    }
    yoff += 0.2;
  }
  
  background(0);
  stroke(255);
  noFill();
  
  translate(width/2, height/2+50);
  rotateX(PI/3);
  translate(-w/2, -h/2);
  for (int y = 0; y < rows-1; y++){
    beginShape(TRIANGLE_STRIP);
     for (int x = 0; x < cols; x++){
       vertex(x*scl, y*scl, terrain[x][y]);
       vertex(x*scl, (y+1)*scl, terrain[x][y+1]);

   // rect(x*scl, y*scl, scl, scl);
    }
    endShape();
    
    beginShape(TRIANGLE_STRIP); //도로
    fill(0,122,0); 
    vertex(45*scl, y*scl, terrain[44][y]);    //44
    vertex(45*scl, (y+1)*scl, terrain[44][y+1]);
    fill(192,132,87);
    vertex(46*scl, y*scl, terrain[45][y]); //45
    vertex(46*scl, (y+1)*scl, terrain[45][y+1]);

    for (int x = 46; x < cols*0.54; x++) {
      fill(0);

      vertex(x*scl, y*scl, terrain[x][y]);
      vertex(x*scl, (y+1)*scl, terrain[x][y+1]);

    }
    fill(192,132,87);
    
    vertex(54*scl, y*scl, terrain[54][y]);
    vertex(54*scl, (y+1)*scl, terrain[54][y+1]);
    
    fill(0,122,0);
    vertex(56*scl, y*scl, terrain[56][y]);
    vertex(56*scl, (y+1)*scl, terrain[56][y+1]);

    endShape();
  }
}
```
