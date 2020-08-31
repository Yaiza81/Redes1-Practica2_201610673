# Manual de Reporte

### Dominio de broadcast y dominio de colisión 

Para poder realizar los cálculos es necesario considerar lo siguiente:
* Hub : 1 dc
        1 db 
        
* Switch: n dc (n = # de puertos conectados)
          1 db
          
* Router: 1db 
          1dc 
        (por cada interfaz conectada)
        
        
 Realizando los calculos de nuestra topología de red, obtenemos 9DC y 3 DB 
 ![image](Imagenes/colisiones.png)

### Captura de paquetes

1. Posicionarse en el enlace entre el switch y la vpc 
     ![image](Imagenes/0.png)

2. Seleccionar "start capture"
    ![image](Imagenes/1.png)

3. Ping de la vpc a las otras maquinas

4. AL dar click en ok, se abrira el programa wireshark

## VP1
    ![image](Imagenes/vpc2_c.png)
    
## VP2
   ![image](Imagenes/vpc3_c.png)

## VP3
  ![image](Imagenes/vpc4_c.png)

## VP4
  ![image](Imagenes/vpc_c.png)
  
## VP5
  ![image](Imagenes/vpc5_c.png)
  
## Tiny Linux 
  ![image](Imagenes/tiny_c.png)
