# Cinemática de los Fluidos: Viscosidad (Unidad 5)
## Análisis de la Viscosidad y Comportamiento de Fluidos

La viscosidad, definida como la resistencia a la deformación cortante originada por fuerzas intermoleculares, es la propiedad central de este análisis. Mientras que los **fluidos newtonianos** mantienen una viscosidad constante ante variaciones en el gradiente de velocidad, los **fluidos no newtonianos** presentan una viscosidad aparente que depende de factores como el esfuerzo de corte, el tiempo de aplicación y la historia cinemática del fluido. 

El informe detalla las clasificaciones de estos fluidos (independientes del tiempo, dependientes del tiempo y viscoelásticos), los modelos matemáticos que describen su comportamiento (Ley de la Potencia, Carreau, Cross, entre otros) y las implicaciones dinámicas de su flujo en conducciones industriales, destacando fenómenos como el **"flujo pistón"** en materiales viscoplásticos.

---

## 1. Fundamentos de la Viscosidad y la Ley de Newton

La viscosidad es la medida de la resistencia de un fluido a la deformación cortante o angular. Su origen reside en las fuerzas intermoleculares del material.

### 1.1. La Experiencia de las Dos Placas
El comportamiento básico se describe mediante un sistema de dos placas separadas por una distancia $y_0$ con un fluido entre ellas:
* **Placa inferior:** Se mantiene fija.
* **Placa superior:** Se desplaza a una velocidad $v_0$ mediante una fuerza $F$.
* **Adhesión:** Debido a las fuerzas de adhesión, la capa de líquido en contacto con cada placa adquiere la velocidad de la misma, creando un gradiente de velocidades entre $0$ y $v_0$.



### 1.2. Ley de Newton de la Viscosidad
La relación entre la fuerza aplicada y la velocidad se expresa como:

$$\tau = \mu \cdot \frac{dv}{dy}$$

**Donde:**
* **$\tau$ (Esfuerzo de corte):** Relación entre la fuerza ($F$) y el área ($A$).
* **$\mu$ (Coeficiente de viscosidad):** Propiedad de la sustancia que depende de la temperatura y la presión.
* **$dv/dy$:** Gradiente de velocidad.

### 1.3. Unidades y Variaciones
* **Unidades:** $Ns/m^2$, $lb \cdot s/ft^2$, o Poise ($P$). $1 P = 0.10 N \cdot s/m^2$. Se utiliza frecuentemente el centipoise ($cP$).
* **Referencia:** El agua tiene una viscosidad de $1 cP$ a $15 °C$.
* **Efecto térmico:** La viscosidad disminuye en líquidos al aumentar la temperatura, mientras que en los gases aumenta.

---

## 2. Clasificación de los Fluidos

La distinción principal se basa en si la relación entre el esfuerzo de corte ($\tau$) y el gradiente de velocidad es lineal o no.

| Categoría | Características |
| :--- | :--- |
| **Fluidos Newtonianos** | $\mu$ es constante. Incluye gases, líquidos de bajo peso molecular (agua, petróleo) y soluciones acuosas simples. |
| **Fluidos No Newtonianos** | $\mu$ es variable (viscosidad aparente). El flujo depende de la geometría, el esfuerzo y, a veces, del tiempo. |

### Grupos de Fluidos No Newtonianos
1.  **Independientes del tiempo:** La velocidad de corte depende solo del esfuerzo en ese instante (fluidos puramente viscosos).
2.  **Dependientes del tiempo:** La relación depende de la duración del esfuerzo y su historia cinemática.
3.  **Viscoelásticos:** Exhiben características de fluidos ideales y sólidos elásticos, con recuperación elástica parcial tras la deformación.



---

## 3. Fluidos Independientes del Tiempo: Modelos y Comportamiento

En estos fluidos, la viscosidad aparente ($\eta$) se define como la relación entre el esfuerzo de corte y la velocidad de corte en un punto dado.

### 3.1. Fluidos Pseudoplásticos
Son los más comunes. Su viscosidad aparente disminuye al aumentar la velocidad de corte.
* **Ejemplos:** Soluciones de goma, adhesivos, mayonesa, pinturas, fluidos biológicos.
* **Rango de medición:** Requieren diversos instrumentos para cubrir velocidades bajas ($\mu_0$) y altas ($\mu_\infty$).

### 3.2. Fluidos Dilatantes
Su viscosidad aumenta con el incremento de la velocidad de corte. Ocurre comúnmente en suspensiones concentradas donde la agitación provoca que el líquido deje de lubricar las partículas sólidas, aumentando la fricción.
* **Ejemplos:** Harina de maíz con azúcar, arenas movedizas, cemento húmedo.

### 3.3. Fluidos Viscoplásticos
Requieren un esfuerzo de corte inicial ($\tau_0$) para comenzar a fluir. Por debajo de este umbral, se comportan como un sólido elástico.
* **Plástico de Bingham:** Relación lineal tras superar $\tau_0$ (ej. pasta de dientes, margarina).
* **Plástico de Casson:** Comportamiento no lineal tras $\tau_0$ (ej. sangre, chocolate fundido, jugo de naranja).

---

## 4. Modelos Matemáticos de Viscosidad Aparente

### 4.1. Ley de la Potencia (Modelo de Ostwald-de Waele)
Es el modelo más utilizado debido a la abundancia de datos experimentales:

$$\tau = m \cdot \left( \frac{dv}{dy} \right)^n$$

* **$n < 1$:** Pseudoplástico.
* **$n = 1$:** Newtoniano.
* **$n > 1$:** Dilatante.
* **$m$:** Coeficiente de consistencia.

### 4.2. Otros Modelos Avanzados
* **Modelo de Carreau:** Utilizado cuando hay desviaciones importantes de la ley de potencia a velocidades de corte muy altas o muy bajas. Considera $\mu_0$ y $\mu_\infty$.
* **Modelo de Cross:** Modelo de cuatro parámetros que se reduce a la ley de potencia o al comportamiento newtoniano en sus límites.
* **Modelo de Ellis:** Modelo de tres constantes útil cuando las desviaciones de la ley de potencia solo ocurren a bajas velocidades de corte.
* **Modelo de Herschel-Bulkley:** Generalización del modelo de Bingham para curvas no lineales tras el esfuerzo inicial.

---

## 5. Datos Típicos de la Ley de Potencia ($n$ y $m$)

| Sistema | Temperatura (K) | $n$ | $m$ (Pa·s) |
| :--- | :---: | :---: | :---: |
| Puré de Manzana | 300 | 0.3 - 0.45 | 12 - 22 |
| Mayonesa | 298 | 0.6 | 5 - 100 |
| Sangre humana | 300 | 0.9 | 0.004 |
| Pasta de dientes | 298 | 0.28 | 120 |
| Polietileno (LDPE) | 433-473 | 0.45 | $4.3 - 9.4 \times 10^3$ |

---

## 6. Fluidos Dependientes del Tiempo

La viscosidad aparente cambia según el tiempo que el fluido ha estado en movimiento.
* **Tixotrópicos:** La viscosidad disminuye con el tiempo bajo una velocidad de corte constante (ej. suspensiones de bentonita). Se debe a la ruptura de uniones estructurales internas.
* **Reopécticos:** La viscosidad aumenta con el tiempo (poco comunes).
* **Histéresis:** Estos fluidos muestran ciclos de histéresis al aumentar y luego disminuir la velocidad de corte.

---

## 7. Flujo en Cañerías y Conductos

### 7.1. Perfiles de Velocidad en Flujo Laminar
El perfil de velocidades depende del índice $n$ de la ley de la potencia. Para un fluido newtoniano ($n=1$), la relación entre la velocidad central y la media es 2. En pseudoplásticos, este valor cae significativamente.



### 7.2. Flujo Pistón (Plug Flow)
Es característico de los fluidos de Bingham. Debido al esfuerzo de corte inicial ($\tau_0$):
* **Zona Central (Núcleo):** Donde el esfuerzo de corte es menor que $\tau_0$, el fluido se desplaza como un sólido rígido con velocidad uniforme.
* **Zona Anular:** Entre el núcleo y la pared, el esfuerzo supera $\tau_0$, y el fluido fluye con un perfil curvo debido a los efectos viscosos.

### 7.3. Número de Reynolds ($Re_{PL}$)
Se define un número de Reynolds específico para fluidos que siguen la ley de potencia para mantener una estructura similar a las ecuaciones de pérdida de carga de fluidos newtonianos, permitiendo el cálculo del factor de fricción ($f$).

