# Descripción

Los algoritmos publicados en el presente repositorio emplean el formalismo de la *Geometría Diferencial* y la *Relatividad General* para calcular numéricamente  y representar gráficamente geodésicas de observadores en caída libre y de la luz en torno a fuentes gravitatorias. En particular, se estudia la métrica de Kerr, con la cual podemos modelar la estructura y el comportamiento de agujeros negros que rotan.

El programa se encuentra codificado en lenguaje *Python*, valiéndose de la librería *SageManifolds*, incorporada en *SageMath*. Además, ha sido compilado en *Jupyter Notebook*, produciendo los resultados que se mostrarán a continuación.

La presentación y discusión completa de los resultados se encuentran recogidas en un trabajo de fin de grado titulado *Análisis Geométrico del Espacio-Tiempo de Kerr y sus Principales Propiedades Físicas*, del grado en Física por la Universidad de Córdoba.

# Resultados

## Agujero negro de Kerr

El programa [Kerr_calculos](Kerr_calculos.ipynb) define la métrica de Kerr y realiza, a partir de esta, diversos cálculos como su inversa o los tensores de curvatura de Ricci y Escalar. Estos últimos han sido empleados para calcular el *Escalar de Kretschmann*, el cual nos ha permitido buscar singularidades de curvatura en nuestra métrica. 

Por otro lado, a partir de la búsqueda de los ceros de la métrica y su inversa, así como de las inversiones de los signos de determinadas componentes de las mismas, se han extraído los diferentes horizontes y regiones del agujero negro de Kerr.

Al introducir las condiciones calculadas anteriormente en el programa [Kerr_graficas](Kerr_graficas.ipynb), se ha logrado representar gráficamente la estructura interna de los agujeros negros que rotan. Véase la siguiente figura:

<img width="390" height="260" alt="Agujero negro de Kerr" src="https://github.com/user-attachments/assets/9924486b-4112-4c53-bc1a-fdeb8da10e7c" />

Vemos cómo, a diferencia de los agujeros negros estáticos dados por la *métrica de Schwarzschild*, en este caso tenemos una singularidad anular evitable concéntrica con los horizontes y contenida en el plano perpendicular al eje de rotación. Además, pasamos a tener dos horizontes de sucesos y unas nuevas superficies a las que denominamos *S+* y *S-*. La región comprenida entre *S+* y el horizonte externo es denominada *ergosfera*. Todo observador que se encuentre dentro de esta se verá obligado a desplazarse en el sentido de rotación del agujero negro debido al efecto de arrastre o *frame dragging* que esta produce sobre el espacio-tiempo.

La imagen que se muestra a continuación recoge cómo varía el signo de las componentes temporal (g00) y espacial radial (g11) de la métrica al atravesar las distintas regiones del agujero negro:

<img width="431" height="245" alt="Regiones agujero negro de Kerr" src="https://github.com/user-attachments/assets/02f4a3ae-d87b-442a-8594-2a9bd97855e3" />

## Geodésicas temporales

**AVISO:**  de aquí en adelante, en la graficación de geodésicas, tan solo se visualizarán la ergosfera y el horizonte de sucesos externo del agujero negro para no saturar las figuras y facilitar su visualización. Además, se mostrará gráficamente la **posición inicial** con un punto de color amarillo y la componente espacial de la **velocidad inicial** con una flecha del mismo color que la curva de trayectoria.

En *Relatividad General*, las trayectorias que siguen los observadores en caída libre son curvas geodésicas temporales futuras unitarias. Como ejemplos de dichas curvas, se muestran a continuación casos sencillos de observadores lanzados con diferentes condiciones iniciales en la vecindad de un agujero negro de Kerr:

<img width="310" height="170" alt="Geodésicas1" src="https://github.com/user-attachments/assets/e7b41aed-991e-440d-9194-52ef4bfc0c72" />

<img width="285" height="170" alt="Geodésicas2" src="https://github.com/user-attachments/assets/9ec18ec1-2daf-4c7d-9ba9-73f5bb8227d4" />

A primera vista, vemos comportamientos usuales de objetos bajo efecto de un potencial gravitatorio: según la posición y velocidad iniciales dadas, se tienen trayectorias de caída y escape (imagen izquierda) u órbitas estables circulares y elípticas (imagen derecha). Sin embargo, en el caso particular de la órbita elíptica, observamos un efecto que no veíamos en el formalismo newtoniano: la *precesión relativista* de la órbita.

En la sección anterior, se introdujo el efecto de *frame dragging* de la ergosfera. En las siguientes imágenes, lo evidenciamos gráficamente colocando dos observadores al borde de la ergosfera, uno con componente espacial de la velocidad inicial nula, y otro con velocidad inicial cercana a la luz en sentido contrario a la rotación del agujero negro:

<img width="247" height="203" alt="Geodésicas4" src="https://github.com/user-attachments/assets/f652d62b-eba2-4970-8319-a3e50774a676" />

<img width="247" height="203" alt="Geodésicas3" src="https://github.com/user-attachments/assets/fd387f30-8c4e-49a4-8845-26e4ec8489f2" />

Cada figura muestra la misma situación vista desde dos perspectivas diferentes: una frontal y otra lateral. Vemos cómo, para ambas condiciones iniciales descritas anteriormente, cuando los observadores se adentran a la ergosfera por atracción gravitatoria, emprenden de forma inevitable una trayectoria en el sentido de giro del agujero negro.

En realidad, este efecto de arrastre también existe, en menor medida, fuera de la ergosfera. Esto es debido a la contribución a la métrica de un término cruzado entre la componente temporal y la espacial axial. Dicho término provocará una desviación de las trayectorias hacia el sentido de giro del agujero negro y, a medida que nos aproximamos a la ergosfera, dicho efecto es cada vez mayor. Dentro de la ergosfera, el término cruzado contiene la única contribución de la componente temporal a la métrica (g00 habrá pasado a ser espacial), de modo que tener una determinada velocidad hacia el futuro implica un movimiento inevitable en la coordenada axial.

Veamos representado el fenómeno que acabamos de describir. Si rescatamos la órbita circular que vimos en las primeras imágenes de esta sección y, junto a ella, lanzamos otro observador con condiciones iniciales idénticas pero invirtiendo el sentido de la componente espacial de la velocidad inicial, se obtiene la siguiente figura:

<img width="434" height="186" alt="Geodésicas8" src="https://github.com/user-attachments/assets/fc50f5f8-de97-4153-bcae-e4655237874f" />

Se observa cómo, en el caso en el que la velocidad inicial va en contra de la rotación del agujero negro, una trayectoria que en principio debiese formar una órbita circular idéntica al otro caso representado, en realidad se desvía por efecto del arrastre y acaba cayendo a su interior. Por lo tanto, estamos viendo dentro del marco relativista otro fenómeno que no se podría explicar desde el formalismo newtoniano: dado un mismo observador, con condiciones iniciales idénticas y bajo efecto de un mismo potencial gravitatorio, la trayectoria resultante varía con el sentido inicial de su velocidad espacial. Por otro lado, si la posición inicial se hubiese encontrado dentro de la ergosfera, como vimos en las dos imágenes anteriores, en lugar de recorrer una cierta distancia en sentido contrario a la rotación mientras se desvía lentamente hasta moverse a favor de esta, saldría directamente en sentido contrario a su velocidad espacial inicial.

Por último, veamos qué ocurre si tomamos una posición inicial común fuera de la ergosfera e iteramos el módulo de la velocidad inicial:

<img width="303" height="209" alt="Geodésicas5" src="https://github.com/user-attachments/assets/6949898a-b885-4dd3-b9e8-361686589cfd" />

Tenemos el mismo grupo de observadores repetidos al lado izquierdo y derecho del punto inicial, pero con sentido de la velocidad espacial inicial invertido. Si tan solo nos fijamos en el lado derecho, vemos el efecto esperado de una fuente gravitatoria: las curvas serán más o menos cerradas en torno al agujero negro en función del módulo de su velocidad inicial. Sin embargo, en el lado izquierdo volvemos a ver el mismo fenómeno que describimos anteriormente, al invertir el sentido de la velocidad las trayectorias se modifican completamente, desviándose por efecto del arrastre hasta ir en el mismo sentido de la rotación del agujero negro.

## Geodésicas luz

Una de las consecuencias físicas más revolucionarias e interesantes de la llegada de la *Relatividad General* fue descubrir que la trayectoria de la luz se ve curvada por efecto de potenciales gravitatorios. En este marco teórico, la luz se mueve siguiendo las llamadas geodésicas luminosas, y podemos ver cómo estas son afectadas por la métrica de Kerr en las siguientes figuras:

<img width="201" height="200" alt="Geodésicas9" src="https://github.com/user-attachments/assets/756926cf-5eb3-4558-acb2-20534de80335" />

<img width="197" height="200" alt="Geodésicas10" src="https://github.com/user-attachments/assets/0dcde18b-2fd9-40ff-8b9c-c087fb19b94e" />

En estas imágenes, se han representado geodésicas luz partiendo de puntos iniciales contenidos en el plano con coordenada azimutal de 45º y a diferentes distancias radiales del agujero negro. Ambas figuras muestran las mismas condiciones iniciales pero con sentidos de la velocidad espacial inicial contrarios. En el caso izquierdo, vemos cómo la luz se comporta de forma idéntica a cualquier observador bajo efectos de un campo gravitatorio: se curva en torno a la fuente gravitatoria y dichas curvas se vuelven más cerradas a medida que reducimos la distancia radial inicial, dando como resultado trayectorias de caída y trayectorias de escape. En la figura derecha, en cambio, vemos de nuevo cómo las curvas se ven desviadas por el efecto de arrastre de la rotación del agujero negro, evidenciando que también actúa sobre la luz.

Veamos qué ocurre si, para las mismas posiciones iniciales, lanzamos la luz en la dirección azimutal:

<img width="210" height="283" alt="Geodésicas12" src="https://github.com/user-attachments/assets/0a491283-3362-45a7-bab2-77525ff055ab" />

Se vuelve a poner de manifiesto el efecto del *frame dragging* sobre las geodésicas luz, inclinándolas hacia la derecha (sentido de rotación del agujero negro). Además, en esta imagen es mucho más fácil ver cómo, a medida que las posiciones iniciales son más cercanas a la ergosfera, el efecto de arrastre se va haciendo más notorio (las inclinaciones de las trayectorias se vuelven más pronunciadas).

De la misma forma que con las geodésicas temporales, es lógico preguntarse si existen condiciones iniciales para las cuales las geodésicas luz forman órbitas circulares estables en torno al agujero negro. Dada la gran dificultad que supone encontrar dichas condiciones a base de prueba y error, se ha creado un procedimiento para calcularlas. Para ello, se ha empleado el formalismo de Euler-Lagrange, aplicando condición de coordenada radial invariante (buscamos circunferencias) y condición de vectores luminosos. Además, comenzaremos estudiando el caso en el que la velocidad inicial espacial se encuentra contenida en la coordenada axial (es decir, la componente azimutal también es nula). 

Como resultado, se ha calculado e implantado en [Kerr_graficas](Kerr_graficas.ipynb) una función que toma como parámetros de entrada la componente azimutal de la posición inicial y devuelve los únicos valores de la componente radial de la posición inicial (recordemos que no necesitamos la axial, pues la métrica de Kerr es axialmente simétrica) y la componente azimutal de la velocidad inicial para los cuales se encontrarán órbitas circulares estables si estas existen. 

Tomando un ángulo azimutal inicial de 90º, es decir, al buscar órbitas contenidas en el plano ecuatorial del agujero negro (recordemos que la velocidad espacial inicial no se sale de la dirección axial), se obtienen los siguientes 2 resultados:

<img width="406" height="193" alt="Geodésicas6" src="https://github.com/user-attachments/assets/73bca7f4-c406-424a-b037-29319e0c627d" />

Estos son los denominados *anillos luz del agujero negro de Kerr*, y se clasifican en:
* *Curva prógrada:* representada en color rojo. Es la correspondiente a una velocidad inicial en el mismo sentido que la rotación del agujero negro y un radio inicial más pequeño.
* *Curva retrógada:* representada en color verde. Es la correspondiente a una velocidad inicial en sentido contrario a la rotación del agujero negro y un radio inicial más grande.

Cabe notar que la curva prógrada no se ha podido dibujar completamente debido a las limitaciones de exactitud del método numérico empleado (valores límites de tolerancia y paso del programa) y a la gran inestabilidad que produce encontrarse tan cerca del horizonte de sucesos. 

Vemos que los agujeros negros de Kerr pueden poseer 2 órbitas estables circulares de luz en su plano ecuatorial. A continuación, es lógico preguntarse cómo afecta a estas órbitas el efecto de arrastre de la rotación, al igual que hicimos con las geodésicas temporales en la sección anterior. Para ello, volvemos a representar la órbita circular retrógada (ahora en color rojo), junto con otra curva (verde) que parte con las mismas condiciones iniciales pero sentido opuesto de la velocidad axial inicial (es decir, a favor de la rotación):

<img width="863" height="284" alt="Geodésicas7" src="https://github.com/user-attachments/assets/9fe72dcc-5357-492b-95cb-a9d0f19f1cb0" />

Probemos ahora el mismo algoritmo para casos fuera de dicho plano. Por ejemplo, ángulo azimutal inicial de 45º:

<img width="376" height="383" alt="Geodésicas11" src="https://github.com/user-attachments/assets/e1a483e7-5477-4215-90fa-3b02b0b16005" />

<img width="278" height="329" alt="Geodésicas14" src="https://github.com/user-attachments/assets/b4b1d8c8-6b73-4c58-bb7e-016681f4c8fe" />

<img width="365" height="363" alt="Geodésicas13" src="https://github.com/user-attachments/assets/def095b0-97be-4807-b10f-aa92d776b358" />
