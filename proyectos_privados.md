## 🔒 Proyectos Privados

[🔙 Volver al resumen general](README.es.md)

### [2024] Compilador de AJS.

Este proyecto implementa un compilador completo para el lenguaje AlmostJavaScript (AJS). AJS es un lenguaje imperativo, débilmente tipado, inspirado en JavaScript, que soporta tipos básicos, objetos, estructuras de control y funciones definidas por el usuario.

Funcionalidades implementadas:

- Análisis léxico con `ply.lex`:
    - Reconocimiento de tokens: números en distintas bases (decimal, binario, octal, hexadecimal), flotantes, caracteres, booleanos, `null` y palabras reservadas.
    - Manejo correcto de comentarios (`//` y `/* */`).

- Análisis sintáctico con `ply.yacc`:
    - Gramática en forma BNF que define declaraciones, expresiones, asignaciones, objetos, funciones y estructuras de control.
    - Reglas organizadas jerárquicamente para evitar ambigüedades.

- Análisis semántico:
    - Tabla de símbolos con tipos inferidos para variables.
    - Tabla de registros para objetos y sus propiedades.
    - Comprobación de tipos y conversiones (por ejemplo, carácter → entero, entero → flotante).
    - Validación de funciones: número de parámetros, tipos y retorno.

[*Repositorio Compilador AJS*](https://github.com/NathaliaMoniz/P2-Practica-Final-PDL.git)


### [2024] Analizador léxico y sintáctico de un tipo de JSON llamado AJSON.

Este proyecto consiste en el desarrollo de un analizador léxico y sintáctico para un lenguaje tipo JSON llamado AJSON, utilizando la librería `PLY` de Python. El objetivo es reconocer, analizar y mostrar la estructura de archivos escritos en este formato extendido, permitiendo además operaciones de evaluación sobre comparaciones y valores.

- Lexer (`ajson_lexer.py )
  
  Implementa el analizador léxico. Reconoce:
  
  - Tipos numéricos: enteros, reales, notación científica, binarios, octales y hexadecimales
  - Cadenas con y sin comillas
  - Operadores (`<`, `>`, `==`, `<=`, `>=`)
  - Palabras clave (`null`, `true`, `false`)
  - Estructura sintáctica básica (`{`, `}`, `:`, `,`)

- Parser (`ajson_parser.py`) 
  
  Implementa la gramática del lenguaje AJSON. Permite:
  
  - Evaluación de valores y comparaciones
  - Interpretación de estructuras anidadas
  - Unión de diccionarios como estructura de datos de salida
  - Impresión estructurada del árbol anidado

[*Repositorio Analizador léxico y sintáctico AJSON*](https://github.com/NathaliaMoniz/P1-Introduccion-PDL.git)


### [2023] Problemas de Satisfacción de Restricciones y Búsqueda Heurística.

[PRIVADO] Este proyecto se compone de dos partes diferenciadas, cada una centrada en resolver un problema mediante técnicas de satisfacción de restricciones y búsqueda heurística, respectivamente.

1. *[Nov 2023]* Satisfacción de Restricciones: Asignación de ambulancias a plazas de parking.

    Este proyecto consiste en asignar correctamente un conjunto de ambulancias (algunas con requisitos especiales, como conexión eléctrica o maniobrabilidad) a plazas de aparcamiento respetando una serie de restricciones.

    Modelado y resolución:
    - Se define el problema como un CSP con:
        - Variables: ambulancias
        - Dominios: plazas disponibles (con/sin conexión eléctrica)
        - Restricciones:
            - Cada ambulancia ocupa una única plaza.
            - Dos ambulancias no pueden compartir plaza.
            - Ambulancias con congelador deben aparcar en plazas con carga eléctrica.
            - Las ambulancias TSU deben tener plazas vacías a su lado.
            - Las TNU no pueden bloquear a una TSU delante suyo.
    - Se implementa en Python usando la librería `python-constraint`.
    - Se evalúan varios escenarios:
        - Casos con soluciones válidas de distinta complejidad.
        - Casos sin solución por falta de plazas o restricciones no cumplibles.
    - Se mejoró el rendimiento pasando de 15 minutos a unos 5 minutos de ejecución en escenarios grandes.

2. *[Dic 2023]* Búsqueda Heurística: Recogida y transporte de pacientes con A*.

    Este proyecto consiste en transportar pacientes (contagiosos y no contagiosos) desde sus domicilios hasta centros médicos respetando restricciones sanitarias y minimizando el coste energético mediante el algoritmo A*.

    Elementos del modelo:
    - Estado: posición de la ambulancia, ocupación de asientos y lista de pacientes por recoger.
    - Operadores:
        - Movimiento por el mapa.
        - Recogida y subida de pacientes (distinguiendo entre tipos).
        - Entrega de pacientes en el centro adecuado.
    - Restricciones:
        - Capacidad de la ambulancia (10 plazas, 2 para contagiosos).
        - Los pacientes contagiosos deben bajarse antes que los no contagiosos.
        - La energía del vehículo es limitada (50 unidades).
    - Heurística usada: distancia de Manhattan al parking.

[*Repositorio Satisfacción de Restricciones y Búsqueda Heurística*](https://github.com/celiapatricio/p2-471979-471948.git)


### [2023] Página web del restaurante ficticio Pixar Bites.

[PRIVADO] Este proyecto consiste en el desarrollo de una aplicación web interactiva y responsive para un restaurante ficticio y temático llamado *Pixar Bites*. El objetivo principal es aplicar conocimientos de diseño web, experiencia de usuario, accesibilidad y estructura modular en HTML, CSS y JavaScript. 

Tiene como finalidad educativa poner en práctica los Principios de Diseño Web, las Heurísticas de Usabilidad de Nielsen y los Patrones de Diseño de Interfaces de Usuario, integrándolos en una experiencia web accesible, coherente y atractiva.

Funcionalidades implementadas:
- Página principal (index.html)
    - Diseño responsive con barra de navegación tipo hamburguesa.
    - Secciones temáticas con navegación interna:
        - Nuestra Historia: presenta el origen del restaurante y su inspiración en el universo de Pixar.
        - Nuestro Local: muestra imágenes del comedor, barra y zona de juegos con descripciones.
        - Nuestra Cocina: carrusel automático de platos inspirados en el universo Pixar.
    - Galería interactiva con carrusel.
    - Estilos personalizados con fuentes importadas de Google Fonts.

- Reservas online (reserva.html): permite reservar mesa.

- Inicio de sesión y pedidos (inicio_sesion.html, pedido.html): secciones orientadas a servicios a domicilio.

- Reseñas y comentarios (resenas.html): espacio para opiniones de usuarios.

- Mini-juego temático (juego.html): sección lúdica para niños.

- Formulario de contacto (contacto.html): comunicación con el restaurante.

- Promociones activas (promociones.html): sección dinámica con ofertas.

[*Repositorio Página Web Pixar Bites*](https://github.com/Nachofc333/ProyectoInterfaces.git)


### [2023] Programación Lineal: Planificación óptima de centros de atención telefónica.

[PRIVADO] Esta práctica aborda la formulación y resolución de dos problemas de optimización entera en el contexto de la asignación de llamadas telefónicas a localizaciones de atención, con restricciones de capacidad, tiempo de respuesta y balance de carga. Se utiliza programación lineal entera mixta para encontrar soluciones óptimas que minimicen el tiempo o coste total del sistema.

1. *[Oct 2023]* Distribución con tres localizaciones existentes.

    Asignar llamadas entrantes desde distintos distritos (D1–D5) a tres localizaciones (L1–L3) minimizando el tiempo total de respuesta.

    Restricciones clave:
    - Cada localización tiene un límite máximo de llamadas.
    - El tiempo de respuesta máximo permitido para cada combinación localización-distrito.
    - Se busca un reparto equilibrado del esfuerzo entre localizaciones.

    Resultados:
    - Tiempo total mínimo: 483800
    - Todas las llamadas son atendidas cumpliendo las restricciones.
    - Llamadas distribuidas eficientemente entre L1 (principalmente D1 y D4), L2 (D1, D2 y D5) y L3 (D2 y D3).
    - La solución es óptima e íntegramente factible.

2. *[Oct 2023]* Ampliación con posibles nuevas localizaciones.
    
    Reformular el problema para permitir la construcción selectiva de nuevas localizaciones (L4, L5, L6) y decidir tanto la asignación de llamadas como la inversión en infraestructura, minimizando ahora el coste total (que combina construcción y operación).

    Restricciones adicionales:
    - Coste asociado a la apertura de cada nueva localización.
    - Cobertura mínima exigida por localización y distrito.
    - Como novedad, se introduce el uso de variables binarias para decidir la construcción (Se_construye) y asignación (Se_atiende).

    Resultado:
    - Coste total mínimo: 866700
    - Se decide construir L4 y L5, mientras que L6 no se construye.
    - Las llamadas se distribuyen entre seis localizaciones, incluyendo las nuevas.
    - La solución cumple todas las restricciones impuestas y es óptima según los criterios del solver.

[*Repositorio Proyecto de Programación Lineal*](https://github.com/celiapatricio/p1-471979-471948.git)


### [2023] Control óptimo de un Termostato con Programación Dinámica.

[PRIVADO] Esta práctica implementa una simulación para optimizar el uso de un termostato, utilizando técnicas de programación dinámica y simulación estocástica. El sistema toma decisiones automáticas para encender o apagar el termostato con el objetivo de alcanzar un estado final (temperatura objetivo) minimizando el coste energético.

Funcionalidades principales:

- Lectura de datos de transición desde ficheros CSV (t1.csv, t2.csv), que contienen las probabilidades de transición entre estados (temperaturas) al encender o apagar el termostato.

- Cálculo de la política óptima mediante la ecuación de Bellman, que estima el coste mínimo para cada estado (v(s)) y determina si es mejor encender o apagar en cada caso.

- Simulación paso a paso, en la que el usuario introduce la hora y el estado inicial, y el programa va tomando decisiones hasta alcanzar el estado final (22.0), mostrando en cada paso: la hora, la acción tomada (encender/apagar) y el nuevo estado alcanzado.

[*Repositorio MDP Termostato*](https://github.com/celiapatricio/practica_termostato.git)

### [2023] Proyecto enfocado al Desarrollo de Software.

[PRIVADO] Este conjunto de ejercicios aborda distintas competencias fundamentales en el desarrollo de software, combinando aspectos técnicos y éticos. Permiten demostrar lo aprendido poniéndolo en práctica, y proporcionan una base sólida para el desarrollo de software ético, estructurado y mantenible.

1. *[Ene 2023]* Aspectos Éticos y Legales de la Ingeniería del Software

    Este ejercicio plantea un dilema ético en el que Ana, ingeniera informática, debe decidir si actuar de forma ética o priorizar los intereses de su empresa. Se analizan los actores implicados, se aplican artículos del Código Ético del CCII y se reflexiona sobre qué haría un buen profesional ante esta situación. El objetivo es desarrollar pensamiento crítico y responsabilidad profesional.

2. *[Feb 2023]* Normativa de Estilo y Buenas Prácticas de Codificación.

    Este ejercicio está centrado en establecer y aplicar un conjunto de reglas de estilo y convenciones de codificación para un proyecto desarrollado en Python, utilizando la herramienta pylint como sistema de validación. El objetivo principal es garantizar que el código fuente sea legible, coherente, mantenible y profesional, alineándose con las normas PEP8, que son el estándar de estilo más utilizado en Python.

    [*Repositorio Normativa de Código*](https://github.com/celiapatricio/G80.2023.T10.EG2.git)

3. *[Mar 2023]* Desarrollo Dirigido por Pruebas.

    En este ejercicio se implementan funcionalidades para la gestión de pedidos usando TDD (Test-Driven Development). Se abordan tres requisitos funcionales:

    - Solicitar envío de producto: validación de inputs (EAN13, dirección, tipo de pedido, teléfono, código postal) y generación de un OrderID.
    - Enviar producto: validación del archivo de entrada JSON y consistencia del hash.
    - Entregar producto: validación del tracking code y creación del archivo de entrega si el día es correcto.

    [*Repositorio Desarrollo Dirigido por Pruebas*](https://github.com/100471979/G80.2023.T10.EG3.git)

4. *[Abr 2023]* Refactoring y Diseño Simple.

    Este último ejercicio se centra en mejorar la calidad interna del código desarrollado en EG3 mediante:

    - Refactoring: eliminar malas prácticas como funciones largas, código duplicado, nombres misteriosos, clases grandes o comentarios innecesarios. Se siguen patrones comunes de mejora como Extraer Función o Extraer Clase.

    - Diseño Simple: implementación del patrón Singleton para garantizar una única instancia de OrderManager y las clases de almacén.

    - Normativa PEP8: adaptación del código a las reglas validadas por pylint.

    - Registro en GitHub: se exige seguimiento con commits y pruebas automatizadas (XML), asegurando una trazabilidad completa del desarrollo.

    El objetivo es consolidar la capacidad de refactorizar y diseñar software robusto, limpio y fácilmente mantenible.

    [*Repositorio Refactoring y Diseño Simple*](https://github.com/100471979/G80.2023.T10.EG4.git)
