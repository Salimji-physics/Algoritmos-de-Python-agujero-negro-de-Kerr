# Descripción

Los algoritmos publicados emplean el formalismo de la *Geometría Diferencial* y la *Relatividad General* para calcular numéricamente  y representar gráficamente geodésicas de observadores en caída libre y de la luz en torno a fuentes gravitatorias. En particular, se estudia la métrica de Kerr, con la cual podemos modelar la estructura y el comportamiento de agujeros negros que rotan.

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

<img width="503" height="329" alt="Geodésicas5" src="https://github.com/user-attachments/assets/6949898a-b885-4dd3-b9e8-361686589cfd" />

## Geodésicas luz

<img width="278" height="329" alt="Geodésicas14" src="https://github.com/user-attachments/assets/b4b1d8c8-6b73-4c58-bb7e-016681f4c8fe" />

<img width="365" height="363" alt="Geodésicas13" src="https://github.com/user-attachments/assets/def095b0-97be-4807-b10f-aa92d776b358" />

<img width="240" height="323" alt="Geodésicas12" src="https://github.com/user-attachments/assets/0a491283-3362-45a7-bab2-77525ff055ab" />

<img width="376" height="383" alt="Geodésicas11" src="https://github.com/user-attachments/assets/e1a483e7-5477-4215-90fa-3b02b0b16005" />

<img width="337" height="315" alt="Geodésicas10" src="https://github.com/user-attachments/assets/0dcde18b-2fd9-40ff-8b9c-c087fb19b94e" />

<img width="421" height="400" alt="Geodésicas9" src="https://github.com/user-attachments/assets/756926cf-5eb3-4558-acb2-20534de80335" />

<img width="863" height="284" alt="Geodésicas7" src="https://github.com/user-attachments/assets/9fe72dcc-5357-492b-95cb-a9d0f19f1cb0" />

<img width="656" height="293" alt="Geodésicas6" src="https://github.com/user-attachments/assets/73bca7f4-c406-424a-b037-29319e0c627d" />
