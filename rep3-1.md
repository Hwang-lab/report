# report 3-1
## 17학번 황근원

```
PImage img;

void setup() {
  size(800, 650);
  frameRate(100);
  img = loadImage("p.jpg");
  // p는 숨은 그림찾기의 이미지 입니다.
  img.loadPixels();
  loadPixels();
}

void draw() {
  for (int x = 0; x < img.width; x++) {
    for (int y = 0; y < img.height; y++ ) {
      int loc = x + y*img.width;
      float r,g,b;
      r = red (img.pixels[loc]);
      float maxdist = 25;
      // maxdist 의 값을 크게하면 마우스 주변이 더 잘 보입니다. 그림 찾기의 난이도를 위해 좁게 했습니다.
      float d = dist(x, y, mouseX, mouseY);
      float adjustbrightness = 255*(maxdist-d)/maxdist;
      // 밝기의 범위입니다. 숫자가 작을수록 범위가 커집니다.
      r += adjustbrightness;
      r = constrain(r, 0, 255);
      color c = color(r);
      pixels[y*width + x] = c;
    }
  }
  updatePixels();
}

```
# comment
* 1. 프로세싱 Examples 중에 하나를 선택하시오.
* 저는 이미지 프로세싱에 brightness를 선택했습니다.
* 2. 프로그램에 대해서 설명을 하시오.
* p라는 숨은 그림찾기란느 이미지를 놓고 마우스로 숨은 그림을 찾는 단순한 게임입니다. 전체적인 배경은 검정색이고 마우스 주변만 밝게 해서 숨은 그림 찾기의 난이도가 조금 올라 갔습니다.
* 3. 내가 변형할 내용에 대해서 적으시오.
* 마우스 주변의 밝기 조정(크기빛 명도)과 이미지를 숨은 그림으로 변환하는 것입니다.
* 4. 변형된 코드의 결과에 대해서 설명하시오.
*   img = loadImage("p.jpg"); 이미지를 숨은 그림 찾기로 바꿉니다. float maxdist = 25; 마우스 주변의 밝기 범위입니다. float adjustbrightness = 255*(maxdist-d)/maxdist; 이것도 밝기의 크기입니다.
* 5. 과제 작성소감을 적으시오.
* 단순한 값을 바꾸는 것만으로도 숨은 그림찾기의 재미를 높일 수 있었습니다. 틀린 곳을 클릭시 x표시 정답은 o표시를 하도록 하고싶었지만
이미지 위에 그림을 표현하는 것을 하지 못해 아쉽니다. 조금 더 공부하여 완성하고 싶습니다!
