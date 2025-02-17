
<p align="center">
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

# 🖥️ Práctica Wordpress en AWS

---

## 🎯 Objetivo

Instalación de Wordpress en instancia Ubuntu EC2 con soporte de base de datos RDS y EFS

---

### 1. Creación de la VPC

Iniciamos el laboratorio de AWS:

![image](https://github.com/user-attachments/assets/e8be3c4b-43d3-4742-851d-c7a86f585632)

Entramos al laboratorio:

![image](https://github.com/user-attachments/assets/8b4156b7-e48e-4832-a49c-ac90dc622f87)

Vamos al apartado de VPC y la creamos:

![image](https://github.com/user-attachments/assets/2524a6e6-3f70-428c-ad7b-91a9abb41fb8)

![image](https://github.com/user-attachments/assets/c6494b13-19c4-4ad0-a35e-a8106e0332e0)

Configuramos la VPC:

![image](https://github.com/user-attachments/assets/5e8a9071-8364-4b2f-a4ca-1ada5b049fc1)

![image](https://github.com/user-attachments/assets/34e75304-366e-4675-8736-1f6a6fccd082)

![image](https://github.com/user-attachments/assets/86f49129-fc2f-45e0-9a2c-bae3e34349e2)

Ahora la VPC se empieza a crear:

![image](https://github.com/user-attachments/assets/47138904-7345-4432-a2fe-6a0727376d11)

---

### 2. Creación de las máquinas EC2 en la subred publica y privada

Vamos a la zona de creación de máquinas EC2:

![image](https://github.com/user-attachments/assets/84e03612-2354-42b9-b4f2-eddddf5501b4)

Creamos la máquina para la red pública:

![image](https://github.com/user-attachments/assets/db74e7d4-3f83-46b2-8efb-8774964093a1)

Elegimos el sistema operativo:

![image](https://github.com/user-attachments/assets/4df21756-6d51-4efe-9eba-9ebc53702482)

Asignamos el par de claves para conexión con ssh

![image](https://github.com/user-attachments/assets/ed5c5aaa-232f-4248-823e-889cc3547957)

La asignamos a la VPC y subred publica 1:

![image](https://github.com/user-attachments/assets/7b25c303-cb52-4f15-9a66-ae87dcd253bb)

Creamos las reglas de firewall:

![image](https://github.com/user-attachments/assets/f682c494-678c-4f56-9747-913a864cf23d)

Creamos la máquina:

![image](https://github.com/user-attachments/assets/ce3e4f62-785f-48f0-ad78-2175ab15ddb8)













