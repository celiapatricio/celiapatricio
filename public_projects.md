## 📖 Public Projects

[🔙 Back to general overview](README.es.md)

### [2024] Peer-to-peer File Distribution System

This project develops a peer-to-peer distributed system for file sharing between clients, implemented using a combination of technologies such as C, Python, Bash, and SOAP-based web services. The solution integrates TCP socket communication, multithreaded execution, and remote procedure calls (RPC), all under a modular and scalable architecture. The client acts as a multithreaded interpreter, while the server handles concurrent requests, manages a binary database, and communicates with other modules. It also includes functional and concurrency testing across different operating systems, demonstrating its robustness and portability.

[*Peer-to-peer File Distribution System Repository*](https://github.com/celiapatricio/sistema-peer-to-peer.git)

### [2024] Practical Projects in Operating Systems: Programming in Unix/Linux Environments

This repository contains the complete work developed in the Operating Systems course during the 2023–2024 academic year, including the development from scratch of classic Unix utilities (like `wc` or `ls`), an interactive command interpreter (*minishell*) with support for redirections, pipes, built-in commands and history, and a multithreaded system that simulates concurrent operations in a store using synchronized producers and consumers. Each section includes exhaustive testing, error handling, and detailed explanations of the implementation.

[*Operating Systems Programming Projects Repository*](https://github.com/celiapatricio/sistemas-operativos.git)

### [2024] Unsupervised Learning: Star Type Classification

This project consists of applying unsupervised machine learning techniques to identify and classify different types of stars from an astronomical dataset. The goal is to analyze whether it is possible to reproduce traditional astronomical classifications using clustering algorithms and attribute encoding strategies.

Dataset:

The dataset contains 240 stars and the following attributes:

- `Temperature`: Surface temperature (K)

- `L`: Luminosity (relative to the Sun)

- `R`: Radius (relative to the Sun)

- `A_M`: Absolute magnitude

- `Color`: Spectrum color

- `Spectral_Class`: Spectral class (O, B, A, F, G, K, M)

Implemented features:

- K-means implementation from scratch:
    - A custom K-means function must be created.
    - Compare its efficiency and results with scikit-learn's implementation.

- Handling of categorical variables
    
    Two approaches to compare:
    - One-hot encoding
    - Ordinal encoding based on physical order (energy or temperature)

- Application of multiple clustering algorithms:
    - In addition to K-means, apply at least one other algorithm (e.g., DBSCAN or Agglomerative).
    - Compare results between algorithms and different encodings.

- Result evaluation:
    - Discuss whether the obtained groups match the star classes used in astronomy (white dwarf, supergiant, etc.)

- Proposed clustering pipeline:
    - Design a recommended workflow including:
        - Preprocessing (scaling, encoding, feature selection)
        - Algorithm and hyperparameter configuration
        - Way to analyze the results

[*Star Classification Clustering Repository*](https://github.com/celiapatricio/Star_Classification_Clustering.git)

### [2024] Compiler for the AJS Language: Lexical, Syntax and Semantic Analyzer

This project is an extension of a previous lab, in which a lexical and syntax analyzer was developed for the AJS language, a simplified version of JavaScript. This project completes the compiler implementation by including a semantic analyzer and refactoring previous parts for integration. All development was done in Python using the `PLY` library.

1. Lexical analyzer.

    Uses regular expressions to identify language elements such as numbers (integers, floats, binaries, octals, hexadecimals, scientific notation), strings, characters, identifiers, operators, and reserved keywords. Comments and lexical errors are handled, and tests are automated to validate proper token recognition.

2. Syntax analyzer.

    From the tokens, the syntax tree is built using precedence and production rules. It processes declarations, assignments, conditional structures, loops, functions, and AJSON objects. The grammar was adapted to facilitate the later inclusion of semantic analysis.

3. AJS grammar.

    A detailed grammar is defined for the language, covering expressions, complex structures, basic data types, declarations of nested objects, functions with typed parameters, and function calls.

4. Semantic analyzer.

    Responsible for checking the program’s consistency in terms of types, declarations, and context. Global and local symbol tables are managed, assignments, return types, object property accesses, and function overloading are validated. It also ensures that conditions in loops and conditionals are boolean and that blocks are not empty.

[*AJS Language Compiler Repository*](https://github.com/celiapatricio/AJS_Language_Compiler.git)

### [2024] Prototype of a Ubiquitous Virtual Shopping Cart

This prototype addresses the challenge of replacing the traditional physical shopping cart with a solution based on the mobile device as a ubiquitous interaction interface. The context is based on a realistic case like *Black Friday* at El Corte Inglés, where physical space is compromised due to the high influx of customers and their carts.

The proposed solution integrates web technologies, mobile sensors (NFC, camera, accelerometer, microphone, vibration), and real-time communication via *socket.io*, to transform the mobile phone into a rich interaction device adapted to the physical store environment.

System structure:

- Client Web App (`/www/cliente`): allows the customer to perform all operations on the virtual cart (add, remove, pay, sort, etc.)
- Employee Web App (`/www/empleado`): allows the clerk to view the customer’s products and manage the payment and query process.
- Node.js Server (`index.js`): manages the connection logic, registration, real-time communication, and access to JSON data.
- JSON files (`empleados.json`, `registro.json`, `clientes.json`, etc.): simulate a small database for users, employees, products, and questions.

Implemented features:

- Ubiquitous interactions
    1. Add product to cart → Scanning a QR code from the `QR` folder.
    2. Remove product → Clicking on the product and shaking the device.
    3. Mark as favorite → Double-clicking on a product.
    4. Sort cart → Dragging products up/down using touch gestures.
    5. Proximity payment (NFC + Bluetooth LE) → Connection to a simulated checkout using *nRF Connect* and the `heart_rate` Bluetooth service. Payment is made by bringing the customer’s phone close to this device.

- Additional features
    6. Login and registration for customers and employees → Password validation, persistence in `.json` files.
    7. Real-time Q&A system → Customer sends voice or text questions; the employee responds and both interfaces sync via WebSocket.
    8. Coupons unlocked by movement → Coupons appear when shaking the phone and are automatically applied at checkout.
    9. Product search and indoor geolocation → The customer searches for a product, it is shown on a map, and its position updates as the device moves (simulated).

Technologies used:

- `Node.js` + `Express.js`

- `socket.io` for real-time communication

- Web interaction APIs:
  - `DeviceMotion` and `TouchEvent` for gestures
  - `Web Speech API` for voice input
  - `Web NFC` and `Bluetooth Low Energy` for ubiquitous payment

- HTML5, CSS3, vanilla JavaScript

- `.json` files for data persistence

[*Ubiquitous Virtual Shopping Cart Prototype Repository*](https://github.com/Belen-gomez/AplicacionCarritoCompra.git)

### [2024] Wind Energy Production Forecasting with Scikit-Learn

This project aims to build a machine learning system capable of predicting the electric energy to be generated by a wind farm 24 hours in advance, using meteorological variables provided by the ECMWF model. The project follows a complete Machine Learning approach, including exploratory data analysis, model selection and tuning, performance evaluation, and predictions on new data.

Goals:

- Predict the energy output of the Sotavento wind farm (Galicia)

- Apply various regression models (KNN, trees, linear regression, Lasso, and SVM)

- Perform a complete analysis: EDA, feature selection, cross-validation, hyperparameter tuning

- Evaluate model performance and make real predictions on unlabeled data

Applied methodology:

1. EDA (Exploratory Data Analysis):
   - Removal of irrelevant variables (only those from grid position 13 are used)
   - Detection of null values, constant columns, and data normalization
   - Identification of relevant numerical variables for regression

2. Experimental evaluation:
   - Use of double cross-validation (inner/outer loop)
   - Comparison among several base and optimized models
   - Evaluation using metrics such as MAE, MSE, and R²

3. Implemented models:
   - KNN
   - Decision trees
   - Linear and Lasso regression
   - SVM
   - Dummy regressors for baseline comparison

4. Hyperparameter tuning

5. Final prediction and competition:
   - Training the best model on all available data
   - Saving the model (`modelo_final.pkl`) and generating predictions (`predicciones.csv`) for the competition dataset

6. Additional analysis (classification):
   - Transform the problem into binary classification (high/low energy)
   - Compare classifier performance using new metrics (F1-score, accuracy, etc.)

[*Wind Energy Prediction Repository*](https://github.com/celiapatricio/Energy_Prediction_System.git)
