# Sistemas Digitales para las Comunicaciones
## TP5


1 - Generar un script de octave, python, matlab, o cualquier otro lenguaje similar que implemente el sistema.
La señal b es una secuencia binaria aleatoria. Toma los valores 0 y 1, o alternativamente -1 y 1.

Script en python:


![1-script](https://user-images.githubusercontent.com/33461466/156263982-38357e30-5789-47a4-9430-fbea68ffc933.PNG)

Real:
![1- Real](https://user-images.githubusercontent.com/33461466/156263999-4272882f-4e25-4fdb-9505-059ca264e022.PNG)

Imaginario:
![2-imag](https://user-images.githubusercontent.com/33461466/156264029-e0b05aef-e8e2-40ef-b8b5-a39ec647c84c.PNG)

## La señal d inserta  M−1  ceros entre cada bit y luego le asigna un 1 al bit 1 y un -1 al bit 0. Puede tomar los vaores -1, 0 o 1.

Real:
![3-ceros](https://user-images.githubusercontent.com/33461466/156264092-55c7228b-1b0d-4de3-a6f0-dd606f16a2b1.PNG)
Imaginario:
![4-ceros Img](https://user-images.githubusercontent.com/33461466/156264098-3edc098e-2d17-4fb4-bf70-92f8b59bba2a.PNG)

## El pulso p puede tener varias formas:
Pulso raiz de coseno elevado.

![5-cosenoelevado](https://user-images.githubusercontent.com/33461466/156264211-17d3bbb7-d7c1-4eb1-85f2-7932e0566ca8.PNG)

## La señal x es la señal a transmitir por el canal, se obtiene mediante la convolución entre d y p, o realizando el filtrado mediante el filtro FIR. En cualquier caso es importante descartar los primeros  Lp−12  valores, para que las señales d y x queden "sincronizadas".

![6-scriptFIR](https://user-images.githubusercontent.com/33461466/156264274-2e3ea58c-d882-4bc9-ac29-d3ce5af6e2b0.PNG)

Real:

![7-fir real](https://user-images.githubusercontent.com/33461466/156264296-f5973a7a-3138-4318-8e0d-53cea0cdf583.PNG)
Imaginario:
![8-fir img](https://user-images.githubusercontent.com/33461466/156264309-9b189a99-e0e6-432e-ad6d-bde4eda2d35d.PNG)


## El filtro h es el equivalente de banda base del canal. Utilizaremos:
Una delta de altura unitaria con fase igual a cero (canal ideal).
Una delta de altura unitaria con fase distinta de cero.

![1-script pasa bajo](https://user-images.githubusercontent.com/33461466/156264375-9ec48d49-c3b5-42f1-b8f0-f70f4a1b7358.PNG)

Filtro Pasa bajo:
![2-pasa bajo](https://user-images.githubusercontent.com/33461466/156264384-9b1394b2-3951-48de-bcfd-f27d46c8502b.PNG)

Real:
![3-real](https://user-images.githubusercontent.com/33461466/156264413-b052212f-791f-43c8-81ba-c60f87e62f29.PNG)

Imaginario:
![4-img](https://user-images.githubusercontent.com/33461466/156264433-c504ba0b-2811-4737-b0b6-f3531bfa6129.PNG)

## La señal n representa a ruido blanco gaussiano aditivo del canal. Se puede generar con muestras de una distribución normal con media cero. Para la varianza de la distribución, considerar la relación entre el error estándard y el nivel de ruido:  σ=N0/2−−−−√  (Modulación en banda pasante).


![6-script 1](https://user-images.githubusercontent.com/33461466/156264487-9635dfd7-a104-47fd-86e1-f8d1f278e915.PNG)

![6-script 2](https://user-images.githubusercontent.com/33461466/156264493-2df200b9-5c82-4336-a04d-312a9514c72c.PNG)

Real:
![6-real](https://user-images.githubusercontent.com/33461466/156264511-bd334e40-87a1-4456-b60f-0d29f3a3e28b.PNG)

Imaginario:
![7-img](https://user-images.githubusercontent.com/33461466/156264525-07d00d2f-2706-4a83-989c-a6b765585326.PNG)

## El filtro FIR del receptor debe estar escalado para que la amplitud máxima de la señal y (sin ruido) sea igual a 1.

![image](https://user-images.githubusercontent.com/33461466/156264959-42eeeee1-2313-493b-94e7-9ff4f259dbc4.png)

![image](https://user-images.githubusercontent.com/33461466/156264990-f65c3422-c646-4bec-8915-d62459350089.png)

![image](https://user-images.githubusercontent.com/33461466/156265021-07761b56-8aee-4a51-9008-64521c4a3ee6.png)

## La señal ^b se obtiene quedándose por la muestra correcta de la señal y, es decir, realizando un subsampleo.

![image](https://user-images.githubusercontent.com/33461466/156265139-3a631464-b042-4e1a-a266-bc111f1b2a02.png)

![image](https://user-images.githubusercontent.com/33461466/156265166-3529f143-b0a0-4635-9ee7-00ea0afb7ea9.png)

![image](https://user-images.githubusercontent.com/33461466/156265187-9ea83d4b-7dbf-422e-878f-7343025142c5.png)

## 2-Para el pulso raíz de cosenos elevado elija una potencia de ruido y de manera similar al ejercicio 3, graficar las señales d, c e y (atención, y en vez de x) superpuestas en un mismo gráfico. Realice el gráfico para cada pulso del punto anterior. Verificar que las deltas coinciden con los picos de los pulsos, inclusive para el pulso raíz de coseno elevado. Realizarlo para el canal ideal.
![image](https://user-images.githubusercontent.com/33461466/156265547-ce8a6e28-91d8-40e4-a7f4-7c4ae87e8b65.png)

![image](https://user-images.githubusercontent.com/33461466/156265592-23c55a3b-14f1-4451-9746-19f29814f24c.png)

## Realizar un gráfico de MSE y BER vs la relación señal a ruido, para ello:
Para las métricas considere:
MSE: Error cuadrático medio mean((b-hat_b)^2).
BER: Bit-error rate sum(b!=hat_b)/length(b).

![image](https://user-images.githubusercontent.com/33461466/156265866-10533417-ee98-4c8f-a1ae-51c3305fb57b.png)

![image](https://user-images.githubusercontent.com/33461466/156266033-aac16f73-216a-4bdf-bdda-64abe3bd747f.png)


## La relación señal a ruido es SNR=Ps/Pn

![image](https://user-images.githubusercontent.com/33461466/156266250-66d5d8f8-a7c3-44b5-9464-52abe514de90.png)
.



