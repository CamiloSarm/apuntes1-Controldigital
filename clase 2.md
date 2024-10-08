# Transformada Z y Función de Transferencia

En esta clase, exploraremos la transformada Z, una herramienta esencial en el análisis y diseño de sistemas de control digital. Veremos cómo se aplica la transformada Z para resolver ecuaciones en diferencias, cómo se relaciona con la transformada de Laplace y cómo se puede utilizar para obtener funciones de transferencia en el dominio Z. Estos conceptos son fundamentales para el análisis de sistemas discretos.

## 1. Muestreo en Términos Matemáticos

### 1.1. Función en Términos de Muestras
Cuando se tiene una función continua \(f(t)\), se puede expresar su equivalente discreto mediante el muestreo. El periodo de muestreo \(T\) define la frecuencia con la que se toman las muestras de la señal continua.

🔑 **Definición**: El *muestreo* es el proceso de convertir una señal continua en una secuencia de valores discretos tomados a intervalos regulares.

## 2. Ecuaciones en Diferencias

Las ecuaciones en diferencias son la contraparte discreta de las ecuaciones diferenciales en sistemas continuos. Representan el comportamiento dinámico de un sistema en términos de sus señales de entrada y salida.

### 2.1. Características de las Ecuaciones en Diferencias
Estas ecuaciones pueden ser lineales, no lineales, homogéneas o inhomogéneas, y variantes o invariantes en el tiempo.

## 3. Solución de Ecuaciones en Diferencias

### 3.1. Métodos Iterativos
La solución por métodos iterativos da los valores de la salida \(y(k)\) para un número finito de muestras.

💡 **Ejemplo 1**:
Dada la ecuación:
\[ y_k = \frac{1}{3}(-2y_{k-1} + y_{k-2} + 2u_{k-1} - 3u_{k-2}) \]
Con condiciones iniciales:
\[ y_{-2} = 1; y_{-1} = -2 \]
Calcula \(y_0\).

### 3.2. Transformada Z
La transformada Z proporciona una expresión matemática para la solución de la ecuación en cualquier muestra.

## 4. Transformada Z

La transformada Z es la contraparte discreta de la transformada de Laplace y es fundamental para el análisis de sistemas discretos.

### 4.1. Relación Z y L
La transformada Z se relaciona con la transformada de Laplace en que ambas transformadas convierten ecuaciones diferenciales o en diferencias en funciones algebraicas.

## 5. Función de Transferencia en el Dominio Z

### 5.1. Definición
La función de transferencia en el dominio Z es la relación entre la salida y la entrada muestreadas de un sistema dinámico.

🔑 **Definición**: Una *función de transferencia* en el dominio Z describe la relación entre la entrada y la salida de un sistema en función de la variable \(z\).

💡 **Ejemplo 2**:
Dada la ecuación:
\[ 3y(k) + 2y(k-1) - y(k-2) = 2u(k-1) - 3u(k-2) \]
Obtener la función de transferencia.

## 6. Sistemas Causales y No Causales

### 6.1. Sistemas No Causales
Un sistema no causal es aquel que responde antes de que se aplique la entrada.

### 6.2. Sistemas Causales
Un sistema causal solo responde después de que se aplica la entrada.

## 7. Ejercicios

### 📚 Ejercicio 1

**Enunciado**: Dada la siguiente ecuación en diferencias:

\[
y[k+2] + 0.8y[k+1] + 0.07y[k] = u[k-1]
\]

Aplicar la transformada Z para encontrar la función de transferencia del sistema.

**Solución**:

1. **Aplicación de la transformada Z**:  
   Aplicamos la transformada Z a ambos lados de la ecuación:

   \[
   Z\{y[k+2]\} + 0.8Z\{y[k+1]\} + 0.07Z\{y[k]\} = Z\{u[k-1]\}
   \]

   Utilizando las propiedades de la transformada Z:

   \[
   z^2Y(z) + 0.8zY(z) + 0.07Y(z) = z^{-1}U(z)
   \]

2. **Factorización y despeje**:

   \[
   Y(z)(z^2 + 0.8z + 0.07) = z^{-1}U(z)
   \]

   La función de transferencia es:

   \[
   H(z) = \frac{Y(z)}{U(z)} = \frac{z^{-1}}{z^2 + 0.8z + 0.07}
   \]

**Conclusión**: La función de transferencia del sistema, obtenida mediante la transformada Z, es:

\[
H(z) = \frac{z^{-1}}{z^2 + 0.8z + 0.07}
\]

---

### 📚 Ejercicio 2

**Enunciado**: Determine la salida de un sistema discreto cuya función de transferencia es \(H(z) = \frac{z-0.5}{z^2 - 1.8z + 0.81}\), para una entrada en escalón unitario \(u[k] = 1\).

**Solución**:

1. **Expansión en fracciones parciales**:

   \[
   H(z) = \frac{z-0.5}{(z-0.9)(z-0.9)}
   \]

   Expandimos en fracciones parciales:

   \[
   H(z) = \frac{A}{z-0.9} + \frac{B}{(z-0.9)^2}
   \]

   Resolviendo para \(A\) y \(B\):

   \[
   A = 1, \quad B = 0.5
   \]

2. **Respuesta del sistema**:

   La salida \(y[k]\) se obtiene aplicando la transformada Z inversa:

   \[
   y[k] = 1 \cdot 0.9^k + 0.5k \cdot 0.9^k
   \]

**Conclusión**: La salida del sistema es \(y[k] = 0.9^k + 0.5k \cdot 0.9^k\).

---

## 8. Conclusiones

En esta clase, hemos aprendido sobre la transformada Z y su aplicación en la resolución de ecuaciones en diferencias. También hemos discutido la importancia de las funciones de transferencia en el dominio Z para el análisis de sistemas discretos.

## 9. Referencias

- Chen, C.-T. *Analog and Digital Control Design*. Saunders College Publishing.
- Barrero Mendoza, O. *Sistemas de control digital*. Universidad de Ibagué, 2021.