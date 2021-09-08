# H-Bridge-code

## Table of contents

### Table of contents

* [Task Info](#task-info)
* [Task code](#task-code)

##task info

This documentataion show to how whrite code of H-Bridge.

## code H-Bridge
   
   `#define MOTOR_IN1 12 `
   
   `   #define MOTOR_IN2 13     `
   
   `void motor_forward(void);  // a function that will be called to rotate it clockwise`
   
   `void motor_reverse(void);  // a function that will be called to totate it counter-clockwise`
   
  `void motor_stop(void);     // a function that will be called to stop the rotation `

`void setup()   ` 
{
  ` pinMode(MOTOR_IN1, OUTPUT);  // set the first pin of the relay as output
  pinMode(MOTOR_IN2, OUTPUT);  // set the 2nd pin of the relay as output     `
}

`void loop()  ` 
{
  `  motor_forward();             // move forward/clockwise
  delay(3000);                 // keep rotating cw for 3 seconds
  motor_stop();                // stop rotating
  delay(3000);                 // stand still for 3 seconds
  motor_reverse();             // reverse the rotation direction/ccw
  delay(3000);                 // keep rotating ccw for 3 seconds
  motor_stop();                // stop rotating
  delay(3000);                 // stand still for 3 seconds            `
}

`       void motor_forward(void)       // the function that will cause the motor to rotate cw            `
{
 `         digitalWrite(MOTOR_IN1, HIGH);
  digitalWrite(MOTOR_IN2, LOW);              `
}

`           void motor_reverse(void)       // the function that will cause the motor to rotate ccw        `
{
 `             digitalWrite(MOTOR_IN1, LOW);
  digitalWrite(MOTOR_IN2, HIGH);                 `
}

`        void motor_stop(void)          // the function that will cause the motor to stop rotating              `
{
  `         digitalWrite(MOTOR_IN1, LOW);
  digitalWrite(MOTOR_IN2, LOW);
}           `



















