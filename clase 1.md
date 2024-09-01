# Introducción al Control Digital

En esta clase, exploraremos los conceptos fundamentales del control digital, un campo que se centra en el uso de señales digitales para controlar sistemas físicos. Veremos cómo se comparan las señales digitales con las analógicas, la estructura de un controlador digital, y el proceso de conversión de señales análogas a digitales. Este conocimiento es clave para entender la implementación de sistemas de control en entornos modernos, donde la exactitud, la flexibilidad y los costos juegan un papel crucial.

## 1. Señales Digitales vs Analógicas

### 1.1. Definición de Señales Digitales
Las señales digitales son aquellas que tienen solo dos posibles valores o estados, comúnmente representados como "0" y "1". Su forma de onda es cuadrada.

### 1.2. Definición de Señales Analógicas
Las señales analógicas son continuas y pueden tomar cualquier valor dentro de un rango definido en el dominio del tiempo.

🔑 **Definición**: Una *señal digital* es una señal que solo puede tener dos valores discretos, mientras que una *señal analógica* es una señal continua que puede variar dentro de un rango.

## 2. Por qué Control Digital

El control digital se prefiere en muchas aplicaciones debido a su exactitud, la capacidad de implementar controladores complejos sin errores de implementación, flexibilidad en la programación y ajustes, mayor velocidad de procesamiento, y reducción de costos en comparación con los sistemas analógicos.

## 3. Estructura del Controlador Digital

### 3.1. Estructura del Controlador
En un sistema de control digital, se utilizan conversores A/D (Análogo-Digital) para transformar las señales analógicas de la planta en señales digitales que pueden ser procesadas por un computador. Luego, un conversor D/A (Digital-Análogo) transforma las señales digitales de vuelta a analógicas para actuar sobre la planta.

## 4. Procedimiento de Conversión

### 4.1. Muestreo
El muestreo es el proceso de medir los valores de voltaje de una señal analógica a intervalos regulares. La frecuencia de muestreo se mide en Hz.

💡 **Ejemplo 1**: Si se mide una señal a 1000 Hz, significa que se toman 1000 muestras por segundo.

### 4.2. Cuantización
La cuantización convierte la señal analógica muestreada en una serie de valores discretos.

🔑 **Definición**: *Cuantización* es el proceso de asignar valores discretos a las muestras de una señal analógica.

### 4.3. Codificación
La codificación asigna valores binarios a los valores cuantizados.

## 5. Ejemplos

💡 **Ejemplo 2**: Codificación de una señal con un rango de [0, 3] V usando 2 bits.
- 0 V → 00
- 0,75 V → 01
- 1,5 V → 10
- 2,25 V → 11

## 6. Consideraciones Prácticas

Los conversores A/D comerciales están limitados en cuanto al rango de voltajes que pueden convertir. Además, es crucial considerar los tiempos de muestreo y cuantización para evitar errores de sincronización en la conversión de señales.

## 7. Conversión Digital a Análoga

Un conversor D/A convierte señales digitales en valores análogos correspondientes. La resolución del conversor depende del número de bits utilizados en la representación digital.

💡 **Ejemplo 3**: Un conversor D/A de 4 bits con un rango de 0 a 15V puede representar la señal con una resolución de 1V.

## 8. Métodos de Conversión

### 8.1. Resistores Ponderados
Este método es simple pero no muy exacto. Se basa en el uso de resistencias de diferentes valores para generar la señal análoga.

### 8.2. Red de Escalera R-2R
Este método es más exacto y utiliza una configuración en escalera de resistencias R y 2R.

## 9. Ejercicios

### 📚 Ejercicio 1

**Enunciado**: Dada una señal analógica con un rango de voltaje de 0 a 3 V, que es muestreada y cuantizada usando un convertidor A/D de 3 bits, determine los niveles de cuantización y las representaciones binarias correspondientes para cada nivel.

**Solución**:

1. **Número de niveles de cuantización**:  
   Dado que el convertidor A/D es de 3 bits, el número total de niveles de cuantización es \(2^3 = 8\).

2. **Rango total**:  
   El rango de voltaje es de 0 a 3 V.

3. **Tamaño de cada paso de cuantización**:  
   \[
   \text{Tamaño del paso} = \frac{\text{Rango total}}{\text{Número de niveles}} = \frac{3 \text{ V}}{8} = 0.375 \text{ V}
   \]

4. **Niveles de cuantización y representación binaria**:

   | Nivel | Rango de Voltaje (V) | Representación Binaria |
   |-------|----------------------|------------------------|
   | 0     | 0.000 - 0.375        | 000                    |
   | 1     | 0.375 - 0.750        | 001                    |
   | 2     | 0.750 - 1.125        | 010                    |
   | 3     | 1.125 - 1.500        | 011                    |
   | 4     | 1.500 - 1.875        | 100                    |
   | 5     | 1.875 - 2.250        | 101                    |
   | 6     | 2.250 - 2.625        | 110                    |
   | 7     | 2.625 - 3.000        | 111                    |

**Conclusión**: Para cada rango de voltaje, se asigna una representación binaria correspondiente en el convertidor A/D de 3 bits.

---

### 📚 Ejercicio 2

**Enunciado**: Si un convertidor D/A tiene un rango de entrada de 0 a 15 V y se utilizan 4 bits para la conversión, determine la resolución del convertidor y la salida correspondiente para una entrada digital de 1010.

**Solución**:

1. **Resolución del convertidor**:  
   La resolución se calcula como:

   \[
   \text{Resolución} = \frac{\text{Rango total}}{2^n} = \frac{15 \text{ V}}{2^4} = \frac{15 \text{ V}}{16} = 0.9375 \text{ V}
   \]

2. **Cálculo de la salida para 1010**:  
   Convertimos el valor binario 1010 a decimal, que es 10. Luego, la salida es:

   \[
   \text{Salida} = \text{Resolución} \times \text{Valor decimal} = 0.9375 \text{ V} \times 10 = 9.375 \text{ V}
   \]

**Conclusión**: La salida correspondiente para una entrada digital de 1010 es 9.375 V.

---

## 10. Conclusiones

En esta clase hemos abordado los fundamentos del control digital, explorando las diferencias entre señales digitales y analógicas, y los pasos necesarios para convertir una señal análoga en digital y viceversa. También hemos discutido la importancia de la frecuencia de muestreo y la codificación en la precisión del control digital.

## 11. Referencias

- Ogata, K. *Sistemas de control en tiempo discreto*. Prentice Hall, 2nd edition, 1996.
- Visioli, A. *Digital Control Engineering*. Elsevier, 2nd edition, 2013.
- Kuo, B. *Sistemas de control Digital*. México DF, 1992.