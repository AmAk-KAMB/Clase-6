# SISTEMAS HIDRAULICOS 

Los sistemas hidráulicos se refieren a aquellos que involucran el flujo de líquidos (generalmente agua o aceite) a través de conductos o dispositivos, utilizando principios como la presión y el caudal. 
Estos sistemas se modelan mediante ecuaciones que relacionan las variables como presión, caudal, volumen y resistencia hidráulica.

## Definición: 
Un sistema hidráulico es un conjunto de componentes interconectados (bombas, válvulas, conductos, etc.) que controlan el movimiento y la presión de un fluido, usando las leyes de la mecánica de fluidos. 
Se utilizan frecuentemente en maquinaria industrial, frenos y sistemas de potencia.
## Ejemplo: 
Un sistema de frenos hidráulico en un automóvil, donde el líquido de frenos se presiona para accionar las pinzas de freno.

## MODELO MOTO DC 
El modelo de un motor de corriente continua (DC) basado en la corriente de campo se refiere al análisis y representación matemática del motor, considerando el comportamiento de la corriente que fluye a 
través de los devanados de campo, que genera el campo magnético necesario para el funcionamiento del motor. A continuación se describe cómo se modela este tipo de motor.
![download](https://github.com/user-attachments/assets/044f1086-566b-4cd1-9a16-eb99f5f61b0c)

# MOTOR DC POR CORRIENTE DE CAMPO 
En los motores de corriente continua con excitación separada o serie, el campo magnético se genera mediante una corriente de campo que circula por los devanados del estator, mientras que la armadura (rotor) 
es la parte giratoria. La velocidad y el par motor dependen tanto de la corriente de la armadura como de la corriente de campo.
![images](https://github.com/user-attachments/assets/fbc94591-14a3-46ce-8dde-e14d25b28f0a)

## Ecuaciones fundamentales:

Vf=Rf⋅If+LfdI/dtf
​
 
 
## Donde:

**𝑉𝑓:** es el voltaje aplicado al circuito de campo.

**𝐼𝑓:** es la corriente de campo.

**𝑅𝑓:** es la resistencia del devanado de campo.

**𝐿𝑓:** es la inductancia del devanado de campo.
##
## Ecuación de la corriente de armadura:
##
$$V_a = R_a \cdot I_a + L_a \frac{dI_a}{dt} + E_b$$
##
# Donde:

**$$𝑉_𝑎$$:**   es el voltaje aplicado a la armadura.

**$$𝐼_𝑎$$:**   es la corriente de armadura.

**$$𝑅_𝑎$$:** es la resistencia de la armadura.

**$$𝐿_𝑎$$:**  es la inductancia de la armadura.

**$$𝐸_𝑏$$:** es la fuerza contraelectromotriz (back-EMF), que es proporcional a la velocidad angular 
𝜔.
##
## PAR MOTOR (TORQUE):
$$T=K_t⋅ϕ⋅I_a$$
​
## Donde:

**$$𝐾_𝑡$$:** es la constante de torque del motor.

**𝜙:** es el flujo magnético generado por la corriente de campo.

**$$𝐼_𝑎$$:** es la corriente de armadura.

## COMPORTAMIENTO DINAMICO DEL SISTEMA:
El comportamiento dinámico de un motor DC con control por corriente de campo se puede describir mediante un sistema de ecuaciones diferenciales que relacionan el flujo magnético 
𝜙, la corriente de armadura $$𝐼_𝑎$$, la corriente de campo $$𝐼_𝑓$$, y la velocidad 𝜔. El control de la corriente de campo permite modificar el flujo magnético 
𝜙, lo cual afecta tanto la velocidad como el par motor.
##

## Modelado en Dinámica de Sistemas:
En términos de dinámica de sistemas, el modelo por corriente de campo incluye la dinámica del devanado de campo (que determina cómo cambia el flujo magnético en función de la corriente de campo) 
y la interacción con la armadura (que determina el torque y la velocidad).

## Entrada: 
Voltaje aplicado al campo $$𝑉_𝑓$$, voltaje aplicado a la armadura $$𝑉_𝑎$$.
##
## Salida: 
Velocidad 𝜔 y torque 𝑇.

# Modelo por Corriente de Campo

El modelo por corriente de campo de un motor de corriente continua (DC) describe la relación entre las partes eléctricas, magnéticas y mecánicas del motor en función de la corriente que circula 
por el circuito de campo. Este tipo de modelado se utiliza principalmente para entender cómo la corriente de campo influye en el par y la velocidad del motor, controlando indirectamente el 
rendimiento del mismo.
![download](https://github.com/user-attachments/assets/28ecbd84-cd31-4dda-b082-d96ebe2817ff)

## Definición:

El modelo está compuesto por las siguientes partes:

### Parte Eléctrica
Describe cómo la corriente de campo $$i_c$$(t) cambia en respuesta al voltaje aplicado $$v_c$$(t) , las resistencias y las inductancias en el circuito de campo. La ecuación correspondiente es:

$$L_c \frac{di_c(t)}{dt} + R_c i_c(t) = v_c(t)$$

Donde:
- **$$L_c$$:** es la inductancia del devanado de campo.
- **$$R_c$$:** es la resistencia del devanado de campo.
- **$$v_c(t)$$:** es el voltaje aplicado al circuito de campo.

### Parte Magnética
Relaciona el flujo magnético Φ con la corriente de campo $$i_c$$(t) . El flujo magnético es proporcional a la corriente de campo a través de la constante  $$K_c$$, de manera que:


$$Φ = K_c i_c$$(t)


### Parte Mecánica
Describe la dinámica del par motor $$T_m$ y la velocidad angular w(t). El par motor es proporcional al flujo magnético Φ y a la corriente de armadura $$i_a$$(t):


$$T_m = K_a ⋅ K_c ⋅ i_a(t) ⋅ i_c(t)$$

La ecuación de movimiento para el sistema mecánico es:

$$J \frac{d^2\theta}{dt^2} + b \frac{d\theta}{dt} + k\theta = \tau(t)$$

Donde:
- **J**  es el momento de inercia.
- **b**  es el coeficiente de fricción.
- **k**  es la constante de rigidez (en caso de presencia de elementos elásticos).
- **T(t)** es el torque resultante.

## Ejemplo

Un ejemplo práctico del modelo por corriente de campo se encuentra en el control de velocidad de un motor de corriente continua. 
Variando la corriente de campo mediante el voltaje $$v_c$$(t), se puede controlar el flujo magnético  Φ y por lo tanto, ajustar el par motor $$T_m $$, lo que afectará la velocidad 
del motor.

# Metodo de energia para obtener las ecuaciones de movimiento

El método de energía es una técnica en dinámica que se usa para derivar las ecuaciones de movimiento de un sistema mediante principios de energía, como la energía cinética, la energía potencial y el trabajo realizado. Este enfoque puede ser particularmente útil en sistemas complejos o con múltiples grados de libertad.

## Sistema conservativo

Toda la energia cinetica y potencial sale de sistema en forma de trabajo mecanico.

$$ Δ(T + U) = ΔW $$

si no entra energia externa entonces la ecuacion queda de la siguiente manera:

$$ Δ(T + U) = 0 $$
$$ T + U = Constante $$

## Ejemplo
![image](https://github.com/user-attachments/assets/37b44332-acc2-46e2-9b26-1f663412b37b)

$$ T + U = \frac{1}{2} mẋ^{2} + \frac{1}{2} kx^{2} = Constante $$
$$ \frac{d}{dt} (T + U) = mẋẍ + kxẋ = (mẍ + kx)ẋ = 0 $$
$$ mẍ + kx = 0 $$

## Recomendaciones

- Se recomienda su uso en sistemas simples, ya que entre mas interacción de elementos mas difícil es establecer las energías que intervienen
- Para sistemas muy complejos es mejor usar leyes de Newton
- Para usar el enfoque de energía existe un método más completo basado en las ideas de lenguaje


# Conversión movimiento Translacional - Rotacional

La conversión de movimiento translacional a rotacional es un proceso mediante el cual un desplazamiento lineal o rectilíneo (translacional) se convierte en un movimiento giratorio (rotacional). Este principio se utiliza en muchos mecanismos y máquinas. 

## Ejemplo

un ejemplo común es el sistema de un pistón en un motor de combustión interna, donde el movimiento lineal del pistón se transforma en el giro del cigüeñal. La conversión puede lograrse mediante diversos mecanismos, como engranajes, ruedas y ejes o sistemas de biela-manivela.

## Aplicaciones

### 1. Tornillo sinfin
![image](https://github.com/user-attachments/assets/fe006d09-fd3e-4b47-be59-92bd7f0ff6fd)

Su formula es: $$J\frac{W}{8}(\frac{L}{2π})^{2}$$

### 2. Piñon cremallera 
![image](https://github.com/user-attachments/assets/937bdd29-e85e-4f13-ac29-eec201ec86ca)

Su formula es: $$J = Mr^{2} = \frac{W}{8}r^{2}$$

### Trenes de Engranajes, Palancas y Bandas
![image](https://github.com/user-attachments/assets/cf4a074e-2b53-42ca-831a-be25cc80c1cf)

$$ r_{1}N_{2} = r_{2}N_{1} $$
$$ θ_{1}r_{1} = θ_{2}r_{2} $$
$$ T_{1}θ_{1} = T_{2}θ_{2} $$

Por lo tanto : 

$$ \frac{T_{1}}{T_{2}} = \frac{N_{1}}{N_{2}} = \frac{θ_{2}}{θ_{1}} $$

## conclusiones
- El modelamiento de los sistemas mecánicos requiere la aplicación de modelo del fenómeno fisico
- El modelo de ecuaciones diferenciales permitirá describir el movimiento en el dominio del tiempo para cualquier instante de tiempo
- El movimiento lineal y el movimiento rotacional son comparables y los fenomenos fisicos que se presentan son similares
- Un modelo de movimiento rotacional y lineal pueden ser iguales sin embargo describen dos tipos de fenómenos totalmente diferentes.
#
#
# Análisis del Sistema de Masa y Polea

## Paso 1: Definir las variables y parámetros
>**m** = 5 kg (masa suspendida)
>**r** = 0.1 m (radio de la polea)
>**g** = $$9.81 m/s²$$ (aceleración gravitacional)
>**k** = $$100 N/m$$ (constante de elasticidad del cable)
>**b** = $$2 N·s/m$$ (coeficiente de fricción viscosa)
>**k_e** = $$0.5 N·m/A$$ (constante de torque del motor)
>**T**: torque del motor (N·m)
>**θ**: ángulo de rotación de la polea (rad)
>**y**: posición vertical de la masa (m)
>**i**: corriente del motor (A)
>**s**: variable compleja de Laplace

## Paso 2: Analizar el movimiento de la polea

La rotación de la polea está relacionada con la posición vertical de la masa:

$$θ = \frac{y}{r}$$

La velocidad angular de la polea es:

$$ω = \frac{\frac{dy}{dt}}{r}$$

## Paso 3: Aplicar la ley de Newton a la masa

La fuerza en el cable es:

$$F = m \cdot g + b \cdot \frac{dy}{dt} + k \cdot y$$


La aceleración de la masa es:

$$a = \frac{F}{m} = g + \frac{b}{m} \cdot \frac{dy}{dt} + \frac{k}{m} \cdot y$$

Sustituyendo los valores:

$$a = 9.81 + \frac{2}{5} \cdot \frac{dy}{dt} + \frac{100}{5} \cdot y$$

## Paso 4: Relacionar el torque del motor con la fuerza en el cable

El torque del motor es:


$$T = r \cdot F$$

Sustituyendo la expresión de $$( F \)$$:

$$T = r \cdot (m \cdot g + b \cdot \frac{dy}{dt} + k \cdot y)$$

Sustituyendo los valores:


$$T = 0.1 \cdot (5 \cdot 9.81 + 2 \cdot \frac{dy}{dt} + 100 \cdot y)$$

## Paso 5: Aplicar la transformada de Laplace

Transformar la ecuación del torque:


$$T(s) = 0.1 \cdot \left(\frac{5 \cdot 9.81}{s} + 2 \cdot s \cdot Y(s) + 100 \cdot Y(s) \right)$$

Simplificar:

$$T(s) = 0.1 \cdot \left(\frac{49.05}{s} + 2 \cdot s \cdot Y(s) + 100 \cdot Y(s) \right)$$

## Paso 6: Obtener la función de transferencia

Dividir ambos lados por $$( Y(s) \)$$:

$$G(s) = \frac{Y(s)}{T(s)} = \frac{1}{0.1 \cdot (2 \cdot s + 100)}$$

Multiplicar por el factor de conversión del motor:

$$G(s) = \frac{1}{5 \cdot s^2 + 2 \cdot s + 100} \cdot \frac{0.1}{0.01 \cdot s^2 + 0.5}$$

### Función de transferencia final

$$G(s) = \frac{0.02}{(5s^2 + 2s + 100)(0.01s^2 + 0.5)}$$


##Conclusiones

El modelado de sistemas hidráulicos y motores DC permite analizar y optimizar el rendimiento en aplicaciones industriales. La mecánica de fluidos y el control por corriente de campo son esenciales para sistemas de potencia y frenado, y los modelos de ecuaciones diferenciales proporcionan una base para el análisis dinámico y el diseño eficiente de estos sistemas.

## Referencias

>Halliday, D., & Resnick, R. (2018). Fundamentos de Física (10.ª ed.). Wiley.
>
>Cengel, Y., & Cimbala, J. (2020). Mecánica de Fluidos: Fundamentos y Aplicaciones. McGraw-Hill.
>
>Merritt, H. E. (1967). Hydraulic Control Systems. John Wiley & Sons.
>
>Ogata, K. (2010). Ingeniería de Control Moderna (5.ª ed.). Pearson Educación.
