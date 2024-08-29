[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=hpantoja22/PropagacionErrores)
# Estimación del error en la deflexión de un mástil de bote de vela

Dr. Hermes Pantoja Carhuavilca

# Enunciado

La deflexión $y$ de la punta de un mástil en un bote de vela está dada  por la siguiente fórmula:



 $\displaystyle y=\frac{FL^4 }{8EI}\,\,$  
 
![barco](https://github.com/user-attachments/assets/917c413a-9c1c-433e-a29f-cc721ea8e5c7)
  
donde: 


 $F$ es una carga lateral uniforme (N/m), 


 $L$ es la altura del mástil (m),


 $E$ es el módulo de elasticidad (N/m²),


 $I$ es el momento de inercia (m⁴).


Se proporcionan los siguientes valores junto con sus respectivos errores:

 $$ \tilde{F} =750\,\textrm{N/m},~~\Delta \tilde{F} =30\,\textrm{N/m} $$ 

 $$ \tilde{L} =9\,\textrm{m},~~\Delta \tilde{L} =0.03\,\textrm{m} $$ 

 $$ \tilde{E} =7.5\times 10^9 \,{\textrm{N/m}}^2 ,~~\Delta \tilde{E} =5\times 10^7 \,{\textrm{N/m}}^2 $$ 

 $$ \tilde{I} =0.0005\,{\textrm{m}}^4 ,~~\Delta \tilde{I} =0.000005\,{\textrm{m}}^4 $$ 

Se pide: Estimar el error en la deflexión $y$ utilizando la propagación de errores.

# Objetivo

El objetivo de esta actividad es calcular la deflexión de la punta de un  mástil en un bote de vela utilizando la fórmula dada y estimar el error  asociado en la deflexión utilizando la propagación de errores.

# Conceptos Teóricos

La propagación de errores se puede generalizar a funciones que sean  dependientes de más de una variable independiente. Sea una función  $q=f(x_1 ,x_2 )$  donde las medidas ${\tilde{x} }_1$ y ${\tilde{x} }_2$ tienen  errores $\Delta {\tilde{x} }_1$ y $\Delta {\tilde{x} }_2$ .

Si las incertidumbres en $x_1$ y $x_2$ son independientes y aleatorias, entonces la incertidumbre en $q$ es

$$\epsilon_q=\sqrt{\left(\frac{\partial q}{\partial x_1} \Delta \tilde{x}_1\right)^2+\cdots+\left(\frac{\partial q}{\partial x_2} \Delta \tilde{x}_2\right)^2}$$

Llamada error \textbf{Error Cuadrático}.

En otro caso, nunca es mayor que la suma ordinaria
$$\epsilon_q=\sqrt{\left(\frac{\partial q}{\partial x_1} \Delta \tilde{x}_1\right)^2+\cdots+\left(\frac{\partial q}{\partial x_2} \Delta \tilde{x}_2\right)^2}$$

Mediante una versión de la serie de Taylor para el caso de varias variables,  podemos aproximar la función como: 

 $$ f(x_1 ,x_2 )\approx f({\tilde{x} }_1 ,{\tilde{x} }_2 )+\frac{\partial f}{\partial x_1 }\cdot (x_1 -{\tilde{x} }_1 )+\frac{\partial f}{\partial x_2 }\cdot (x_2 -{\tilde{x} }_2 ) $$ 

Con lo que el error en $q$ se puede aproximar como: 

 $$ \xi_q =\Delta f({\tilde{x} }_1 ,{\tilde{x} }_2 )\approx \left|\frac{\partial f}{\partial x_1 }\right|\cdot \Delta {\tilde{x} }_1 +\left|\frac{\partial f}{\partial x_2 }\right|\cdot \Delta {\tilde{x} }_2 $$ 

En nuestro caso, $y=\frac{FL^4 }{8EI}$ , donde las variables $F$ , $L$ , $E$ , e $I$ son independientes, y podemos calcular el error en la deflexión $y$ utilizando esta aproximación. 

# Preguntas 

1.   **Calcular la deflexión:** Implementa una función en Matlab que reciba los valores de $F$ , $L$ , $E$ , e $I$ y calcule la deflexión $y$ usando la fórmula dada.
2. **Propagación del error:** Deriva la expresión para la propagación del error en la deflexión $y$ . Implementa una función en Matlab que calcule el error en $y$ utilizando  la fórmula de propagación de errores.
3. **Ejecutar los cálculos:** Utiliza las funciones desarrolladas para calcular la deflexión y el error  asociado usando los valores proporcionados.
4. **Investigación adicional:**  ¿Cómo afecta el aumento de cada uno de los parámetros $F$ , $L$ , $E$ , o $I$  la deflexión y su error?. Realiza simulaciones variando cada parámetro  individualmente mientras mantienes los otros constantes. Grafique la relación entre $y$ y una de las variables ( $F$ , $L$ , $E$ ó $I$ ),  manteniendo los otros parámetros constantes.
