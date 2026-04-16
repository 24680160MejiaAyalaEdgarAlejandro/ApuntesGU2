<div align="center">
<h1> 📐 Unidad 2: Transformaciones y Geometría Compleja </h1>
<h2> 📈📉 Graficación | SCC-1010 | Ingeniería en Sistemas</h2>
</div>

🛠️ Tecnologías y Entorno
Lenguaje: Python 👩‍💻🐍

Software Core: Blender 5.0 (Motor de renderizado y modelado procedural)

Enfoque: Álgebra lineal aplicada al movimiento bidimensional.
[!IMPORTANT]
DINÁMICA ESPACIAL: En esta unidad, dejamos de crear objetos estáticos para darles vida a través de transformaciones matemáticas. Aprenderemos cómo el software calcula cada movimiento mediante matrices para lograr fluidez y precisión.
<div align="center">
<h3>
〰️〰️〰️〰️〰️〰️〰️ 2.1 Transformación Bidimensional 〰️〰️〰️〰️〰️〰️〰️〰️
</h3>
</div>
<div><h3> 2.1 Conceptos Base </h3></div>Las transformaciones bidimensionales son los procedimientos para alterar la ubicación, tamaño y orientación de objetos en un plano $XY$. Se basan en fórmulas matemáticas aplicadas a cada vértice del objeto.[ESPACIO PARA IMAGEN 1: COMPARATIVA DE TRANSFORMACIONES]Recomendación: Una imagen que muestre un cuadrado original y sus cuatro variantes (trasladado, escalado, rotado y sesgado).

◾ 2.1.1 TraslaciónConsiste en mover un objeto a una nueva posición sumando valores de desplazamiento $(tx, ty)$ a sus coordenadas originales.Lógica: $x' = x + tx$ | $y' = y + ty$.

◾ 2.1.2 EscalamientoAltera el tamaño del objeto multiplicando sus coordenadas por factores de escala $(sx, sy)$.Lógica: $x' = x \cdot sx$ | $y' = y \cdot sy$.

◾ 2.1.3 RotaciónGira el objeto alrededor del origen basándose en un ángulo $\theta$. Requiere el uso de funciones trigonométricas.Fórmula: $x' = x \cos \theta - y \sin \theta$ | $y' = x \sin \theta + y \cos \theta$.

◾ 2.1.4 Sesgado (Shear)
Deforma el objeto inclinándolo en uno de los ejes, alterando su forma pero manteniendo su área.

<div align="center">
<h3>
〰️〰️〰️〰️〰️ 2.2 Representación Matricial de Transformaciones 〰️〰️〰️〰️〰️
</h3>
</div>

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

[ESPACIO PARA IMAGEN 3: CAPTURA DEL EJERCICIO]

Recomendación: Un GIF o captura de pantalla de Blender donde se vea tu objeto moviéndose en el plano con el código de fondo.
