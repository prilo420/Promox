# Promox

Nombre: Juan Felipe Criollo Valderrama

### Documentación

## Creacion de maquinas Hyper-V

1. Seleccionamos Nuevo/ Maquina Virtual...
2. Le ponemos el Nombre: Nodo1
3. Seleccionamos la Generacio

<img src="ca0.0.png" alt="">

5. Configuramos la Memoria de Inicio 
* 4096MB Nodo1
* 4096MB nodo2
6. Configuramos la Conexion
   
<img src="ca0.2.png" alt="">

7. Seleccionamos Instalar un sistema operativo desde un CD/DVD-ROM de arranque/ Archivo de imagen (.iso):
* seleccionamos la iso de Promox

<img src="ca0.3.png" alt="">

8. seleccionamos siguiente/ terminar
9. cconfiguramos para que tenga 4 procesadores
10. se repite todo para el Nodo2

---

## Power shell
* entramos a power sheell como administrador
* Habilitamos la virtualización anidada con este comando 
<img src="N.png" alt="">

```
Set-VMProcessor -VMName "Nodo1" -ExposeVirtualizationExtensions $true
```
```
Set-VMProcessor -VMName "Nodo2" -ExposeVirtualizationExtensions $true
```
---
## Instalacion de los Nodos

1. seleccionamos Install Promox VE (Graphical)

<img src="ca1.png" alt="">

2. Configuramos el idioma y la zona

<img src="ca2.png" alt="">

3. Ingresamos un correo y contraseña

<img src="ca3.png" alt="">

4. Configuramos la red
HotsName | Pve1 | Pve2
Ip Address |  172.27.43.10 |172.27.45.11
Gateway | 172.27.43.1 | 172.27.45.1
DNS Sever | 8.8.8.8 | 8.8.8.8

<img src="ca4.png" alt="">

6. seleccionamos instalar
* quitamos la ISO para no volverlo a instalar
<img src="ca4.png" alt="">
