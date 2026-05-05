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

## 8. Número de Reynolds ($Re$) en Fluidos Newtonianos y No Newtonianos

La fórmula del número de Reynolds ($Re$) varía dependiendo del tipo de fluido y la geometría del sistema. En términos generales, cuantifica la relación entre las **fuerzas de inercia** y las **fuerzas viscosas**.

---

### 8.1 Fluidos Newtonianos
Para estos fluidos, la fórmula general es:

$$Re = \frac{L \cdot V}{\gamma} = \frac{\rho \cdot L \cdot V}{\mu}$$

**Donde:**
*   **$\rho$**: Densidad del fluido.
*   **$V$**: Velocidad del fluido.
*   **$L$ (o $D$)**: Longitud característica (por ejemplo, el diámetro $D$ en una cañería o la longitud $L$ en una placa plana).
*   **$\mu$**: Viscosidad dinámica.
*   **$\gamma$**: Viscosidad cinemática ($\mu/\rho$).

---

### 8.2. Fluidos No Newtonianos
Para fluidos que no siguen la ley de Newton de la viscosidad, se utilizan adaptaciones para mantener una estructura similar en las ecuaciones de flujo:

### Modelo de Ley de Potencia (Pseudoplásticos)
Se define un número de Reynolds específico ($Re_{PL}$):

$$Re_{PL} = \frac{\rho V^{2-n} D^n}{8^{n-1} m \left(\frac{3n+1}{4n}\right)^n}$$

Donde **$n$** es el índice de comportamiento y **$m$** es el coeficiente de consistencia.

### Plásticos de Bingham
Se utiliza el número de Reynolds de Bingham ($Re_B$):

$$Re_B = \frac{\rho V D}{\mu_B}$$

Donde **$\mu_B$** es la viscosidad plástica.

### Número de Reynolds Generalizado ($Re_{MR}$)
Utilizado para fluidos independientes del tiempo en cañerías circulares:

$$Re_{MR} = \frac{\rho V^{2-n'} D^{n'}}{8^{n'-1} m'}$$

Aquí, **$n'$** y **$m'$** son parámetros experimentales obtenidos de la curva de esfuerzo de corte.

### Modelo de Herschel-Bulkley
Para este modelo se utiliza una versión modificada ($Re_{mod}$):

$$Re_{mod} = \frac{8 \rho V_{ann}^2}{\tau_0^H + m \left(\frac{8 V_{ann}}{D_{shear}}\right)^n}$$

---

### 8.3 Regímenes de Flujo
Independientemente del fluido, el número de Reynolds determina el tipo de régimen en una cañería:

*   **Laminar:** $Re < 2100$.
*   **Transición:** $2100 < Re < 4000$.
*   **Turbulento:** $Re > 4000$.

---

### 9. La Capa Límite
La **capa límite** se define como la zona donde se manifiesta la influencia de la viscosidad del fluido [1]. En esta región, la velocidad del fluido se ve afectada por las fuerzas cortantes, variando desde cero en la pared (condición de no deslizamiento) hasta alcanzar la velocidad de la corriente libre [1, 2].

### 10. Subcapa Laminar
Incluso cuando el flujo general es **turbulento**, siempre existe una delgada **subcapa laminar** pegada a las paredes del conducto o superficie [3]. 

Esta subcapa es crítica para determinar la naturaleza de la fricción:
*   **Comportamiento liso:** Si la subcapa laminar es lo suficientemente gruesa como para cubrir las irregularidades (rugosidades) de la pared, la cañería se comporta como si fuera lisa [3].
*   **Comportamiento rugoso:** Si las rugosidades sobresalen de esta subcapa, el conducto se considera hidráulicamente rugoso [3].

### 11. La Rugosidad y su Impacto
La rugosidad de una superficie altera significativamente la resistencia al avance del fluido.

## Coeficiente de Arrastre ($C_d$)
El impacto de la rugosidad se puede observar en el coeficiente de arrastre. Por ejemplo, para una esfera con un número de Reynolds de $10^6$:
*   **Esfera lisa:** Presenta un $C_d$ de **0,1** [4, 5].
*   **Esfera rugosa:** Presenta un $C_d$ mucho mayor, de **0,48** [5].

## Resistencia al Movimiento
La resistencia total que se opone al movimiento tiene dos orígenes principales relacionados con la capa límite:
1.  **Resistencia de superficie:** Debida directamente a la existencia de la capa límite y la fricción viscosa [6].
2.  **Resistencia de forma:** Debida al desprendimiento de la capa límite, lo que genera zonas de baja presión detrás del objeto [6].

## Aplicación en Conductos
En el diseño industrial, el uso de superficies con distintas texturas altera el flujo. Por ejemplo, el paso de burbujas de aire es diferente si se utilizan tubos de cristal **lisos** en comparación con tubos **corrugados** (rugosos) [7]. En regímenes turbulentos para fluidos no newtonianos, se suelen adaptar fórmulas como la de Darcy-Weisbach considerando las variaciones en el coeficiente de fricción provocadas por estas condiciones de superficie [8, 9].

---

# Guía de Estudio: Mecánica de Fluidos No Newtonianos

Esta guía ha sido diseñada para proporcionar una revisión exhaustiva de los principios de la reología y el comportamiento de los fluidos no newtonianos, basándose en los fundamentos de la viscosidad, los modelos matemáticos de flujo y las aplicaciones industriales y biológicas.

---

## I. Cuestionario de Repaso (Respuestas Cortas)

**Instrucciones:** Responda a las siguientes preguntas utilizando la información técnica proporcionada en el material de origen. Cada respuesta debe tener una extensión de 2 a 3 oraciones.

1.  ¿Cómo se define la viscosidad de un fluido y cuál es su origen físico?
2.  ¿Cuál es la diferencia fundamental entre un fluido newtoniano y uno no newtoniano?
3.  ¿Qué es la "viscosidad aparente" y por qué es necesaria en el estudio de fluidos no newtonianos?
4.  Describa las características principales de un fluido pseudoplástico y mencione dos ejemplos.
5.  ¿En qué consiste el comportamiento de un fluido dilatante y cuál es la explicación física de este fenómeno?
6.  ¿Qué es el "esfuerzo de corte inicial" (tensión de fluencia) en los fluidos viscoplásticos?
7.  Explique la diferencia entre los fluidos dependientes del tiempo: tixotrópicos y reopécticos.
8.  ¿Cómo afecta la temperatura a la viscosidad en líquidos frente a los gases?
9.  ¿Qué se entiende por "flujo pistón" en el contexto de fluidos de Bingham en tuberías?
10. Dentro del modelo de la ley de potencia (Oswald-de Waele), ¿qué representan los parámetros $n$ y $m$?

---

## II. Clave de Respuestas

1.  **Definición de viscosidad:** Es la medida de la resistencia de un fluido a la deformación cortante o angular. Su origen se encuentra en las fuerzas intermoleculares que actúan dentro de la sustancia.
2.  **Diferencia fundamental:** En los fluidos newtonianos, la viscosidad es constante independientemente del gradiente de velocidad. En cambio, en los no newtonianos, la viscosidad es variable y depende de las condiciones de flujo, como el esfuerzo de corte o el tiempo.
3.  **Viscosidad aparente:** Se define como la relación entre el esfuerzo de corte y la velocidad de corte en un punto determinado. Es necesaria porque permite aplicar la estructura de la ecuación de Newton a fluidos donde la viscosidad cambia según el gradiente de velocidad.
4.  **Fluidos pseudoplásticos:** Son aquellos cuya viscosidad aparente disminuye al aumentar la velocidad de corte, siendo el tipo más común de fluido no newtoniano. Ejemplos típicos incluyen la mayonesa, las pinturas y las soluciones de polímeros.
5.  **Fluidos dilatantes:** Son fluidos donde la viscosidad aumenta al incrementar la velocidad de corte. Esto ocurre frecuentemente en suspensiones concentradas donde, al agitarse, el líquido deja de lubricar todas las partículas, aumentando la fricción interna.
6.  **Esfuerzo de corte inicial ($\tau_0$):** Es un valor mínimo de tensión que debe excederse para que el material comience a fluir. Por debajo de este umbral, el material se comporta elásticamente como un sólido.
7.  **Tixotrópicos vs. Reopécticos:** En los fluidos tixotrópicos, la viscosidad aparente disminuye con el tiempo bajo un esfuerzo constante debido a la ruptura de uniones estructurales. En los reopécticos, sucede lo contrario, y la viscosidad aumenta con la duración del esfuerzo.
8.  **Efecto de la temperatura:** La viscosidad disminuye al aumentar la temperatura en los líquidos, mientras que en los gases la viscosidad aumenta con el incremento de la temperatura.
9.  **Flujo pistón:** Es un fenómeno que ocurre en la zona central de una tubería donde el esfuerzo de corte es menor al límite de fluencia del fluido. Esta zona se desplaza como un bloque sólido rodeado por un anillo de fluido que sí presenta un perfil de velocidad curvo.
10.  **Parámetros $n$ y $m$:** El parámetro $n$ es el índice de comportamiento (determina si es pseudoplástico, newtoniano o dilatante), mientras que $m$ es el coeficiente de consistencia del fluido, un parámetro empírico de ajuste.

---

## III. Glosario de Términos Clave

*   **Agregados de cemento:** Ejemplo de fluido dilatante cuando está húmedo, donde la viscosidad sube con la agitación.
*   **Centipoise (cP):** Unidad de viscosidad equivalente a 0,01 Poise; la viscosidad del agua a 15 °C es de aproximadamente 1 cP.
*   **Coeficiente de consistencia ($m$):** Parámetro experimental en la ley de potencia que indica cuán "espeso" es el fluido bajo condiciones específicas.
*   **Esfuerzo de corte ($\tau$):** Fuerza aplicada por unidad de área tangencial a la dirección del flujo.
*   **Fluido de Bingham:** Sustancia que requiere un esfuerzo inicial para fluir y luego presenta una relación lineal entre el esfuerzo y el gradiente de velocidad.
*   **Fluido de Casson:** Modelo común para materiales biológicos (sangre) y pastas alimenticias, caracterizado por un comportamiento viscoplástico no lineal.
*   **Fluido viscoelástico:** Material que muestra recuperación elástica parcial después de una deformación, combinando propiedades de fluidos ideales y sólidos elásticos.
*   **Gradiente de velocidad ($dv/dy$):** Cambio de la velocidad del fluido con respecto a la distancia perpendicular a la dirección del flujo; también llamado velocidad de corte.
*   **Histéresis:** Fenómeno observado en fluidos dependientes del tiempo donde la curva de esfuerzo de corte al aumentar la velocidad no coincide con la curva al disminuirla.
*   **Índice de comportamiento ($n$):** Exponente en la ley de potencia que clasifica al fluido como pseudoplástico ($n < 1$), newtoniano ($n = 1$) o dilatante ($n > 1$).
*   **Ley de Newton de la viscosidad:** Ecuación que establece que el esfuerzo de corte es directamente proporcional al gradiente de velocidad ($\tau = \mu \cdot dv/dy$).
*   **Lodo rojo:** Ejemplo industrial de una suspensión residual (industria del aluminio) que presenta comportamiento dependiente del tiempo.
*   **Número de Reynolds para fluidos no newtonianos ($Re_{PL}$):** Adaptación del número de Reynolds tradicional que utiliza parámetros de la ley de potencia para predecir regímenes de flujo.
*   **Poise (P):** Unidad de viscosidad en el sistema CGS, equivalente a $0,10 \text{ N}\cdot\text{s}/\text{m}^2$.
*   **Yield pseudoplastic:** Material viscoplástico que, una vez superado el esfuerzo inicial, sigue un comportamiento curvo (no lineal) en su flujo.
