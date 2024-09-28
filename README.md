## Self Balancing Robot
The system is a self-balancing robot that corrects tilts in its angle, returning the robot to a more stable position. It consists of a sturdy chassis, motor control circuit, stm32 microcontroller and an external accelerometer. The chassis is made of plexiglass and has two layers. The lower layer holds all the circuitry, namely, the h-bridge driver and the external power supply. Under this layer, there are two motors that control the wheels of the robot, these are connected to the H-bridge which is controlled by the STM32 microcontroller. The top layer supports the STM32 microcontroller, which is also connected accelerometer and interfaces with it using I2C. The two layers are connected using four studs, which ensures that both surfaces are parallel, and that gyroscope measurements are as accurate as possible. The software loaded on the STM32 microcontroller takes measurements from both the accelerometer and gyroscope (and normalizes them), fuses them using a complementary/linear Kalman filter, then applies a PD control algorithm which sends a PWM signal to the motors via the h-bridge driver circuit. Feedback data from the program is also displayed on an LCD.


![Balancing Robot](https://github.com/inhald/Self-Balancing-Robot/blob/main/chassis_photo.jpg)


[Demo](https://www.youtube.com/watch?v=SOBp2ADBT7k)

