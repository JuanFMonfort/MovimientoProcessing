# MovimientoProcessing
```java

float x=55.0;
float y=55.0;
float velocidadX=10.0;
float velocidadY=20.0;
float radio=55.0;
int direccionX=1;
int direccionY=-1;
PImage img;
int space=20;

void setup(){
  size(120, 500);
  noStroke();
  ellipseMode(RADIUS);
  imageMode(CENTER);
  img = loadImage("pedobear.png");
}

void draw(){
  background(255);
  fill(0, 15);
  //image(img, x, height/2, radio, radio);//imagen para movimiento en eje X.
  //image(img, x, y, radio, radio);//imagen para movimiento en los dos ejes(X/Y).
  //rect(0, 0, width, height);
  
  /*x=x+velocidadX;
  if(x>width+radio){//Moviment Horizontal amb repeticio, no necesita direccion.
    x=-radio;
  }*/
  
  y=y+velocidadY;
  if(y>height+radio){//Moviment Vertical amb repeticio, no necesita direccion.
    y=-radio;
  }
  
  /*x+=velocidadX*direccionX;
  if ((x>width-radio)||(x<radio)){//Moviment Horzontal amb retorno, necesita direccion.
    direccionX= -direccionX;
  }*/
  
  /*y+=velocidadY*direccionY;
  if ((y>height-radio)||(y<radio)){//Moviment Vertical amb retorno, necesita direccion.
    direccionY= -direccionY;
  }*/
  
  if(direccionY==-1){
    fill(255, 0, 0);
  }else{
    fill(0, 0, 255);
  }
  
  ellipse(x, y, radio, radio);
  
  /*x+=velocidadX*direccionX;
  if ((x>width-radio)||(x<radio)){
    direccionX= -direccionX;
  }
                                    //Moviment en dos dimensions (ejer X/Y).
  y+=velocidadY*direccionY;
  if ((y>height-radio)||(y<radio)){
    direccionY= -direccionY;
  }*/
}
```
