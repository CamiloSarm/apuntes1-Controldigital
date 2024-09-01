# Discretización de Controladores

En esta clase, nos enfocamos en los métodos para discretizar controladores analógicos. La discretización es fundamental cuando se implementan controladores en sistemas digitales, ya que permite transformar un sistema continuo en su equivalente discreto. Veremos varios métodos de discretización y su aplicación en el diseño de controladores.

## 1. Discretización de Señales Analógicas

### 1.1. Invarianza al Impulso
Este método utiliza la respuesta al impulso de un sistema continuo para obtener su equivalente discreto.

🔑 **Definición**: La *invarianza al impulso* es un método de discretización que preserva la respuesta al impulso de un sistema continuo en su equivalente discreto.

## 2. Invarianza al Paso

Este método se basa en la respuesta al escalón y es útil cuando se busca preservar la respuesta al escalón del sistema continuo en el sistema discreto.

💡 **Ejemplo 1**:
Dado el sistema continuo:
\[ C(s) = \frac{2s - 2}{(s + 1)(s + 3)} \]
Obtener su equivalente discreto utilizando invarianza al paso.

## 3. Métodos de Euler

### 3.1. Euler Adelante
Es una aproximación discreta de la derivada basada en la diferencia hacia adelante.

### 3.2. Euler Atrás
Es una aproximación discreta de la derivada basada en la diferencia hacia atrás.

## 4. Método Trapezoidal (Tustin)

Este método proporciona una mejor aproximación que los métodos de Euler al utilizar un promedio entre la diferencia hacia adelante y hacia atrás.

🔑 **Definición**: El *método trapezoidal* o método de Tustin es un método de discretización que utiliza un promedio entre las diferencias hacia adelante y hacia atrás para aproximar la derivada.

## 5. Teorema de Muestreo

El teorema de muestreo de Nyquist establece que la frecuencia de muestreo debe ser al menos el doble de la frecuencia más alta presente en la señal para evitar el aliasing.

## 6. Aliasing

El aliasing ocurre cuando la frecuencia de muestreo es insuficiente, causando que las altas frecuencias se confundan con las bajas.

## 7. Resumen

Existen varios métodos de discretización de controladores continuos, cada uno con sus ventajas y desventajas. La elección del método adecuado depende del sistema y de los requisitos de diseño.

## 8. Ejercicios

### 📚 **Ejercicio 1**: Utilizando el método de Tustin, discretiza el siguiente sistema:
\[ H(s) = \frac{5}{s + 2} \]

**Solución**:
Aplicando el método trapezoidal, se obtiene:
\[ H(z) = \frac{5(2)}{(2)(1 + z^{-1}) + 2} \]

### 📚 **Ejercicio 2**: Determine la estabilidad de un sistema al ser discretizado con el método de Euler hacia adelante.

## 9. Conclusiones

Hemos explorado diversos métodos de discretización, cada uno con sus características y aplicaciones específicas. Es esencial elegir el método adecuado según las necesidades del sistema para garantizar una implementación efectiva en un entorno digital.

## 10. Referencias

- Ramos, G. *Material curso Control Digital*. Universidad Nacional de Colombia, 2015.
- Visioli, A. *Digital Control Engineering*. Elsevier, 2nd edition, 2013.