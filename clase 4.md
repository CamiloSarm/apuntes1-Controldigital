# Estabilidad en Sistemas Discretos

En esta clase, abordaremos el tema de la estabilidad en sistemas discretos, un concepto crucial en el control digital. La estabilidad se refiere a la capacidad de un sistema para producir una salida limitada cuando se le aplica una entrada limitada. En el contexto de sistemas discretos, la estabilidad se analiza principalmente a través de la ubicación de los polos en el plano Z, diferenciándose del análisis en el dominio continuo con la transformada de LaPlace.

## 1. Concepto de Estabilidad Absoluta

La estabilidad absoluta en sistemas discretos se determina evaluando la respuesta del sistema ante una entrada tipo escalón. Si la respuesta tiene las mismas características que la entrada, el sistema se considera estable. En este contexto, la posición de los polos en el plano Z juega un papel fundamental, ya que estos deben estar dentro del círculo unitario para garantizar la estabilidad.

## 2. Espacio LaPlace vs Espacio Z

El análisis de estabilidad difiere cuando se utiliza la transformada de LaPlace en comparación con la transformada Z:

- **Transformada de LaPlace:** La estabilidad se analiza en un plano complejo donde la frontera de estabilidad está definida por el eje vertical.
- **Transformada Z:** La estabilidad está relacionada con la ubicación de los polos en un círculo unitario.

> 🔑 **_Estabilidad_:** Capacidad de un sistema para producir una salida limitada a partir de una entrada limitada, manteniendo sus polos dentro del círculo unitario en el plano Z.

## 3. Ejemplos de Estabilidad

### 3.1 Ejemplo 1: Ubicación de Polos

Dado un sistema con la siguiente función de transferencia:

$$ G(z) = \frac{4}{z^3 - 7.8z^2 + 13.4z + 3} $$

Al resolver el polinomio característico:

$$ z^3 - 7.8z^2 + 13.4z + 3 = 0 $$

Se encuentran los polos en \(z = 5\), \(z = 3\), y \(z = 0.2\). Como dos de los polos están fuera del círculo unitario, el sistema es inestable.

💡**Ejemplo 1**: Demostración de un sistema inestable con polos fuera del círculo unitario.

### 3.2 Ejemplo 2: Ubicación de Polos

Para otro sistema con la función de transferencia:

$$ G(z) = \frac{z - 3}{z^3 - 1.5z^2 + 0.66z - 0.08} $$

Los polos encontrados en \(z = 0.5\), \(z = 0.8\), y \(z = 0.2\) están todos dentro del círculo unitario, lo que indica que el sistema es estable.

💡**Ejemplo 2**: Ilustración de un sistema estable con todos los polos dentro del círculo unitario.

## 4. Estabilidad Asintótica y BIBO

- **Estabilidad Asintótica:** Un sistema es asintóticamente estable si su respuesta a cualquier condición inicial tiende a cero con el tiempo.
- **Estabilidad BIBO (Bounded Input, Bounded Output):** Un sistema es BIBO estable si su respuesta a una entrada acotada permanece acotada.

> 🔑 **_Estabilidad BIBO_:** La propiedad de un sistema donde para cualquier entrada acotada, la salida también es acotada.

## 5. Análisis de Estabilidad usando el Criterio de Jury

El criterio de Jury se aplica para evaluar la estabilidad de sistemas discretos mediante un conjunto de condiciones que deben cumplirse para que el sistema sea considerado estable.

💡**Ejemplo 3**: Uso del criterio de Jury para determinar la estabilidad de un sistema dado.

## 6. Ejercicios

📚**Ejercicio 1**: Dado el sistema con función de transferencia \(G(z) = \frac{2z + 1}{z^2 - 1.2z + 0.36}\), determinar si el sistema es estable.

**Solución**: Resolver el polinomio característico y verificar la ubicación de los polos respecto al círculo unitario.

📚**Ejercicio 2**: Aplicar el criterio de Jury al polinomio característico \(z^3 - 2z^2 + 1.5z - 0.5 = 0\) y determinar si el sistema es estable.

**Solución**: Evaluar las condiciones del criterio de Jury para confirmar la estabilidad.

## 7. Conclusiones

En esta clase, hemos aprendido a identificar la estabilidad en sistemas discretos mediante la ubicación de polos en el plano Z y la aplicación del criterio de Jury. Estos conceptos son esenciales para el diseño y análisis de sistemas de control digital.

## 8. Referencias

- Visioli, A. *Digital Control Engineering*, 2nd Edition, Elsevier, 2013.
- Material complementario sobre estabilidad de sistemas en el dominio Z.