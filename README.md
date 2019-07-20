# Arduino_Maker
Brilliant Usage of Arduino

/***************************************************** Tracker *****************************************************/
![텍스트](https://user-images.githubusercontent.com/51029215/61582552-3aeb6f80-ab67-11e9-97a6-5496456e34f3.png)
![텍스트](https://user-images.githubusercontent.com/51029215/61582558-46d73180-ab67-11e9-9a3b-e9a40b0c4e5c.jpg)



Tracker : 아두이노, 초음파 센서(2), 서보 모터로 물체를 추적하는 행위를 구현

Tracker_pulseIn : 초음파 센서의 신호 수신을 내장 함수인 pulseIn 함수를 선택

                : ~ pi/5(rad/sec) 수준의 속도까지는 수월하게 추적 가능함
                
           Prob : 초음파센서 전면 약 5m이상 거리에 장애물이 없는 개활지에서 작동 불능상태.
           
Tracker_interrupts : 코드상 개활지에서 발생하는 pulseIn함수로 인해 발생하는 code blocking 문제를 계산 및 명령을 loop에서 ISR로 옮겨 보완함

                   : ~pi/2(rad/sec)의 속도까지 추적 가능함
                   
              Prob : (특히 물체가 센서와 약 10cm 이내로 근접하였을 경우) 고개가 좌우로 요동치는 모습을 볼 수 있음.
              
             After : 두 동일한 SR-04 센서의 출력(TRIG)-수신(ECHO) Signal pairing이 보장받지 못하기 때문으로 예상하여 
             
                     수신 영역대가 다른 초음파센서를 구비하여 동작시켜볼 예정
                     
/***************************************************** Tracker *****************************************************/

