# Análisis Técnico: Flujo en Conductos Cerrados y Cálculo de Pérdidas de Carga

Este documento sintetiza los principios fundamentales, ecuaciones y metodologías para el análisis del flujo de fluidos incompresibles en cañerías, abarcando regímenes laminar y turbulento para fluidos newtonianos y no newtonianos.

---

## Resumen Ejecutivo

El estudio del flujo en conductos cerrados es crítico para determinar las pérdidas de energía que ocurren por efectos viscosos y geométricos.

* **Pérdidas de Carga:** Se calculan universalmente mediante la **ecuación de Darcy-Weisbach**.
* **Regímenes de Flujo:** Distinción entre laminar ($Re < 2000$), transición y turbulento ($Re > 4000$).
* **Perfil de Velocidades:** Presencia de una subcapa viscosa delgada cerca de las paredes.
* **Sistemas Complejos:** Métodos para tuberías en serie, paralelo y redes (Hardy Cross).

---

## 1. Perfil de Velocidades en Régimen Turbulento

Cuando un fluido ingresa a una cañería, la viscosidad genera una capa límite que crece hasta cubrir toda la sección transversal (**flujo completamente desarrollado**).

### Estructura del Flujo Turbulento
1.  **Subcapa Viscosa ($\delta_l$):** Efectos viscosos elevados, flujo aproximadamente laminar.
2.  **Capa de Transición:** Coexistencia de efectos viscosos y remolinos (hasta $14 \delta_l$).
3.  **Núcleo Turbulento:** Perfil de velocidad aproximadamente plano.

### Ecuaciones de Perfil
* **Espesor de la subcapa viscosa:** $$\delta_l = 14,14 \cdot \frac{D}{Re \cdot \sqrt{f}}$$
* **Ecuación de Blasius (aproximada):** $$\frac{u}{u_{max}} = \left( \frac{y}{r_0} \right)^{1/7}$$
* **Ecuación de precisión (Newtonianos):** $$u = (1 + 1,326 \sqrt{f}) V - 2,04 \sqrt{f} V \log\left[ \frac{r_0}{r_0 - r} \right]$$

---

## 2. Cálculo de Pérdidas: Ecuación de Darcy-Weisbach

La pérdida de carga primaria ($h_p$) se expresa mediante la ecuación general:

$$h_p = f \cdot \frac{L}{D} \cdot \frac{V^2}{2g}$$

Donde $f$ es el **factor de fricción**, $L$ y $D$ la geometría del conducto, y $V$ la velocidad media. Las pérdidas son inversamente proporcionales a $D^5$.

---

## 3. Factores de Fricción para Fluidos Newtonianos

El cálculo de $f$ depende del régimen y la rugosidad relativa ($e/D$).

| Autor | Aplicación | Condición / Rango |
| :--- | :--- | :--- |
| **Blasius** | Cañería lisa | $3000 < Re < 10^5$ |
| **Nikuradse** | Cañería lisa | $Re > 4000$ |
| **Colebrook-White** | Lisa y rugosa | Estándar industrial (implícita) |
| **Haaland** | Lisa y rugosa | Explícita (error mínimo) |
| **Von Kármán** | Cañería rugosa | Independiente de $Re$ |

---

## 4. Fluidos No Newtonianos

Se adaptan los modelos mediante números de Reynolds equivalentes ($Re_{MR}$ o $Re_{PL}$).

* **Ley de la Potencia:** Se utilizan las ecuaciones de Dodge y Metzner.
* **Modelo de Irvine (1988):** Para fluidos de la ley de potencia.
* **Fluidos Viscoplásticos (Bingham):** Se emplean el número de Bingham ($Bi$) y el número de Hedstrom ($He$).

---

## 5. Clasificación de Pérdidas y Geometrías Especiales

* **Pérdidas Primarias:** Por viscosidad en tramos rectos.
* **Pérdidas Secundarias:** En accesorios (válvulas, codos) calculadas como $h_s = k \cdot \frac{V^2}{2g}$.
* **Conductos No Circulares:** Se utiliza el **Diámetro Hidráulico** ($D_h$):
    $$D_h = 4 \cdot R_h = 4 \cdot \frac{\text{Área}}{\text{Perímetro mojado}}$$

---

## 6. Metodologías de Resolución

1.  **Tipo 1 (Pérdida de carga):** Hallar $h_p$ conocidos $D$ y $Q$.
2.  **Tipo 2 (Descarga):** Hallar $Q$ conocidos $D$ y $h_p$ (requiere iteración).
3.  **Tipo 3 (Tamaño):** Hallar $D$ conocidos $Q$ y $h_p$ (el más complejo).

---

## 7. Sistemas de Tuberías y Factores Operativos

### Configuraciones de Red
* **Serie:** Caudal constante, pérdidas sumatorias ($\sum h_{p_i}$).
* **Paralelo:** Pérdida constante, caudales sumatorios ($\sum Q_i$).
* **Ramificadas:** Método de **Hardy Cross** (Ley de Nodos y Mallas).

### Envejecimiento y Cavitación
* **Envejecimiento:** Aumento de rugosidad con el tiempo ($k_{viejo} = k_{nuevo} + \alpha t$).
* **Cavitación:** Ocurre cuando $P < P_{vapor}$. Produce daños estructurales y vibraciones.
