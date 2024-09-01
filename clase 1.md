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

### 📚 **Ejercicio 1**: Diseñe un circuito con un conversor D/A utilizando una red de escalera R-2R y determine la salida analógica para una entrada digital de 1011.

**Solución**:
1. Asumir valores para R y 2R.
2. Calcular la salida utilizando la fórmula del circuito.

### 📚 **Ejercicio 2**: Explique el impacto de la frecuencia de muestreo en la calidad de la conversión de señales análogas a digitales.

**Solución**:
- Mayor frecuencia de muestreo mejora la fidelidad de la señal digital, mientras que una frecuencia baja puede causar pérdida de información.

## 10. Conclusiones

En esta clase hemos abordado los fundamentos del control digital, explorando las diferencias entre señales digitales y analógicas, y los pasos necesarios para convertir una señal análoga en digital y viceversa. También hemos discutido la importancia de la frecuencia de muestreo y la codificación en la precisión del control digital.

## 11. Referencias

- Ogata, K. *Sistemas de control en tiempo discreto*. Prentice Hall, 2nd edition, 1996.
- Visioli, A. *Digital Control Engineering*. Elsevier, 2nd edition, 2013.
- Kuo, B. *Sistemas de control Digital*. México DF, 1992.