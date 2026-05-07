# Resumen Integral: Flujo de Fluidos en Conductos Cerrados

Este documento sintetiza la teoría, ecuaciones y metodologías para el estudio del flujo de fluidos incompresibles (**Newtonianos y No Newtonianos**) en cañerías, basado en los materiales de la cátedra de Mecánica de los Fluidos.

---

## 1. Perfil de Velocidades en Régimen Turbulento
Cuando un fluido entra en una cañería, se forma una capa límite laminar que crece hasta volverse turbulenta, cubriendo eventualmente toda la sección (**flujo completamente desarrollado**, generalmente tras 50 diámetros).

### Estructura del Perfil
El perfil turbulento es más plano que el laminar y se divide en tres zonas:

1. **Subcapa viscosa ($\delta_l$):** Delgada capa junto a la pared donde predominan los efectos viscosos y el flujo es aproximadamente laminar.
   - **Fórmula del espesor:** $\delta_l = 14,14 \frac{D}{Re \sqrt{f}}$
2. **Capa de transición:** Zona donde conviven efectos viscosos y remolinos, extendiéndose hasta $14 \delta_l$.
3. **Zona turbulenta:** Ocupa el centro del conducto. La uniformidad de la velocidad aumenta con el número de Reynolds ($Re$).

### Ecuaciones del Perfil (Fluidos Newtonianos)
- **Ecuación Logarítmica:**
  $$u = (1 + 1,326 \sqrt{f}) V - 2,04 \sqrt{f} V \log \left[ \frac{r_0}{r_0 - r} \right]$$
- **Ley de Blasius (Potencia 1/7):**
  $$\frac{u}{u_{max}} = \left( \frac{y}{r_0} \right)^{1/7}$$
  *(donde $y = r_0 - r$)*

---

## 2. Cálculo de Pérdidas: Ecuación de Darcy-Weisbach
Es la ecuación general para determinar la pérdida de carga por fricción ($h_p$) en cualquier régimen de flujo:

$$h_p = f \frac{L}{D} \frac{V^2}{2g}$$

Si se expresa en función del caudal ($Q$):

$$h_p = f \frac{L Q^2}{32 g \pi^2 D^5} = \text{Cte} \cdot \frac{1}{D^5}$$

---

## 3. Factores de Fricción ($f$) para Fluidos Newtonianos
El factor $f$ depende del número de Reynolds ($Re = \frac{\rho V D}{\mu}$) y la rugosidad relativa ($e/D$).

### Ecuaciones por Régimen
- **Régimen Laminar ($Re < 2000$):** $f = \frac{64}{Re}$
- **Régimen Turbulento (Cañería Lisa):**
  - **Blasius:** $f = \frac{0,316}{Re^{0,25}}$ (para $3000 < Re < 10^5$).
  - **Prandtl/Nikuradse:** $\frac{1}{\sqrt{f}} = 2 \log(Re \sqrt{f}) - 0,8$.
- **Régimen Turbulento (Cualquier Cañería):**
  - **Colebrook-White:** $\frac{1}{\sqrt{f}} = -2 \log \left( \frac{e/D}{3,7} + \frac{2,51}{Re \sqrt{f}} \right)$
  - **Haaland (Explícita):** $\frac{1}{\sqrt{f}} = -1,8 \log \left[ \left( \frac{e/D}{3,7} \right)^{1,11} + \frac{6,9}{Re} \right]$

### Diagrama de Moody
Gráfico doble logarítmico que representa estas ecuaciones en cuatro zonas: laminar, crítica (incertidumbre), transición y zona rugosa (donde $f$ solo depende de $e/D$).

---

## 4. Fluidos No Newtonianos
Se utilizan números de Reynolds equivalentes ($Re_{MR}$) y no se emplea el diagrama de Moody estándar.

### Modelos y Reynolds Equivalentes
- **Ley de la Potencia (Pseudoplásticos):**
  $$Re_{PL} = \frac{\rho V^{2-n} D^n}{8^{n-1} m \left( \frac{3n+1}{4n} \right)^n}$$
- **Modelos de Bingham y Herschel–Bulkley:** Utilizan el **Número de Hedstrom** ($He$) y el **Número de Bingham** ($Bi$):
  - $He = \frac{\rho D^2 \tau_0^B}{\mu_B^2}$
  - $Bi = \frac{\tau_0^B D}{\mu_B V}$

### Cálculo de $f$ en Régimen Turbulento
- **Dodge y Metzner:** $\frac{1}{\sqrt{f}} = \frac{4}{n'^{0,75}} \log [Re_{MR} f^{(2-n')/2}] - \frac{0,4}{n'^{1,2}}$
- **Irvine (1988):** $f = \frac{D(n)}{Re_{MR}^{1/(3n+1)}}$

---

## 5. Pérdidas Primarias y Secundarias
- **Pérdidas Primarias:** Debidas a la viscosidad en tramos rectos.
- **Pérdidas Secundarias:** Debidas a accesorios (válvulas, codos) que generan turbulencias locales.
  - **Fórmula:** $h_s = k \frac{V^2}{2g}$
  - **Método de Longitud Equivalente ($L_e$):** Sustituye el accesorio por un tramo de cañería con pérdida idéntica.

---

## 6. Conductos No Circulares
Se utiliza el **Radio Hidráulico** ($R_h$) para adaptar las fórmulas:
- $R_h = \frac{\text{Área}}{\text{Perímetro Mojado}}$
- Para cañerías circulares llenas: $R_h = D/4 \rightarrow D = 4 R_h$.
- En las fórmulas de $Re$ y Darcy, se reemplaza $D$ por el **Diámetro Hidráulico** ($D_h = 4 R_h$).

---

## 7. Métodos de Cálculo de Pérdidas Primarias
Existen tres tipos de problemas según la incógnita ($h_p, Q, \text{ o } D$):

1. **Método Aproximado (Iterativo):** Se supone un valor de $f$, se calcula la incógnita, se verifica el nuevo $Re$ y se ajusta $f$ hasta convergencia.
2. **Método Exacto/Riguroso:** Magnitudes adimensionales independientes de $D$:
   - $N_1 = f \cdot Re^5 = \frac{128}{\pi^3} \frac{h_p}{L} \frac{Q^3 \rho^5}{\mu^5}$
   - $N_2 = \frac{e/D}{Re} = \frac{\pi e \mu}{4 Q \rho}$

---

## 8. Sistemas de Tuberías
- **En Serie:** Caudales iguales ($Q = \text{cte}$) y las pérdidas se suman ($h_t = \sum h_i$).
- **En Paralelo:** Pérdidas iguales en todas las ramas ($h_p = \text{cte}$) y el caudal total es la suma de los parciales.
- **Redes Ramificadas (Hardy Cross):**
  - **Caudal corrector ($\Delta Q$):** $\Delta Q = - \frac{\sum a_i Q_i^2}{2 \sum a_i Q_i}$ (donde $h = a Q^2$).

---

## 9. Envejecimiento y Cavitación
- **Envejecimiento:** $k_{viejo} = k_{nuevo} + \alpha t$.
- **Cavitación:** Ocurre cuando la presión cae por debajo de la tensión de vapor ($P < P_v$). Se previene asegurando que la presión mínima en cualquier punto sea mayor a la de vapor.

# Guía de Estudio: Flujo en Conductos Cerrados

Esta guía de estudio ha sido diseñada para profundizar en los conceptos fundamentales de la mecánica de fluidos aplicados al flujo en cañerías, abarcando desde los perfiles de velocidad hasta el cálculo de pérdidas de carga en fluidos newtonianos y no newtonianos.

---

## Cuestionario de Repaso

**Instrucciones:** Responda a las siguientes preguntas de manera concisa, utilizando entre dos y tres oraciones para cada una.

1. ¿Cómo se desarrolla un flujo turbulento completamente desarrollado al entrar el fluido en una cañería?
2. ¿Qué es la subcapa viscosa y por qué es relevante para la ingeniería?
3. ¿Cuál es la diferencia entre una cañería "hidráulicamente lisa" y una "rugosa"?
4. Describa la utilidad y aplicación general de la ecuación de Darcy-Weisbach.
5. ¿De qué variables depende el factor de fricción ($f$) según el análisis dimensional y experimental?
6. ¿Qué caracteriza a la "zona crítica" en el diagrama de Moody?
7. ¿Cómo varía el cálculo del factor de fricción para fluidos no newtonianos en comparación con los newtonianos?
8. Explique la diferencia entre pérdidas primarias y pérdidas secundarias en un sistema de tuberías.
9. ¿Cómo se adapta el cálculo del número de Reynolds para conductos de sección no circular?
10. ¿Qué es la cavitación y cuáles son sus efectos negativos en las instalaciones?

---

## Clave de Respuestas

1. Al entrar el fluido, se forma una capa límite laminar que crece hasta transformarse en turbulenta y cubrir toda la sección transversal. Este estado de flujo completamente desarrollado se alcanza usualmente en una distancia de unos 50 diámetros en tuberías lisas, o menos si hay rugosidad.
2. Es una capa límite viscosa sumamente delgada cerca de la pared donde la velocidad es cero y los efectos de la viscosidad son muy elevados. Es fundamental para el diseño de operaciones de transferencia de materia y energía debido a que el flujo allí es aproximadamente laminar.
3. Una cañería es hidráulicamente lisa si sus imperfecciones o rugosidades quedan totalmente dentro del espesor de la subcapa viscosa ($e < \delta_l$). Se considera rugosa cuando las imperfecciones sobrepasan la subcapa viscosa y la capa de transición combinadas ($e > \delta_l$).
4. Es una ecuación general utilizada para calcular las pérdidas de carga ($h_p$) tanto en régimen laminar como turbulento. Se aplica a fluidos newtonianos y no newtonianos, relacionando el factor de fricción, la longitud, el diámetro y el cuadrado de la velocidad.
5. El factor de fricción es una propiedad del sistema que depende del número de Reynolds (velocidad, viscosidad, densidad y diámetro) y de la rugosidad relativa de la cañería ($e/D$). En regímenes completamente turbulentos, puede llegar a depender exclusivamente de la rugosidad relativa.
6. La zona crítica se sitúa entre un número de Reynolds de 2000 y 4000. En este rango existe una gran incertidumbre en las curvas del factor de fricción, por lo que no se aconseja diseñar instalaciones que operen en estas condiciones.
7. Para fluidos no newtonianos no se utiliza el diagrama de Moody; en su lugar, se definen números de Reynolds equivalentes (como el de Reynolds generalizado o de Bingham). El factor de fricción se determina mediante ecuaciones específicas según el modelo del fluido (ley de potencia, Bingham, etc.).
8. Las pérdidas primarias son aquellas causadas por la viscosidad del fluido a lo largo de los tramos rectos de cañería. Las pérdidas secundarias se producen en los accesorios (válvulas, codos, filtros) debido a turbulencias localizadas y desprendimientos de la capa límite.
9. Se utiliza el concepto de radio hidráulico ($R_h$), que es el cociente entre el área transversal del fluido y el perímetro mojado. Para los cálculos de Reynolds y Darcy-Weisbach, el diámetro se reemplaza por el diámetro hidráulico ($D_h$), definido como cuatro veces el radio hidráulico.
10. Se produce cuando la presión del líquido cae por debajo de su tensión de vapor, formando burbujas que implotan al alcanzar zonas de mayor presión. Sus efectos incluyen la disminución del rendimiento, daños físicos en los conductos, ruidos y vibraciones.

---

## Temas para Ensayo

**Instrucciones:** Desarrolle una respuesta extensa y argumentativa para las siguientes propuestas.

* **Evolución del perfil de velocidades:** Analice cómo se transforma el perfil de velocidades desde la entrada de la cañería hasta el régimen turbulento desarrollado, detallando la influencia del número de Reynolds y la rugosidad de la pared.
* **Análisis comparativo de métodos de cálculo:** Compare el "método aproximado" y el "método exacto" para la resolución de problemas de pérdida de carga, discutiendo las ventajas de utilizar software matemático frente al uso manual del diagrama de Moody.
* **Complejidad en fluidos no newtonianos:** Discuta las dificultades adicionales que presenta el flujo turbulento en fluidos viscoplásticos y pseudoplásticos, y evalúe la validez de aplicar criterios de rugosidad de fluidos newtonianos en estos casos.
* **Sistemas de tuberías y leyes de distribución:** Explique los principios hidráulicos (equivalentes a las leyes de Kirchhoff) que rigen el flujo en tuberías en serie, paralelo y ramificadas, haciendo especial énfasis en el método de Hardy Cross.
* **Impacto del envejecimiento en infraestructuras:** Evalúe cómo el proceso de corrosión e incrustación altera la rugosidad absoluta con el tiempo y las implicancias que esto tiene en la potencia requerida de las bombas a largo plazo.

---

## Glosario de Términos Clave

| Término | Definición |
| :--- | :--- |
| **Cavitación** | Fenómeno de formación e implosión de burbujas de vapor cuando la presión del fluido desciende por debajo de su presión de vapor. |
| **Diagrama de Moody** | Gráfico doble logarítmico que permite obtener el factor de fricción ($f$) en función del número de Reynolds y la rugosidad relativa. |
| **Diámetro Hidráulico** | Magnitud utilizada para conductos no circulares, calculada como $D_h = 4 \cdot R_h$. |
| **Ecuación de Darcy-Weisbach** |
