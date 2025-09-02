# STM32_L298N_DCmotorPWM

## 📌 English Description
This project demonstrates DC motor control using an STM32F103 Nucleo board and the L298N motor driver.  
Speed is controlled via PWM; forward, reverse, brake, and coast are implemented.  
It’s a beginner-friendly example for embedded/robotics learning.

**Pin Map (STM32 ↔ L298N)**  
- ENA → **D12 (PA6, TIM3_CH1 PWM)**  
- IN1 → **D5 (PB4)**  
- IN2 → **D4 (PB5)**  
- OUT1/OUT2 → **DC Motor terminals**  
- GND (L298N) ↔ **GND (STM32)**  
- Battery **+** → L298N **Vs(“12V”)**, Battery **–** → **GND**  
> Note: Remove the **ENA jumper** to enable external PWM from PA6.

---

## 📌 한국어 설명
이 프로젝트는 STM32F103 Nucleo 보드와 L298N 모터 드라이버로 DC 모터를 제어하는 예제입니다.  
PWM으로 속도를 조절하고, 정/역회전·브레이크·코스트 기능을 구현했습니다.  
임베디드/로보틱스 기초 학습에 적합한 예제입니다.

**핀맵 (STM32 ↔ L298N)**  
- ENA → **D12 (PA6, TIM3_CH1 PWM)**  
- IN1 → **D5 (PB4)**  
- IN2 → **D4 (PB5)**  
- OUT1/OUT2 → **DC 모터 단자**  
- GND (L298N) ↔ **GND (STM32)**  
- 배터리 **+** → L298N **Vs(“12V”)**, 배터리 **–** → **GND**  
> 참고: **ENA 점퍼**를 제거해야 PA6에서 외부 PWM으로 속도 제어가 됩니다.

---

## 📹 Demo Video
[![YouTube Demo Thumbnail](https://img.youtube.com/vi/2Z3h3-cMfJA/0.jpg)](https://youtu.be/2Z3h3-cMfJA)

---

## 🔹 Core Code
```c
motor_forward();
motor_set_duty(20); HAL_Delay(1500);
motor_set_duty(40); HAL_Delay(1500);

motor_coast(); motor_set_duty(0); HAL_Delay(1500);

motor_reverse();
motor_set_duty(25); HAL_Delay(2000);

motor_brake(); motor_set_duty(0); HAL_Delay(1000);
```


