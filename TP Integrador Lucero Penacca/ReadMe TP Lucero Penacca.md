# Proyecto_Final— RAG local completo con interfaz Gradio

Tecnicatura Superior en Ciencias de Datos e IA — IFTS24
Materia: Técnicas de Procesamiento de Habla - Junio 2026

Profesor: Matías Barreto

Equipo: Sara Lucero y Victoria Penacca

El siguiente proyecto está orientado a analizar un género literario: la poesía, y una temática: el amor. En la voz de 3 autores de estilos muy diferentes: Jorge Luis Borges, Pablo Neruda y Gustavo Adolfo Bécquer. De cada uno elegimos 3 poemas, y además, sumamos 2 de Borges escritos originalmente en inglés.
Nos interesó experimentar cómo procesaba el modelo un lenguaje que se caracteriza por su elevada carga simbólica y la utilización de elementos como las metáforas, lo que suponíamos iba a presentar cierta dificultad, como sucede en el caso del uso de la ironía o el sarcasmo.
Además, agregamos un texto que compara los estilos de los 3 poetas, un breve ensayo, para darle información al sistema para que pudiera responder sobre la comparativa de los estilos. También sumamos las poesías en inglés para ver qué sucedía con el tema de incorporar otro idioma.
Hicimos 3 series de ejercicios. En cada caso repetimos las mismas 4 preguntas, pero fuimos subiendo los archivos progresivamente. En el Ejercicio 1, sólo subimos los archivos de Neruda y Bécquer. En el Ejercicio 2, sumamos lo de Borges y en el Ejercicio 3, el ensayo.
Esto lo hicimos en el modo local. Y también hicimos las mismas series cambiando el valor de k, modificando la cantidad de fragmentos que el programa tomaba para el análisis. Primero lo corrimos con 3 y después con 5. Cuando hicimos el cambio, borramos el archivo chroma_proyecto para que se volviera a generar y no tomara la información que ya tenía incorporada. En HuggingFace lo corrimos sólo con el valor 3.
Los resultados obtenidos los detallamos a continuación, así como nuestras conclusiones.
Esperamos que disfruten, como nosotras, de las posibilidades que nos dio la materia interactuando con este proyecto.

Breve descripción del Notebook: configuración y despliegue de LLMs locales con Ollama, procesamiento de documentos, bases de datos vectoriales con ChromaDB y desarrollo de sistemas RAG (Retrieval-Augmented Generation) completos integrando LangChain.


## Contenido
| Notebook | Tema |
|---|---|
| Proyecto_final_rag_gradio_POESIA | Proyecto integrador: RAG local completo con interfaz de usuario en Gradio y preparación de archivos (`app.py`, `requirements.txt`) para su despliegue en HuggingFace Spaces |
## Carpetas y Archivos PDF
| Carpeta | Descripción | Archivos |
|---|---|---|
| CARPETA_DATOS_POESIA | Esta carpeta incluye todos los textos que se utilizaron para el entrenamiento y testeo de la app | `Neruda`, `Bécquer`, `Borges poesía en español`, `Borges Two english poems` y `El amor en la poesía de Borges, Neruda y Bécquer` |



## Resultados del Proyecto

### Ejercicio RAG 1
**Archivos subidos:** 2 archivos con poesías de Neruda y Bécquer.
#### Pregunta 1
_¿Cuál es el tema transversal que se ve en todos los textos?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| El tema transversal que se ve en todos los textos es el amor y la poesía. | El tema transversal que se ve en todos los textos es el amor, la pasión, la pérdida y la eternidad del sentimiento frente al paso del tiempo y la existencia. | El tema transversal que se ve en todos los textos es el amor y su persistencia frente a la adversidad o el fin de la vida. Las líneas hablan del poder de la muerte y de la posibilidad de eventos catastróficos, pero enfatizan que la llama del amor nunca podría apagarse, independientemente de las circunstancias. Este tema central se retrata a través de la metáfora de eventos naturales y la muerte, pero subraya la fuerza duradera del amor. |
#### Pregunta 2
_Compará la poesía sobre el amor de Borges, Neruda y Bécquer_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| No se puede comparar la poesía sobre el amor de Borges, Neruda y Bécquer basándose únicamente en los documentos proporcionados, ya que estos solo contienen un poema de Gustavo Adolfo Bécquer. | Basándose únicamente en los documentos proporcionados, se puede comparar la poesía sobre el amor de Gustavo Adolfo Bécquer y Pablo Neruda. Gustavo Adolfo Bécquer: La poesía de Bécquer aborda el amor desde una perspectiva de la intensidad emocional y la pérdida, así como la naturaleza de la poesía misma. Se evidencia un amor que es una llama inquebrantable ("Pero jamás en mí podrá apagarse / La llama de tu amor") y un profundo sentimiento de anhelo y búsqueda, incluso después de la pérdida ("Mi alma no se contenta con haberla perdido. / Como para acercarla mi mirada la busca"). También reflexiona sobre el paso del tiempo y la irrecuperabilidad de la belleza pasada en su poema "Rima 52". Pablo Neruda: La poesía de Neruda se centra en la experiencia activa del deseo y la relación mutua. El poema describe una pasión donde existe un intercambio de sentimientos ("Yo la quise, y a veces ella también me quiso") y una admiración intensa por la persona amada ("Cómo no haber amado sus grandes ojos fijos"). Comparación: Mientras que Bécquer se enfoca en la perdurabilidad del amor como una llama interna y el dolor de la ausencia, Neruda enfatiza la experiencia del deseo mutuo y la intensidad de la conexión física y emocional. | Los documentos proporcionados contienen poesía de Gustavo Adolfo Bécquer, pero no hay poesía de Jorge Luis Borges o Pablo Neruda presentes. Para comparar la poesía sobre el amor de Borges, Neruda y Bécquer, necesitaríamos poemas específicos de cada uno de estos poetas. Una vez que se proporcionen los textos relevantes, podríamos analizar temas, estilos, imágenes y expresiones emocionales para realizar una comparación comparativa. Como no hay poemas de Borges y Neruda disponibles aquí, no podemos realizar dicha comparación. |
#### Pregunta 3
_¿A quién dedica Borges sus poesías en inglés?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| No se encuentra información en los documentos proporcionados sobre a quién dedica Borges sus poesías en inglés. | No se encuentra información en los documentos proporcionados sobre a quién dedica Borges sus poesías en inglés. | Los documentos proporcionados no contienen información específica sobre a quién Borges dedica sus poesías en inglés. La información solicitada no se encuentra en los textos proporcionados. |
#### Pregunta 4
_To whom does Borges dedicate his Two english poems?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| No se encuentra esta información en los documentos proporcionados. | No se encuentra información en los documentos proporcionados que responda a esa pregunta. | Los documentos proporcionados no contienen información sobre una dedicatoria de Jorge Luis Borges a dos poemas en inglés. La información solicitada no se encuentra dentro del texto proporcionado. |

### Ejercicio RAG 2
**Archivos subidos:** 4 archivos con poesías de Borges (en español y en inglés), Neruda y Bécquer.
#### Pregunta 1
_¿Cuál es el tema transversal que se ve en todos los textos?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| El tema transversal que se ve en todos los textos es la naturaleza del amor, el tiempo y la existencia frente a la inmutabilidad o el cambio del mundo. | El tema transversal que se ve en todos los textos es la complejidad del amor, el paso del tiempo, la memoria y la confrontación con la mortalidad y la pérdida. | El tema transversal que se ve en todos los textos es la inmutabilidad y la durabilidad del amor frente a las adversidades y cambios de la vida. A pesar de la mención de eventos catastróficos como el nublarse del sol, secarse el mar y romperse el eje de la tierra, el poema enfatiza que la llama del amor no podrá apagarse, subrayando su fuerza y persistencia duraderas. |
#### Pregunta 2
_Compará la poesía sobre el amor de Borges, Neruda y Bécquer_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| No se puede realizar la comparación solicitada, ya que los documentos proporcionados solo contienen un fragmento de poesía atribuida a Gustavo Adolfo Bécquer y no incluyen textos de Borges o Neruda. | No se puede realizar la comparación solicitada, ya que los documentos proporcionados solo contienen textos de Gustavo Adolfo Bécquer. No hay información sobre la poesía de Borges ni de Neruda. | Como no hay documentos específicos proporcionados sobre la poesía sobre el amor de Jorge Luis Borges, Pablo Neruda y Gustavo Adolfo Bécquer, no puedo comparar directamente sus obras en este contexto.Para una comparación adecuada, proporcione documentos o descripciones específicas de sus poemas o versos relacionados con el amor.|
#### Pregunta 3
_¿A quién dedica Borges sus poesías en inglés?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| Borges dedica su primer poema en inglés a Beatriz Bibiloni Webster de Bullrich. | Borges dedica su primer poema en inglés a Beatriz Bibiloni Webster de Bullrich. | Borges dedica sus poesías en inglés a Beatriz Bibiloni Webster de Bullrich. Esto se menciona en el documento con el título "To Beatriz Bibiloni Webster de Bullrich". |
#### Pregunta 4
_To whom does Borges dedicate his Two english poems?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| Borges dedica sus dos poemas ingleses a Beatriz Bibiloni Webster de Bullrich. | Borges dedica sus dos poemas ingleses a Beatriz Bibiloni Webster de Bullrich. | Borges dedicó sus dos poemas en inglés a Beatriz Bibiloni Webster de Bullrich. |

### Ejercicio RAG 3
**Archivos subidos:** 4 archivos con poesías de Borges (en español y en inglés), Neruda y Bécquer. 1 archivo con un análisis comparativo de los enfoques de los 3 autores en su obra poética sobre el amor.
#### Pregunta 1
_¿Cuál es el tema transversal que se ve en todos los textos?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| Memoria y la conciencia de su fragilidad. | Memoria y la conciencia de su fragilidad. | El tema transversal que se ve en todos los textos es la naturaleza duradera y resistente del amor, a pesar de las adversidades y eventos catastróficos que pueden ocurrir en el mundo, como los cambios en el sol, el mar, la tierra y la propia muerte. La línea "Pero jamás en mí podrá apagarse la llama de tu amor" enfatiza la perpetuidad del amor, destacándolo como un elemento constante y fuerte en medio de la impermanencia del mundo. |
#### Pregunta 2
_Compará la poesía sobre el amor de Borges, Neruda y Bécquer_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| La poesía amorosa de Borges, Neruda y Bécquer demuestra que un mismo sentimiento puede ser representado desde perspectivas muy diferentes y profundas. Las diferencias en su representación del amor son las siguientes: Gustavo Adolfo Bécquer: Muestra el amor como un sueño ideal y muchas veces doloroso. Busca capturar la emoción íntima y el ideal romántico de un amor absoluto. Pablo Neruda: Representa el amor como una pasión intensa que une el cuerpo, la naturaleza y la memoria, transformando el deseo en imágenes de extraordinaria fuerza sensorial. Jorge Luis Borges: Convierte el amor en una reflexión sobre el tiempo y la condición humana, alejándose de la expresión apasionada para acercarse a una mirada más filosófica, ligándolo al enigma del paso del tiempo y a la identidad personal. A pesar de estas diferencias, sus voces coinciden en un punto esencial: la memoria y la conciencia de la fragilidad del amor. | La poesía amorosa de Borges, Neruda y Bécquer demuestra cómo un mismo sentimiento puede adquirir matices profundamente distintos, aunque coinciden en temas esenciales como la memoria y la conciencia de la fragilidad. Las diferencias en su representación del amor son las siguientes: Gustavo Adolfo Bécquer: Muestra el amor como un sueño ideal y muchas veces doloroso. Busca capturar la emoción íntima y el ideal romántico de un amor absoluto, caracterizándose por la intimidad, la melancolía y la búsqueda de un amor ideal. Expresa el dolor del amor imposible o perdido. Pablo Neruda: Celebra la unión entre los cuerpos y la naturaleza, transformando el deseo en imágenes de extraordinaria fuerza sensorial. Representa el amor como una pasión intensa que une el cuerpo, la naturaleza y la memoria. Recuerda con nostalgia un amor que ya no existe. Jorge Luis Borges: Convierte el amor en una reflexión sobre el tiempo y la condición humana, acercándose a una mirada más filosófica. Lo presenta como un enigma ligado al paso del tiempo y a la identidad personal, desde la reflexión intelectual y la nostalgia del tiempo. En resumen, sus voces se distinguen así: Bécquer desde la intimidad romántica, Neruda desde la intensidad de los sentidos y la entrega apasionada, y Borges desde la reflexión intelectual y la nostalgia del tiempo. | 1. Perspectiva: Borges: Aborda el amor como un enigma ligado al paso del tiempo y a la identidad personal, con un enfoque filosófico.  Neruda: Centra el amor en la pasión intensa que une el cuerpo, la naturaleza y la memoria, celebrando la unión y la fuerza sensorial. Bécquer: Ilustra el amor como un sueño ideal y a menudo doloroso, enfocándose en la emoción íntima y el romanticismo absoluto. 2. Concepciones del ser humano: Borges: Reflexiona sobre el ser humano en términos de identidad personal y el paso del tiempo, sugiriendo una comprensión más abstracta y analítica del amor. Neruda: Exalta la conexión entre el cuerpo, la naturaleza y la memoria, presentando una visión más concreta y orgánica del
 |
#### Pregunta 3
_¿A quién dedica Borges sus poesías en inglés?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| No se proporciona información en los documentos sobre a quién Borges dedica sus poesías en inglés. | No se encuentra información en los documentos sobre a quién dedica Borges sus poesías en inglés. | Los documentos proporcionados no mencionan específicamente a quién dedica Borges sus poesías en inglés. La información proporcionada discute las temáticas y estilos de Borges en su poesía, como el amor, el tiempo, la identidad y la muerte, pero no da detalles sobre sus destinatarios en inglés.|
#### Pregunta 4
_To whom does Borges dedicate his Two english poems?_
| En local con k=3 | En local con k=5 | En HuggingFace |
|---|---|---|
| Borges dedica sus dos poemas en inglés a Beatriz Bibiloni Webster de Bullrich. | Borges dedica sus dos poemas a Beatriz Bibiloni Webster de Bullrich. | Borges dedicó sus "Two English Poems" a Beatriz Bibiloni Webster de Bullrich. Esto se puede ver en la dedicatoria al comienzo del poema, donde escribe "To Beatriz Bibiloni Webster de Bullrich." |

## Conclusiones
Como conclusiones generales vemos que la cantidad de fragmentos que el sistema lee determina absolutamente la riqueza de las respuestas. En algunos casos leía los 3 fragmentos de un solo archivo, lo que obviamente limita aún más sus respuestas. En algunos casos dice no tener información de algunos autores cuando sí estaba en el repositorio.
En el caso de leer 5 fragmentos incluso puede hacer un análisis comparativo aun sin el ensayo como insumo.
También es interesante ver que cuando se le consulta por la dedicatoria de las poesías en inglés con la pregunta formulada en español, dice no tener la información, pero cuando se le formula la pregunta en inglés, direcciona la consulta a los textos en inglés y encuentra la respuesta, aunque la escribe en español.
En síntesis, un sistema de estas características debidamente alimentado con material de calidad y con un modelo que permita hacer consultas amplias puede ser una fuente interesante de análisis literario. Pero se debe hacer con conocimiento de las 2 claves para obtener información de calidad: los textos que hay que proveer y la capacidad de procesamiento.

