# STM32_L298N_DCmotorPWM

## 📌 English Description
This project demonstrates DC motor control using an STM32F103 Nucleo board and the L298N motor driver.  
The motor speed is controlled via PWM, and functions for forward, reverse, brake, and coast are implemented.  
The project showcases basic embedded motor control suitable for robotics and embedded systems learning.

---

## 📌 한국어 설명
이 프로젝트는 STM32F103 Nucleo 보드와 L298N 모터 드라이버를 이용해 DC 모터를 제어하는 실습입니다.  
PWM으로 속도를 조절하며, 정회전·역회전·브레이크·코스트 기능을 구현했습니다.  
임베디드 및 로보틱스 학습을 위한 기본적인 모터 제어 예제입니다.

---

## 📹 Demo Video
[YouTube Demo](https://youtu.be/2Z3h3-cMfJA?si=nAcFxe7q3gL0Hjh2)

---

## 🔹 Core Code
`c
motor_forward();
motor_set_duty(20); HAL_Delay(1500);
motor_set_duty(40); HAL_Delay(1500);

motor_coast(); motor_set_duty(0); HAL_Delay(1500);

motor_reverse();
motor_set_duty(25); HAL_Delay(2000);

motor_brake(); motor_set_duty(0); HAL_Delay(1000);
