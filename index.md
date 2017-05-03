---
layout: default
---

# [](#header-1)Music Buzzer: "Little Star"

## [](#header-2)Brief Intro for MB

Music Buzzer uses a simple buzzer to play beautiful sounds. In this project, the melody of "Little Star" is played.

The frequency of buzzer controls its pitch, while the time per note controls the beats. When they come together, a beautiful sound is played. Just enjoy it ^_^

## [](#header-2)Source Code for MB

```Arduino
/*------------音符对应蜂鸣器频率------------*/

#define B0  31
#define C1  33
#define CS1 35
#define D1  37
#define DS1 39
#define E1  41
#define F1  44
#define FS1 46
#define G1  49
#define GS1 52
#define A1  55
#define AS1 58
#define B1  62
#define C2  65
#define CS2 69
#define D2  73
#define DS2 78
#define E2  82
#define F2  87
#define FS2 93
#define G2  98
#define GS2 104
#define A2  110
#define AS2 117
#define B2  123
#define C3  131
#define CS3 139
#define D3  147
#define DS3 156
#define E3  165
#define F3  175
#define FS3 185
#define G3  196
#define GS3 208
#define A3  220
#define AS3 233
#define B3  247
#define C4  262
#define CS4 277
#define D4  294
#define DS4 311
#define E4  330
#define F4  349
#define FS4 370
#define G4  392
#define GS4 415
#define A4  440
#define AS4 466
#define B4  494
#define C5  523
#define CS5 554
#define D5  587
#define DS5 622
#define E5  659
#define F5  698
#define FS5 740
#define G5  784
#define GS5 831
#define A5  880
#define AS5 932
#define B5  988
#define C6  1047
#define CS6 1109
#define D6  1175
#define DS6 1245
#define E6  1319
#define F6  1397
#define FS6 1480
#define G6  1568
#define GS6 1661
#define A6  1760
#define AS6 1865
#define B6  1976
#define C7  2093
#define CS7 2217
#define D7  2349
#define DS7 2489
#define E7  2637
#define F7  2794
#define FS7 2960
#define G7  3136
#define GS7 3322
#define A7  3520
#define AS7 3729
#define B7  3951
#define C8  4186
#define CS8 4435
#define D8  4699
#define DS8 4978

#define buzzer_pin 6 //定义蜂鸣器引脚

/*------------定义歌曲音调的数组------------*/

int notes[] = {
  C5, C5, G5, G5, A5, A5, G5,
  F5, F5, E5, E5, D5, D5, C5, 
  G5, G5, F5, F5, E5, E5, D5,
  G5, G5, F5, F5, E5, E5, D5,
  C5, C5, G5, G5, A5, A5, G5,
  F5, F5, E5, E5, D5, D5, C5
};

/*------------定义歌曲节奏的数组------------*/

byte beats[] = {
  500, 500, 500, 500, 500, 500, 1000,
  500, 500, 500, 500, 500, 500, 1000,
  500, 500, 500, 500, 500, 500, 1000,
  500, 500, 500, 500, 500, 500, 1000,
  500, 500, 500, 500, 500, 500, 1000,
  500, 500, 500, 500, 500, 500, 1000
};

void setup() {
  pinMode(buzzer_pin, OUTPUT); //定义蜂鸣器引脚为输出状态
}

void loop() {
  for ( int i = 0; i < 42; i++) {

/*------------设置i在歌曲长度内递增，这样就能逐一执行数组中的数据------------*/

    tone(buzzer_pin, notes[i]); //播放音乐
    delay(beats[i]); //播放间隔

    noTone(buzzer_pin);

    if((i+1)%7==0){
      delay(150);
    }
    else{
      delay(10);
    }
  }
  delay(1000);
}
```

* * *

# [](#header-1)Audio-Controlled Light

## [](#header-2)Brief Intro for ACL

Wow! A light that can be lightened by sound when its dark. Come and have a look!

## [](#header-2)Source Code for ACL

```Arduino
#include <Adafruit_NeoPixel.h>  //调用LED彩灯的库文件

Adafruit_NeoPixel ColorLED = Adafruit_NeoPixel(1, 6, NEO_GRB + NEO_KHZ800);
//定义彩灯引脚以及数量


int state; //定义一个整数变量state
int stateSound;

int Light=0;
double timeP=0.0;

void setup()
{
  ColorLED.begin();
  pinMode(A0, INPUT); //设置光敏传感器引脚为输入状态
  pinMode(A2, INPUT); //设置声敏传感器引脚为输入状态
  Serial.begin(9600); //设置串口波特率为9600
}
void loop()
{
  state = analogRead(A0);
  stateSound = analogRead(A2);
  Serial.print("state:");
  Serial.println(state);
  Serial.print("state2:");
  Serial.println(stateSound);

  if(Light==0){
    if (state < 50 && stateSound>100) { //天黑且有声音,亮灯
      Light=1;
      timeP=millis();
    }
  }
  else {
    if(stateSound>100){
      timeP=millis();
    }
    else{
      if(millis()-timeP>5000){
        Light=0;
      }
    }
  }

  if(Light==1){
    ColorLED.setPixelColor(0, ColorLED.Color(255, 0, 0));  //设置彩灯颜色为红色
    ColorLED.show();  //显示彩灯效果
  }
  else
  {
    ColorLED.setPixelColor(0, ColorLED.Color(0, 0, 0));  //设置彩灯颜色为红色
    ColorLED.show();  //显示彩灯效果
  }
}
```

