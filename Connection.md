Creador: whitecr0wz

Miramos la IP:
![2021-08-18_13-08-1629287067](https://user-images.githubusercontent.com/82907557/129892449-36ab8994-5f1c-42f6-8047-969c13322c3d.jpg)

Enumeración:
![2021-08-18_13-08-1629287265](https://user-images.githubusercontent.com/82907557/129892897-02db6d19-1cdb-40c7-90fb-74a1b9781cf2.jpg)

Vemos un servidor ssh, http y samba.
Vamos directo al samba para echarle un ojo.
![2021-08-18_13-08-1629287468](https://user-images.githubusercontent.com/82907557/129893383-d402a7ad-407f-478f-94fe-b9d61141670a.jpg)

Explotación: 

Vemos que hay un directorio llamada share. Vamos a listarlo.

![2021-08-18_13-08-1629287603](https://user-images.githubusercontent.com/82907557/129893599-a21bb275-c0e3-481b-986a-9d47f39a6257.jpg)

Vemos que index.html lo esta cargando desde el propio servidor. Podemos aprovechar eso para subir una reverse shell.

![2021-08-18_13-08-1629287923](https://user-images.githubusercontent.com/82907557/129894291-33930e84-d821-4eb9-b48b-d16bcdfbaed7.jpg)

Bien! Ya hemos obtenido acceso. Hacemos el típico tratamiento de la TTY!

![2021-08-18_14-08-1629288124](https://user-images.githubusercontent.com/82907557/129895793-99e2e799-ec01-4ba9-83e9-207bfa196a12.jpg)

Ya tenemos local.txt. Ahora vamos ha hacer la privesc. Enumerando binarios SUID encontramos gdb.

![2021-08-18_14-08-1629288369](https://user-images.githubusercontent.com/82907557/129895252-9472048e-4755-4bc1-b09c-312896cbf806.jpg)


Miramos en gftobins como explotarlo, lo hacemos. Y ya estariamos como root.

![2021-08-18_14-08-1629288507](https://user-images.githubusercontent.com/82907557/129895564-26b90e39-d06d-48fa-b2d4-ecf3fd0fc141.jpg)

Maquina bastante fácil.
