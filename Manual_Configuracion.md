# Redes1-Practica2_201610673

Se debe configurar y administrar los dispositivos de una infraestructura de red. La empresa tiene operando 6 máquinas, administradas en 3 subredes;
* 2 en el área de finanzas
* 3 en el área de ventas 
* 1 virtual en el área de Informática. 

### Topología de red 

![image](Imagenes/topo.png)

### Pasos para crear la topología

1. Agregar un router 
 ![image](Imagenes/c1.PNG)   
 
2. Agregar los switch 
![image](Imagenes/switch.PNG) 

3. Agregar las vpc
![image](Imagenes/vpc.PNG) 

4. Agregar la máquina virtual linux 
![image](Imagenes/tiny.PNG)  

5. Agregar una interfaz al router 
![image](Imagenes/agrega_interfaz.png) 

6. Irse a la sección de slots y seleccionar configuración 
![image](Imagenes/interfaz.png)   

Para poder conectarlos
![image](Imagenes/conectar.png)   

## Configuraciones para la topología de Red 
  A continuación se detalla cada uno de los comandos necesarios para realizar la configuración de cada uno de los dispositivos que conforman la topología de red 

### Router 
  1. Comando para acceder a la configuración de la terminal 
      * configure terminal 
  
  2. Comando para acceder a la interfaz fastEthernet 0/0
      * int f0/0

     ![image](Imagenes/r1_f00.PNG)
  
  3. Comando para configurar la ip del router 
       * ip address 192.168.10.1 255.255.255.192
   
       ![image](Imagenes/r1_ip_f00.PNG)
  
  4. Comando para activar la interfaz
       * no shutdown
   
      ![image](Imagenes/r1_activar.PNG)
  
  5. Salir de la interfaz fastEthernet 0/0
       * Exit 
   
      ![image](Imagenes/r1_exit.PNG)
  
  6. Comando para acceder al fastEthernet 0/1
       * int f0/1
      
      ![image](Imagenes/r1_f01.PNG)
  
  7. Comando para configurar la ip del router 
        * ip address 192.168.10.65 255.255.255.192
      
      ![image](Imagenes/r1_ip_f01.PNG)
  
  8. Comando para activar la interfaz
        * no shutdown
     
        ![image](Imagenes/r1_activar.PNG)
  
  9. Salir de fastEthernet 0/1
       * Exit 
    
       ![image](Imagenes/r1_exit.PNG)
   
  10. Comando para acceder al fastEthernet 1/0
       * int f1/0
          
        ![image](Imagenes/r1_f10.PNG)
  
  11. Comando para configurar la ip del router 
       * ip address 192.168.10.129 255.255.255.192
      
       ![image](Imagenes/r1_ip_f10.PNG)
  
  12. Comando para activar la interfaz
       * no shutdown
     
      ![image](Imagenes/r1_activar.PNG)
  
  13. Salir de las configuraciones
       * exit 
      
      ![image](Imagenes/r1_salir.PNG)
  
  14. Guardar los cambios 
        * wr 
       
       ![image](Imagenes/r1_save.PNG)
  
  15. Para mostrar la información de las interfaces
         * show ip interface brief
       
        ![image](Imagenes/r1_sh.PNG)
  
### VPC1
  1. Comando para configurar la ip 
      * ip 192.168.10.2/26 192.168.10.1
   
      ![image](Imagenes/sh_ip_pc1.PNG)
  
  2. Para mostrar la configuración de ip y máscara de red 
      * sh ip 
  
      ![image](Imagenes/sh_ip_pc1.PNG)
  
  3. Para guardar los cambios 
      * save 
  
     ![image](Imagenes/save_pc1.PNG)

### VPC2
  1. Comando para configurar la ip 
      * ip 192.168.10.3/26 192.168.10.1
   
     ![image](Imagenes/sh_ip_pc2.PNG)
  
  2. Para mostrar la configuración de ip y máscara de red 
      * sh ip 
  
     ![image](Imagenes/sh_ip_pc2.PNG)
  
  3. Para guardar los cambios 
      * save 
  
      ![image](Imagenes/save_pc2.PNG)

### VPC3
  1. Comando para configurar la ip 
      * ip 192.168.10.66/26 192.168.10.65
   
     ![image](Imagenes/sh_ip_pc3.PNG)
  
  2. Para mostrar la configuración de ip y máscara de red 
      * sh ip 
  
     ![image](Imagenes/sh_ip_pc3.PNG)
  
  3. Para guardar los cambios 
      * save 
  
     ![image](Imagenes/save_pc3.PNG)

### VPC4
  1. Comando para configurar la ip 
      * ip 192.168.10.67/26 192.168.10.65
   
     ![image](Imagenes/sh_ip_pc4.PNG)
  
  2. Para mostrar la configuración de ip y máscara de red 
      * sh ip 
  
     ![image](Imagenes/sh_ip_pc4.PNG)
  
  3. Para guardar los cambios 
      * save 
  
     ![image](Imagenes/save_pc4.PNG)

### VPC5
  1. Comando para configurar la ip 
      * ip 192.168.10.68/26 192.168.10.65
   
     ![image](Imagenes/sh_ip_pc5.PNG)
  
  2. Para mostrar la configuración de ip y máscara de red 
      * sh ip 
  
     ![image](Imagenes/sh_ip_pc5.PNG)
  
  3. Para guardar los cambios 
      * save 
  
     ![image](Imagenes/save_pc5.PNG)

### linux-1
 1.  Entrar al panel de control y seleccionar Network 
  
     ![image](Imagenes/network.PNG)
  
 2. Ingresar la siguiente ip, gateway, máscara de red 
    
      ![image](Imagenes/linux.PNG)
  
3. Aplicar y Salir 

4. Abrir la terminal 
   Comando para mostrar la configuración 
      * ifconfig 
   
        ![image](Imagenes/ifconfig.PNG)
   
### Comprobar  el estado de la conexión 
  ping ip 
        * ping 192.168.10.2
        * ping 192.168.10.3
        * ping 192.168.10.66
        * ping 192.168.10.67
        * ping 192.168.10.68
        * ping 192.168.10.130
  
   ![image](Imagenes/ping1.PNG)
  
  ![image](Imagenes/ping2.PNG)
    
