# -
斜移十字


float i ;
int x , y , r , b , g ;


void setup() {
  size(300,300) ;//创建300*300画布
  background(255) ;//白色背景
  rectMode(CORNER) ;//用左上点和长和宽定义矩形
  x = 0 ;//初始横线在最左边
  y = 0 ;//初始竖线在最右边
  r = 255 ;
  g = 255 ;
  b = 255 ;//初始线为白色
  noStroke() ;
}


void draw() {
 fill (r,g,b) ;
 rect(x,0,1,500) ;
  x = x + 1 ;//竖线右移
  
  i = random(0,3) ;//随机选一个颜色参数
  if (i >= 2) {
    r = r - 1 ;
  }
  else if (i >= 1) {
    g = g - 1 ;
  }
  else {
    b = b - 1 ;
  }//颜色深一点
  
 fill (r,g,b) ;
 rect(0,y,500,1) ;
 y = y + 1 ;//横线下移
 
 i = random(0,3) ;//随机选一个颜色参数
  if (i >= 2) {
    r = r - 1 ;
  }
  else if (i >= 1) {
    g = g - 1 ;
  }
  else {
    b = b - 1 ;
  }//颜色深一点
}
