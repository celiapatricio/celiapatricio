## 📖 Proyectos Públicos

[🔙 Volver al resumen general](README.es.md)

### [2024] Sistema Peer-to-peer de Distribución de Ficheros.

Este proyecto desarrolla un sistema distribuido peer-to-peer para la compartición de ficheros entre clientes, implementado mediante una combinación de tecnologías como C, Python, Bash y servicios web basados en SOAP. La solución integra comunicación por sockets TCP, ejecución concurrente mediante hilos, y llamadas a procedimientos remotos (RPC), todo bajo una arquitectura modular y escalable. El cliente actúa como intérprete multihilo, mientras que el servidor maneja peticiones concurrentes, gestiona una base de datos binaria y se comunica con otros módulos. Además, incorpora pruebas funcionales y de concurrencia entre diferentes sistemas operativos, lo que demuestra su robustez y portabilidad. 

[*Repositorio Sistema Peer-to-peer: Distribución de Ficheros*](https://github.com/celiapatricio/sistema-peer-to-peer.git)


### [2024] Proyectos Prácticos en Sistemas Operativos: Programación en Entornos Unix/Linux.

Este repositorio recoge el trabajo completo realizado en la asignatura de Sistemas Operativos durante el curso 2023–2024, incluyendo el desarrollo desde cero de utilidades clásicas de Unix (como `wc` o `ls`), un intérprete de comandos interactivo (*minishell*) con soporte para redirecciones, tuberías, mandatos internos e historial, y un sistema multi-hilo que simula operaciones concurrentes en una tienda mediante productores y consumidores sincronizados. Cada apartado incluye pruebas exhaustivas, gestión de errores y explicaciones detalladas de la implementación. 

[*Repositorio Proyectos de Programación en Sistemas Operativos*](https://github.com/celiapatricio/sistemas-operativos.git)


### [2024] Aprendizaje no Supervisado: Clasificación de tipos de Estrellas.

Este proyecto consiste en aplicar técnicas de aprendizaje automático no supervisado para identificar y clasificar distintos tipos de estrellas a partir de un conjunto de datos astronómicos. El objetivo es analizar si es posible reproducir las clasificaciones astronómicas tradicionales utilizando algoritmos de clustering y estrategias de codificación de atributos.

Dataset:

El dataset contiene 240 estrellas y los siguientes atributos:

- `Temperature`: Temperatura superficial (K)

- `L`: Luminosidad (en relación al Sol)

- `R`: Radio (en relación al Sol)

- `A_M`: Magnitud absoluta

- `Color`: Color del espectro

- `Spectral_Class`: Clase espectral (O, B, A, F, G, K, M)

Funcionalidades implementadas:

- Implementación de K-means desde cero:
    - Se debe crear una función propia de K-means.
    - Comparar su eficiencia y resultados con la implementación de scikit-learn.

- Tratamiento de variables categóricas
    
    Dos enfoques a comparar:
    - One-hot encoding
    - Codificación ordinal basada en el orden físico (energía o temperatura).

- Aplicación de múltiples algoritmos de clustering:
    - Además de K-means, aplicar al menos otro algoritmo (como DBSCAN o Agglomerative).
    - Comparar resultados entre algoritmos y diferentes codificaciones.

- Evaluación de resultados:
    - Discutir si los grupos obtenidos tienen correspondencia con las clases estelares usadas en astronomía (enana blanca, supergigante, etc.).

- Propuesta de pipeline de clustering
    - Diseñar un flujo de trabajo recomendado incluyendo:
        - Preprocesamiento (escalado, codificación, selección de atributos).
        - Algoritmo y configuración de hiperparámetros.
        - Forma de analizar los resultados.

[*Repositorio Clustering Clasificación de Estrellas*](https://github.com/celiapatricio/Star_Classification_Clustering.git)


### [2024] Compilador para el lenguaje AJS: Analizador léxico, sintáctico y semántico.

Este proyecto es una extensión de una práctica previa, en la cual se desarrolló un analizador léxico y sintáctico para el lenguaje AJS, una versión simplificada de JavaScript. En este proyecto, se completa la implementación del compilador incluyendo un analizador semántico y se refactorizan partes anteriores para permitir su integración. Todo el desarrollo se ha realizado en Python usando la librería `PLY`.

1. Analizador léxico.

    Utiliza expresiones regulares para identificar elementos del lenguaje como números (enteros, reales, binarios, octales, hexadecimales, notación científica), cadenas, caracteres, identificadores, operadores y palabras reservadas. Se gestionan los comentarios y los errores léxicos, y se automatizan pruebas para validar el correcto reconocimiento de tokens.

2. Analizador sintáctico.

    A partir de los tokens, se construye el árbol sintáctico con reglas de precedencia y producción. Se procesan declaraciones, asignaciones, estructuras condicionales, bucles, funciones y objetos AJSON. La gramática fue adaptada para facilitar la posterior incorporación del análisis semántico.

3. Gramática AJS.

    Se define una gramática detallada para el lenguaje, contemplando expresiones, estructuras complejas, tipos de datos básicos, declaraciones de objetos anidados, funciones con parámetros tipados y llamadas a funciones.

4. Analizador semántico.

    Se encarga de comprobar la coherencia del programa a nivel de tipos, declaraciones y contexto. Se gestionan tablas de símbolos globales y locales, se validan asignaciones, tipos de retorno, accesos a propiedades de objetos y sobrecarga de funciones. Además, se asegura que las condiciones en bucles y condicionales sean booleanas y que los bloques no estén vacíos.

[*Repositorio Compilador del lenguaje AJS*](https://github.com/celiapatricio/AJS_Language_Compiler.git)


### [2024] Prototipo de un Carrito de Compra Virtual Ubicuo

Este prototipo aborda el reto de sustituir el tradicional carrito de la compra físico por una solución basada en el dispositivo móvil como interfaz de interacción ubicua. El contexto parte de un caso realista como el *Black Friday* en El Corte Inglés, en el que el espacio físico se ve comprometido debido a la gran afluencia de clientes y sus carritos.

La solución propuesta integra tecnologías web, sensores del móvil (NFC, cámara, acelerómetro, micrófono, vibración) y comunicación en tiempo real mediante *socket.io*, para transformar el teléfono móvil en un dispositivo de interacción rico y adaptado al entorno físico de una tienda.

Estructura del sistema:

- Aplicación Web Cliente (`/www/cliente`): permite al cliente realizar todas las operaciones sobre el carrito virtual (agregar, eliminar, pagar, ordenar, etc.).
- Aplicación Web Empleado (`/www/empleado`): permite al dependiente visualizar los productos del cliente y gestionar el proceso de pago y preguntas.
- Servidor Node.js (`index.js`): gestiona la lógica de conexión, registro, comunicación en tiempo real y acceso a datos JSON.
- Archivos JSON (`empleados.json`, `registro.json`, `clientes.json`, etc.): simulan una pequeña base de datos para usuarios, empleados, productos y preguntas.

Funcionalidades implementadas:

- Interacciones ubicuas:

    1. Agregar producto al carrito → Escaneando un código QR desde la carpeta `QR`.
    2. Eliminar producto → Haciendo click sobre el producto y agitando el dispositivo.
    3. Marcar como favorito → Doble click sobre un producto.
    4. Ordenar carrito → Arrastrar productos hacia arriba/abajo mediante gestos táctiles.
    5. Pago por proximidad (NFC + Bluetooth LE) → Conexión con una caja simulada mediante *nRF Connect* usando `heart_rate` como servicio Bluetooth. El pago se efectúa acercando el móvil del cliente a este dispositivo.

- Funcionalidades adicionales:

    6. Inicio de sesión y registro para clientes y empleados → Validación de contraseñas, persistencia en archivos `.json`.
    7. Sistema de preguntas/respuestas en tiempo real → Cliente envía dudas por voz o texto; el empleado responde y ambas interfaces se sincronizan vía WebSocket.
    8. Cupones desbloqueables por movimiento → Los cupones aparecen al agitar el móvil, y se aplican automáticamente en el pago.
    9. Búsqueda de productos y geolocalización interna → El cliente busca un producto, se muestra en un mapa y su posición se actualiza al mover el dispositivo (simulación).

Tecnologías utilizadas:

- `Node.js` + `Express.js`

- `socket.io` para comunicación en tiempo real

- APIs Web de interacción:
  - `DeviceMotion` y `TouchEvent` para gestos
  - `Web Speech API` para entrada por voz
  - `Web NFC` y `Bluetooth Low Energy` para pago ubicuo

- HTML5, CSS3, JavaScript vanilla

- Archivos `.json` para persistencia de datos

[*Repositorio Prototipo Carrito Virtual Ubicuo*](https://github.com/Belen-gomez/AplicacionCarritoCompra.git)


### [2024] Predicción de Producción de Energía Eólica con Scikit-Learn

Este proyecto tiene como objetivo construir un sistema de aprendizaje automático capaz de predecir la energía eléctrica que generará un parque eólico con 24 horas de antelación, utilizando variables meteorológicas proporcionadas por el modelo ECMWF. El proyecto sigue un enfoque completo de Machine Learning, que incluye el análisis exploratorio de datos, selección y ajuste de modelos, evaluación de rendimiento y predicciones sobre nuevos datos.

Objetivos: 

- Predecir la producción energética del parque eólico de Sotavento (Galicia).

- Aplicar distintos modelos de regresión (KNN, árboles, regresión lineal, Lasso y SVM).

- Realizar un análisis completo: EDA, selección de atributos, validación cruzada, ajuste de hiperparámetros.

- Evaluar el rendimiento del modelo y hacer predicciones reales con datos no etiquetados.

Metodología aplicada:

1. EDA (Exploratory Data Analysis):
   - Eliminación de variables no relevantes (solo se usan las de la posición 13 de la cuadrícula).
   - Detección de valores nulos, columnas constantes y normalización de datos.
   - Identificación de variables numéricas relevantes para la regresión.

2. Evaluación experimental:
   - Uso de validación cruzada doble (inner/outer loop).
   - Comparación entre varios modelos base y optimizados.
   - Evaluación con métricas como MAE, MSE y R².

3. Modelos implementados:
   - KNN
   - Árboles de decisión
   - Regresión lineal y Lasso
   - SVM
   - Regresores dummy para comparación de base

4. Ajuste de hiperparámetros.

5. Predicción final y competición:
   - Entrenamiento del mejor modelo sobre todos los datos.
   - Guardado del modelo (`modelo_final.pkl`) y generación de predicciones (`predicciones.csv`) para el dataset de competición.

6. Análisis adicional (clasificación):
   - Se transforma el problema en clasificación binaria (energía alta/baja).
   - Se compara el rendimiento de modelos clasificadores con nuevas métricas (F1-score, accuracy, etc.).

[*Repositorio Predicción de la producción de Energía Eólica*](https://github.com/celiapatricio/Energy_Prediction_System.git)

### [2023] Aplicación de Criptografía y Seguridad Informática: Hailo.

Este proyecto consiste en desarrollar una aplicación real en Python que permita aplicar los conceptos aprendidos en teoría sobre criptografía moderna. La aplicación desarrollada llamada Hailo que permite a usuarios registrarse como conductores para publicar su ruta y encontrar a otros pasajeros que desean hacerla. En el desarrollo de la aplicación se utilizan técnicas de criptografía para cifrar los mensajes entre los usuarios, autenticar usuarios y mantener la integridad de la información.

Funcionalidades implementadas

1. Autenticación de usuarios.
   - Registro con nombre, correo, teléfono y contraseña.
   - Contraseñas derivadas de forma segura usando el algoritmo *Scrypt* (KDF) con `salt` aleatorio.
   - Límite de 3 intentos de inicio de sesión.
   - Rotación aleatoria de `salt` y clave derivada en el 50% de los logins exitosos.
   - Almacenamiento local de credenciales en `BaseDeUsuarios`.

2. Cifrado simétrico/asimétrico
   - Uso de criptografía asimétrica por usuario.
   - Generación automática de par de claves pública/privada al registrarse.
   - Claves almacenadas en `usuarios/{correo}/`.

3. MAC (Message Authentication Codes)
   - Uso de funciones HMAC para autenticar mensajes entre entidades.
   - Gestión modular a través de `comunicacion.py` y `claves.py`.

4. Firma digital
   - Las claves privadas permiten firmar mensajes como solicitudes de viaje.
   - Aunque `main.py` no realiza la firma directamente, está contemplada en el diseño modular del sistema.

5. Infraestructura PKI (certificados digitales)
   - Diseño de una jerarquía de autoridades de certificación:
     - AC raíz (autoridad principal)
     - AC de las mesas
     - AC de los clientes
   - Envío de cadenas de verificación con el mensaje, su firma y certificados:
     ```
     M, S(M), Ca, Cac1, Cacr
     ```

[*Repositorio Aplicación Criptográfica Hailo*](https://github.com/Belen-gomez/AplicacionCriptografia.git)


### [2023] Página Web del restaurante ficticio Oasis Rosa.

Este proyecto consiste en el desarrollo de una página web estática para un restaurante ficticio llamado Oasis Rosa, como parte de la práctica del bloque 1 de la asignatura Interfaces de Usuario. El objetivo principal es aprender a estructurar y diseñar sitios web utilizando HTML5 y CSS3, cumpliendo los principios de diseño responsive, buenas prácticas semánticas y validación W3C.

Tecnologías y características implementadas

- HTML5 semántico: uso adecuado de etiquetas header, nav, section, footer, etc.

- CSS3 (en hoja externa): para layout, fuentes, efectos visuales y media queries.

- Diseño responsive: mediante media queries para adaptación a dispositivos móviles y tablets (con breakpoints en 768px y 600px).

- Multimedia e interactividad:
    - Vídeo introductorio.
    - Carruseles de imágenes.
    - Enlaces funcionales (mailto, redes, mapa).
    - Formulario de comentarios.

[*Repositorio Página Web Restaurante Oasis Rosa*](https://github.com/celiapatricio/restaurante-oasis.git)

### [2023] Simulación de Dinámica de Fluidos en C++.

[PUBLICO] Este proyecto tiene como objetivo desarrollar una simulación de dinámica de fluidos 2D, en la que se representa el movimiento y evolución de partículas dentro de una malla espacial a lo largo del tiempo. El programa se ejecuta desde línea de comandos y toma como entrada un fichero binario con la configuración inicial del dominio de simulación y las partículas, devolviendo como salida otro fichero binario con los resultados de la evolución.

[*Repositorio Simulación de Fluidos*](https://github.com/GLuis189/PracticaAC.git)


### [2023] Estructuras de Datos y Algoritmos.

Este proyecto de Estructura de Datos y Algoritmos se compone de dos fases complementarias: en la primera se amplían las funcionalidades de listas enlazadas simples con operaciones avanzadas como eliminación de secuencias, rotaciones y detección de bucles; en la segunda se extienden los árboles binarios de búsqueda con algoritmos para hallar distancias entre nodos y combinar árboles mediante operaciones de conjunto. 

1. Fase 1: Operaciones sobre listas enlazadas simples (`SList2`)

En esta primera fase se desarrolla una clase `SList2`, una extensión de listas enlazadas simples (`SList`), que incorpora nuevos métodos avanzados para manipular y corregir la estructura de la lista.


Funcionalidades implementadas:
- `delLargestSeq()`
    
    Elimina la secuencia más larga de elementos consecutivos con el mismo valor. Recorre la lista buscando secuencias repetidas. Al encontrar la más larga, ajusta los punteros para eliminarla. Se actualiza el tamaño de la lista correctamente.

- `fix_loop()`

    Detecta y elimina bucles (loops) en la lista enlazada. Comprueba si algún nodo apunta de nuevo a uno anterior. Si detecta el ciclo, corta la referencia para romper el bucle. Devuelve True si encuentra y corrige un bucle, False si no lo hay.

- `create_loop(position)`

    Método auxiliar para forzar un bucle artificial en la lista, uniendo el último nodo con un nodo intermedio. Útil para pruebas del método anterior.

- `leftrightShift(left, n)`
    
    Permite rotar la lista: Si left=True: mueve los primeros n nodos al final. Si left=False: mueve los últimos n nodos al inicio. Usa una lista auxiliar y actualiza los punteros de forma eficiente.

2. Fase 2: Operaciones sobre árboles binarios de búsqueda (`BST2`)

En esta segunda fase se implementa la clase `BST2`, una extensión de los árboles binarios de búsqueda (`BinarySearchTree`), que incorpora métodos avanzados para análisis y manipulación de árboles, como el cálculo de distancias entre nodos y la combinación de árboles mediante operaciones de conjunto. Se utilizan árboles AVL como estructura de salida para mantener el equilibrio.

Funcionalidades implementadas:
- `find_dist_k(n, k)`

    Devuelve una lista con todos los nodos del árbol que se encuentran exactamente a una distancia `k` del nodo con valor `n`. Para ello, se localiza el nodo objetivo y se calcula la distancia con cada otro nodo del árbol, considerando su ancestro común más bajo (LCA) y la suma de profundidades relativas. Utiliza una búsqueda recursiva combinada con funciones auxiliares.

- `create_tree(input_tree1, input_tree2, opc)`

    Genera un nuevo árbol AVL como resultado de aplicar una operación de conjunto entre dos árboles de entrada (`input_tree1`, `input_tree2`), según el parámetro `opc`. Las operaciones soportadas son:
  
    - `merge`: Devuelve un árbol que contiene la unión de los elementos de ambos árboles.
    - `intersection`: Devuelve un árbol con los elementos comunes a ambos árboles.
    - `difference`: Devuelve un árbol con los elementos que están en el primer árbol pero no en el segundo.

    Cada operación recorre los nodos de entrada de forma recursiva e inserta los elementos apropiados en el árbol AVL resultante.

[*Repositorio Estructuras de Datos y Algoritmos*](https://github.com/celiapatricio/estructura-datos-algoritmos.git)

