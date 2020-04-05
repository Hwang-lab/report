# report 3-1
## 17학번 황근원

```
PImage img;

void setup() {
  size(1000, 1000);
  frameRate(100);
  img = loadImage("p.jpg");
  //p는 숨은 그림찾기 이미지입니다.
  img.loadPixels();
  loadPixels();
  
}

void draw() {
  for (int x = 0; x < img.width; x++) {
    for (int y = 0; y < img.height; y++ ) {
      // Calculate the 1D location from a 2D grid
      int loc = x + y*img.width;
      // Get the R,G,B values from image
      float r,g,b;
      r = red (img.pixels[loc]);
      //g = green (img.pixels[loc]);
      //b = blue (img.pixels[loc]);
      // Calculate an amount to change brightness based on proximity to the mouse
      float maxdist = 30;//dist(0,0,width,height);
      float d = dist(x, y, mouseX, mouseY);
      float adjustbrightness = 255*(maxdist-d)/maxdist;
      r += adjustbrightness;
      //g += adjustbrightness;
      //b += adjustbrightness;
      // Constrain RGB to make sure they are within 0-255 color range
      r = constrain(r, 0, 255);
      //g = constrain(g, 0, 255);
      //b = constrain(b, 0, 255);
      // Make a new color and set pixel in the window
      //color c = color(r, g, b);
      color c = color(r);
      pixels[y*width + x] = c;
      
    }
  }
  updatePixels();
}
```
# comment
*1. 프로세싱 Examples 중에 하나를 선택하시오.
* 저는 이미지 프로세싱에 brightness를 선택했습니다.
*2. 프로그램에 대해서 설명을 하시오.
*3. 내가 변형할 내용에 대해서 적으시오.
*4. 변형된 코드의 결과에 대해서 설명하시오.
*5. 과제 작성소감을 적으시오.
