#include<Wire.h>
#include<MPU6050.h>

const int MPU6050=0x68;
int16_t AcX,AcY,AcZ,Tmp,GyX,GyY,GyZ,sudX,sudY,sudZ,n,l,GyX1,GyY1,GyZ1,AcX1,AcY1,AcZ1,ax,ay,az,gx,gy,gz,x,y,z;

void setup() {
  Wire.begin();
  Wire.beginTransmission(MPU6050);
  Wire.write(0);
  Wire.write(0x6B);
  Wire.endTransmission(true);
  Serial.begin(9600);
  
}

void loop() {
  Wire.beginTransmission(MPU6050);
  Wire.write(0x3B);
  Wire.endTransmission(false);
  Wire.requestFrom(MPU6050,12,true);
  AcX=Wire.read()<<8|Wire.read();
  AcY=Wire.read()<<8|Wire.read();
  AcZ=Wire.read()<<8|Wire.read();
  GyX=Wire.read()<<8|Wire.read();
  GyZ=Wire.read()<<8|Wire.read();
  GyY=Wire.read()<<8|Wire.read();

  //kalibrasi accelerometer
  AcX1=AcX*0.0001;  
  AcY1=AcY*0.0001;
  AcZ1=AcZ*0.00001;
  l=0.01;
  x=AcX/l;
  y=AcY/l;
  z=AcZ*0.1;
 
  //perhitungan tylor x+x^3/6+5*x^6/24...
  sudX=22/14-x+x*x*x /6+3*x*x*x*x*x/40+5*x*x*x*x*x*x*x/2688;
  sudY=22/14-y+y*y*y /6+3*y*y*y*y*y/40+*y*y*y*y*y*y*y/2688;
  sudZ=z*10;
  
  //kalibrasi gyroskop
  GyX1=GyX*0.001;
  GyY1=GyY*0.1;
  GyZ1=GyZ*0.01;
  
   // besar sudut keduannya
   // sudut/pi * 180
   gx=GyX1/3.14 *180;
   gy=GyY1/3.14 *180;#include<Wire.h>
#include<MPU6050.h>

const int MPU6050=0x68;
int16_t AcX,AcY,AcZ,Tmp,GyX,GyY,GyZ;
float sudX,sudY,sudZ,n,l;
float GyX1,GyY1,GyZ1,AcX1,AcY1,AcZ1,ax,ay,az,gx,gy,gz;

void setup() {
  Wire.begin();
  Wire.beginTransmission(MPU6050);
  Wire.write(0);
  Wire.write(0x6B);
  Wire.endTransmission(true);
  Serial.begin(9600);
  
}

void loop() {
  Wire.beginTransmission(MPU6050);
  Wire.write(0x3B);
  Wire.endTransmission(false);
  Wire.requestFrom(MPU6050,12,true);
  AcX=Wire.read()<<8|Wire.read();
  AcY=Wire.read()<<8|Wire.read();
  AcZ=Wire.read()<<8|Wire.read();
  GyX=Wire.read()<<8|Wire.read();
  GyZ=Wire.read()<<8|Wire.read();
  GyY=Wire.read()<<8|Wire.read();

  //kalibrasi accelerometer
  AcX1=AcX*0.0001;  
  AcY1=AcY*0.0001;
  AcZ1=AcZ*0.00001;
  l=0.01;
  float x=AcX/l;
  float y=AcY/l;
  float z=AcZ;
 
  //perhitungan tylor x+x^3/6+5*x^6/24...
  sudX=22/14 -(x + x*x*x /6 + 3*x*x*x*x*x /40 + 5*x*x*x*x*x*x*x /2688);
  sudY=22/14 -(y + y*y*y /6 + 3*y*y*y*y*y /40 + 5*y*y*y*y*y*y*y /2688);
  sudZ=z;
  
  //kalibrasi gyroskop
  GyX1=GyX*0.001;
  GyY1=GyY*0.1;
  GyZ1=GyZ*0.01;
  
   // besar sudut keduannya
   // sudut/pi * 180
   gx=GyX1/3.14 *180;
   gy=GyY1/3.14 *180;
   gz=GyZ1/3.14 *180;
   ax=sudX/3.14 *180;
   ay=sudY/3.14 *180;
   az=sudZ/3.14 *180;
  
  Serial.print(" Accelerometer :");
  Serial.print(" X = ");Serial.print(sudX*10);Serial.print("cm  ");
  Serial.print(" Y = ");Serial.print(sudY*0.1);Serial.print("cm ");
  Serial.print(" Z = ");Serial.print(sudZ*10);Serial.print("cm ");
  
  Serial.print(" Gyroscope :");
  Serial.print(" X = ");Serial.print(GyX1);
  Serial.print(" Y = ");Serial.print(GyY1);
  Serial.print(" Z = ");Serial.print(GyZ1);
  Serial.println(" ");
  delay(100);
}

   gz=GyZ1/3.14 *180;
   ax=sudX/3.14 *180;
   ay=sudY/3.14 *180;
   az=sudZ/3.14 *180;
  
  Serial.print(" Accelerometer :");
  Serial.print(" X = ");Serial.print(sudX*10);Serial.print("cm  ");
  Serial.print(" Y = ");Serial.print(sudY*0.1);Serial.print("cm ");
  Serial.print(" Z = ");Serial.print(sudZ*10);Serial.print("cm ");
  
  Serial.print(" Gyroscope :");
  Serial.print(" X = ");Serial.print(GyX1);
  Serial.print(" Y = ");Serial.print(GyY1);
  Serial.print(" Z = ");Serial.print(GyZ1);
  Serial.println(" ");
  delay(100);
}
