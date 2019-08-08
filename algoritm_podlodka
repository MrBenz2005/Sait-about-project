#include <Servo.h>
Servo servo;
void setup() {
 servo.attach(3);
 pinMode(4,OUTPUT);
 pinMode(5,OUTPUT);
 pinMode(6,OUTPUT);
 pinMode(7,OUTPUT);
 pinMode(2,INPUT);
 Serial.begin(115200);
}
void loop() {
 
  if (!digitalRead(2)){//если кнопка нажалась один раз
    Serial.println(digitalRead(2));
    servo.write(47);//поворот серво в состояние покоя
    
    analogWrite(6,255);//набирание воды + 3.5 секунды на погружение
    digitalWrite(7,1);
    delay(20500);
    analogWrite(6,0);
    delay(4000);

    analogWrite(5,255);//плывет 7 секунд вперед
    digitalWrite(4,0);
    delay(7000);
    analogWrite(5,0);

    servo.write(0);//поворот на 47 градусов вправо
    delay(1500);

    analogWrite(5,255);//плывет 7 секунд вправо
    digitalWrite(4,0);
    delay(7000);
    analogWrite(5,0);

    servo.write(94);//поворот на 47 градусов влево
    delay(1500);

    analogWrite(5,255);//плывет 7 секунд влево
    digitalWrite(4,0);
    delay(7000);
    analogWrite(5,0);

    analogWrite(6,255);//выкачивание воды + ожидание всплытия
    digitalWrite(7,0);
    delay(20400);
    analogWrite(6,0);

    
  }

