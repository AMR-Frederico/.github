# 🎩 *Frederico*

## 🏎️ Descrição da categoria
O Frederico é um robô da categoria **_Trekking_** (ou **_Robomagellan_**, em inglês), que deve ser capaz de se localizar e locomover em um espaço determinado. 


### **Principais regras**
**Características do robô:**

- Dimensões máximas: 500x500x500 (cm)
- Peso: sem restrição
- Controle: Autônomo

**Características do campo:**

- Dimensões campo: 18x20 (m)
- A competição será realizada em gramado aberto, portanto estará sujeito as condições do campo e do clima ou em ambiente fechado.
- O robô deve ser capaz de identificar e alcançar 3 marcos definidos por uma chapa de metal branca de dimensões 1000x1000x2 (mm).
- Poderá, ou não, ser solicitado um cone para facilitar a identificação dos objetivos.

**Características de prova:**

- Duração: 10 min
- O robô deve alcançar os objetivos e ordem crescente (início para marco 1, marco 1 para marco 2 e marco 2 para marco 3);
- ***Ao redor do objetivo 3 terá obstáculos***, localizados a uma distância máxima de 5m do marco 3, sem tamanho pré definido e que deverão ser contornados, e não transpostos.
- Ao atingor cada marco, ***com pelo uma parte do robô tocando o marco***, o robô deverá sinalizar por meio de um dispositivo luminoso, vísivel e aparente, antes de prosseguir para o próximo objetivo. Ao chegar e sinalizar a chegada no último objetivo, o tempo será parado.
- Ganha o robô que terminar o circuito mais rápido, ou o que avance mais no trajeto.

** **
## O código: 
Para a versão atual do projeto, temos um ESP32 dedicado à leitura e processamento de sensores e também responsável pela sinalização do robô, outro para a leitura dos encoders e controle do driver de motor, e por fim, outro dedicado à conexão bluetooth com o controle de PS4
A mágica em si acontece no Raspberry Pi, em que rodamos o ROS 1 - atualmente utilizamos a versão noetic - que concentra todas as camadas mais alto nível do projeto, é onde fazemos a odometria, controle de posição, segurança e controle de objetivos. 

Nesta organização você encontrará todos os pacores/códigos escritos para o Fred. 

## Hardware
Em questão de hardware, o Fred tem: 

### Potência 
- 4x Motores 12V 1600 rpm 
- 2x driver monster motor VNH2SP30 dual channel 

#### Digital
- 2x ESP32 
- 1x Raspberry Pi 4b+ 
- 3x Sensor ultrassom HCSR05
- 1x Sensor inercial MPU6050 
- 1x Fita Led endereçavel WS2812B 
- 1x RPLidar A1
- 1x Regulador de tensão XL4015

### Baterias 
- 1x Bateria LiPo 5000mAh 20c 
- 1x Bateria LiFe 1100mAh 10c 

*
## 🌐 Links úteis

[🔗 Regras Robocore](https://robocore-eventos.s3.sa-east-1.amazonaws.com/public/Regras+-+Trekking+Indoor.pdf)

### Convenções ROS

[🔗 REP 103 - Standard Units of Measure and Coordinate Conventions](https://www.ros.org/reps/rep-0103.html)

[🔗 REP 105 - Coordinate Frames for Mobile Platforms](https://www.ros.org/reps/rep-0105.html)

[🔗 REP 145 - Conventions for IMU Sensor Drivers](https://www.ros.org/reps/rep-0145.html#data-reporting)
