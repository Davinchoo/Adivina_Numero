# Adivinar Números - Juego en PSeInt

Este es un sencillo programa en **PSeInt** que implementa un juego de adivinación de números. El objetivo del juego es que el jugador adivine un número secreto generado aleatoriamente por la computadora dentro de un rango determinado.

## Descripción

En este juego, el programa genera un número aleatorio dentro de un rango específico (por ejemplo, entre 1 y 100). El jugador debe ingresar sus conjeturas (números) hasta adivinar correctamente el número secreto. El programa proporciona retroalimentación sobre si el número ingresado es mayor o menor que el número secreto, y también cuenta la cantidad de intentos realizados.

## Funcionalidades

- El programa genera un número aleatorio dentro de un rango predefinido.
- El jugador realiza intentos para adivinar el número.
- El programa informa si el número ingresado es mayor, menor o igual al número secreto.
- El juego termina cuando el jugador adivina correctamente el número.
- El programa muestra el número de intentos realizados.

## Instrucciones para Ejecutar

1. **Descargar e instalar PSeInt**:
   Si aún no tienes PSeInt, puedes descargarlo desde su [sitio web oficial](https://pseint.sourceforge.io/).

2. **Abrir el archivo en PSeInt**:
   Una vez descargado el archivo de este proyecto, abre PSeInt y carga el archivo con extensión `.pseint` para comenzar.

3. **Ejecutar el programa**:
   Presiona el botón de ejecutar en PSeInt para iniciar el juego de adivinación.

## Código Fuente

El código principal se encuentra en el archivo `Adivinar_Numero.pseint`, el cual sigue la siguiente estructura básica:

```pseudocode
Proceso Adivina_Numero

    intentos<-10
    num_secreto <- azar(100)+1
    
    Escribir "Adivine el numero (de 1 a 100):"
    Leer num_ingresado
    Mientras num_secreto<>num_ingresado Y intentos>1 Hacer
        Si num_secreto>num_ingresado Entonces
            Escribir "Muy bajo"
        Sino 
            Escribir "Muy alto"
        FinSi
        intentos <- intentos-1
        Escribir "Le quedan ",intentos," intentos:"
        Leer num_ingresado
    FinMientras
    
    Si num_secreto=num_ingresado Entonces
        Escribir "Exacto! Usted adivino en ",11-intentos," intentos."
    Sino
        Escribir "El numero era: ",num_secreto
    FinSi
    
FinProceso
