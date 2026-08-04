# 大deek的代码让我很舒服
* 现在是2026年7月28日的一个下午
打了一把农和两把粥之后
我的蛋已经疼飞了
思来覆去
我把目光投在了在家里吃两个星期灰的arduino主板
先来点基本的
```
void setup() {
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
}

void loop() {
  // 5号渐亮，6号渐暗（同时进行）
  for (int brightness = 0; brightness <= 255; brightness++) {
    analogWrite(5, brightness);      // 5号从暗到亮
    analogWrite(6, 255 - brightness); // 6号从亮到暗
    delay(10);
  }
  // 5号渐暗，6号渐亮（同时进行）
  for (int brightness = 255; brightness >= 0; brightness--) {
    analogWrite(5, brightness);      // 5号从亮到暗
    analogWrite(6, 255 - brightness); // 6号从暗到亮
    delay(10);
  }
}
```
*就这样，两个灯泡就交替发光了
台下观众欣喜若狂
灯泡！灯泡！
