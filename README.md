<div>
<h2> 📘 Unidad 2: Graficación 2D🖥️ </h2>
</div>
<div>
<h2> 📈📉 Graficación | SCC-1010 | Ingeniería en Sistemas</h2>
</div>

### 🛠️ Tecnologías y Entorno
![Git Bash](https://img.shields.io/badge/Git%20Bash-F05032?style=for-the-badge&logo=git&logoColor=white) 
![Blender](https://img.shields.io/badge/Blender-%23F5792A.svg?style=for-the-badge&logo=blender&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) 

Lenguaje: Python 👩‍💻🐍                     
Software Core: Blender 5.0 (Motor de renderizado y modelado procedural)               
Sistema Operativo: Windows 11 🪟                  
Control de Versiones: Git & GitHub 

---

> [!IMPORTANT]
> **DINÁMICA ESPACIAL:** En esta unidad, dejamos de crear objetos estáticos para darles vida a través de transformaciones matemáticas. Aprenderemos cómo el software calcula cada movimiento mediante matrices para lograr fluidez y precisión.

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
<div align="center">
<h3>
〰️〰️〰️〰️〰️〰️〰️ 2.1 Transformación Bidimensional 〰️〰️〰️〰️〰️〰️〰️〰️
</h3>
</div>

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<div><h3> 2.1 Conceptos Base </h3> </div>
Las transformaciones bidimensionales son los procedimientos para alterar la ubicación, tamaño y orientación de objetos en un plano XY. Estas operaciones son esenciales para la animación y la interactividad.

Recomendación: Una infografía que muestre las 4 transformaciones básicas (Traslación, Escala, Rotación y Sesgado) aplicadas a un mismo objeto.

🔴 2.1.1 TraslaciónEs el desplazamiento de un objeto a una nueva posición. Se logra sumando valores de desplazamiento (tx, ty) a las coordenadas originales (x, y).
 
🔴 2.1.2 EscalamientoCambia el tamaño de un objeto. Un factor mayor a 1 aumenta el tamaño, mientras que uno menor a 1 lo reduce. Puede ser uniforme o no uniforme.
 
🔴2.1.3 RotaciónGira un objeto alrededor de un punto pivote (usualmente el origen o el centro del objeto) siguiendo un ángulo 0
 
🔴2.1.4 Sesgado (Shear)Produce una distorsión en la forma del objeto, como si se inclinara lateralmente, desplazando los puntos en proporción a su distancia desde un eje.

<div align="center">
<h3>
    
![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)
〰️〰️〰️〰️〰️ 2.2 Representación Matricial de Transformaciones 〰️〰️〰️〰️〰️
</h3>
</div>

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div><h3> El Poder de las Matrices </h3></div>
Para optimizar el rendimiento, los motores de graficación como Blender no calculan cada transformación por separado, sino que utilizan Coordenadas Homogéneas. Esto permite expresar cualquier transformación como una multiplicación de matrices de   3 X 3. 

Recomendación: Una imagen que muestre la matriz genérica de transformación y cómo se multiplican los puntos.

🎮 Ejercicio de Control: Movimiento por Teclado
Implementamos un sistema de control reactivo donde las teclas de dirección ejecutan una traslación en tiempo real sobre el objeto activo.

```Python
def mover_objeto(eje, valor):
    obj = bpy.context.active_object
    if eje == 'X':
        obj.location.x += valor
    elif eje == 'Y':
        obj.location.y += valor

# Este concepto es la base de la interactividad en videojuegos
```

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div align="center">
<h3>
〰️〰️〰️〰️〰️〰️〰️ 2.3 Trazo de Líneas Curvas 〰️〰️〰️〰️〰️〰️〰️〰️
</h3>
</div>

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div> <h3> Definición Matemática </h3> </div>
A diferencia de un mapa de bits, las curvas en graficación vectorial se definen mediante ecuaciones. Las más utilizadas en el software de diseño y 3D son las curvas paramétricas que permiten un control total sobre la curvatura.

🔴2.3.1 Bézier
Las curvas de Bézier se basan en puntos de control. Un segmento de Bézier tiene puntos finales (anclajes) y puntos de control que "atraen" la curva hacia ellos, definiendo su forma sin ser parte de la línea.

Uso: Logotipos, tipografías y trazado de caminos en Blender.
🔴2.3.2 B-spline
Las B-splines (Basis Splines) ofrecen una mayor flexibilidad. A diferencia de las Bézier, mover un punto de control en una B-spline solo afecta a una sección local de la curva, lo que facilita el modelado de superficies muy complejas.




<table>
  <tr>
    <td><img width="473" height="565" alt="image" src="https://github.com/user-attachments/assets/9d42e4c8-ed6d-4e34-b795-27b85c2bcac9" /></td>
    <td><img width="426" height="586" alt="image" src="https://github.com/user-attachments/assets/0cb5c32b-fef3-4300-af06-12b67fab5a06" />
</td>
  </tr>
</table>

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div align="center">
<h1> ❄️ 2.4 Fractales ❄️ </h1>
<p><i>La geometría de la autosimilitud: El orden dentro del caos</i></p>
</div>

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div> <h3> ¿Qué es un Fractal? </h3> </div>
Un fractal es un objeto geométrico cuya estructura básica, fragmentada o aparentemente irregular, se repite a diferentes escalas. El término fue propuesto por Benoît Mandelbrot en 1975.

En la graficación por computadora, los fractales son esenciales porque permiten generar escenarios complejos (montañas, nubes, costas) con muy poco código, utilizando la recursividad.

🔴 Características Principales
Autosimilitud: Si observas una parte pequeña del fractal, se ve exactamente igual (o muy parecida) al objeto completo.

Dimensión no entera: A diferencia de una línea (dimensión 1) o un plano (dimensión 2), los fractales tienen dimensiones fraccionarias.

Algoritmo Recursivo: Se crean repitiendo un proceso matemático infinitamente.

---

🌲 Aplicaciones en el Mundo Real
Los fractales no son solo teoría; sin ellos, los gráficos de los videojuegos modernos serían planos y aburridos:

Paisajes Procedimentales: Creación de terrenos, cordilleras y valles.

Sistemas L (L-Systems): Algoritmos fractales específicos para simular el crecimiento de plantas, árboles y estructuras biológicas.

<img width="250" height="183" alt="image" src="https://github.com/user-attachments/assets/9f16005a-4588-444f-86d2-d93cfcd43dbb" />

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div align="center">
<h1> 🔠 2.5 Uso y Creación de Fuentes de Texto </h1>
<p><i>Tipografía tridimensional: Cuando las palabras se convierten en mallas</i></p>
</div>

![](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<div> <h3> El Texto como Geometría </h3> </div>
En la graficación por computadora, el texto puede representarse de dos formas: Mapas de bits (fuentes rasterizadas para interfaces sencillas) y Fuentes Vectoriales (basadas en curvas de Bézier). En Blender, trabajamos con estas últimas para permitir transformaciones 3D.

🔴 2.5.1 Tipos de Fuentes
TTF (TrueType Fonts): Creadas por Apple y Microsoft, utilizan curvas de Bézier cuadráticas. Son las más comunes.

OTF (OpenType Fonts): Evolución de las TTF, permiten un mayor soporte de caracteres y utilizan curvas de Bézier cúbicas, lo que ofrece un trazado más preciso.

🔴 2.5.2 Transformación de Texto en Blender
Al añadir un objeto de texto en Blender, este hereda propiedades de curva que nos permiten:

Extrusión: Dar grosor a las letras para que dejen de ser planas.

Bevel (Biselado): Redondear los bordes para que capturen mejor los reflejos de luz.

Conversión a Malla: Transformar el texto en vértices y caras para poder editar letra por letra.

🎨 Ejercicio de Diseño: Fuentes y Materiales
En este ejercicio práctico, aprendemos a manipular el texto mediante código para generar títulos dinámicos en un escenario.

```Python
import bpy

# Añadir texto al escenario
bpy.ops.object.text_add(location=(0, 0, 0))
text_obj = bpy.context.object
text_obj.data.body = "GRAFICACIÓN 2024"

# Aplicar transformaciones geométricas
text_obj.data.extrude = 0.1  # Grosor
text_obj.data.bevel_depth = 0.02  # Biselado

```



<div align="center">
<h1> 📚 Bibliografía y Referencias - Unidad 2 </h1>
</div>

📘 Foley, J. D. (1996). Computer Graphics: Principles and Practice. Addison-Wesley.

📗 Rogers, D. F. (1997). Mathematical Elements for Computer Graphics. McGraw-Hill.

📒 Blender API Documentation. Text Curve Data Objects. Recuperado de docs.blender.org
