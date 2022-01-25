# Trafic Light with 1 (RGB) LED

> Program 

```ino
// Coded by Shiva
int
  R = 13,
  G = 12,
  B = 11
;

void setup(){
  pinMode(R, OUTPUT);
  pinMode(G, OUTPUT);
  pinMode(B, OUTPUT);
}

void loop(){
  signal(HIGH, LOW, LOW);
  signal(HIGH, HIGH, LOW);
  signal(LOW, HIGH, LOW);
}

void signal(int r, int g, int b){
  digitalWrite(R, r);
  digitalWrite(G, g);
  digitalWrite(B, b);
  delay(r==g?2000:5000);
}
```

> Circuit

![](rbg_trafic_light.png)
