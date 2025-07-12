## 📖 Public Projects

[🔙 Back to general summary](README.md)

### [2024] Peer-to-Peer File Distribution System

This project develops a distributed peer-to-peer system for file sharing among clients, implemented using a combination of technologies such as C, Python, Bash, and SOAP-based web services. The solution integrates TCP socket communication, multithreaded execution, and remote procedure calls (RPC), all under a modular and scalable architecture. The client acts as a multithreaded interpreter, while the server handles concurrent requests, manages a binary database, and communicates with other modules. It also includes functional and concurrency tests across different operating systems, demonstrating its robustness and portability.

[*Peer-to-Peer File Distribution System Repository*](https://github.com/celiapatricio/sistema-peer-to-peer.git)


### [2024] Practical Projects in Operating Systems: Programming in Unix/Linux Environments

This repository collects the complete work carried out in the Operating Systems course during the 2023–2024 academic year. It includes the development from scratch of classic Unix utilities (such as `wc` or `ls`), an interactive command interpreter (*minishell*) with support for redirections, pipes, built-in commands and history, and a multithreaded system simulating concurrent operations in a store using synchronized producers and consumers. Each section includes exhaustive tests, error handling, and detailed explanations of the implementation.

[*Operating Systems Programming Projects Repository*](https://github.com/celiapatricio/sistemas-operativos.git)


### [2024] Unsupervised Learning: Classification of Star Types

This project applies unsupervised machine learning techniques to identify and classify different types of stars based on an astronomical dataset. The goal is to analyze whether traditional astronomical classifications can be reproduced using clustering algorithms and attribute encoding strategies.

Dataset:

The dataset contains 240 stars and the following attributes:

- `Temperature`: Surface temperature (K)
- `L`: Luminosity (relative to the Sun)
- `R`: Radius (relative to the Sun)
- `A_M`: Absolute magnitude
- `Color`: Spectral color
- `Spectral_Class`: Spectral class (O, B, A, F, G, K, M)

Implemented functionalities:

- Custom implementation of K-means:
    - A self-built K-means function is required.
    - Compare its performance and results with scikit-learn’s version.

- Handling categorical variables:
    
    Two approaches compared:
    - One-hot encoding
    - Ordinal encoding based on physical order (e.g., energy or temperature)

- Application of multiple clustering algorithms:
    - In addition to K-means, at least one other algorithm is applied (such as DBSCAN or Agglomerative).
    - Compare results across algorithms and encoding methods.

- Results evaluation:
    - Discuss whether the resulting groups correspond to astronomical classes (white dwarf, supergiant, etc.).

- Clustering pipeline proposal:
    - Design a recommended workflow including:
        - Preprocessing (scaling, encoding, feature selection)
        - Algorithm and hyperparameter configuration
        - Analysis method

[*Star Classification Clustering Repository*](https://github.com/celiapatricio/Star_Classification_Clustering.git)


### [2024] AJS Language Compiler: Lexical, Syntactic, and Semantic Analyzer

This project extends a previous assignment in which a lexical and syntactic analyzer was developed for the AJS language, a simplified version of JavaScript. In this project, the compiler is completed with a semantic analyzer, and previous parts are refactored for integration. The entire development is done in Python using the `PLY` library.

1. Lexical analyzer

    Uses regular expressions to identify language elements such as numbers (integers, reals, binaries, octals, hexadecimals, scientific notation), strings, characters, identifiers, operators, and reserved words. It handles comments and lexical errors, and includes automated tests to validate correct token recognition.

2. Syntactic analyzer

    Builds the syntax tree from tokens using precedence and production rules. It processes declarations, assignments, conditionals, loops, functions, and AJSON objects. The grammar is adapted to facilitate semantic analysis.

3. AJS grammar

    A detailed grammar is defined, covering expressions, complex structures, basic data types, nested object declarations, typed function parameters, and function calls.

4. Semantic analyzer

    Ensures program consistency in terms of types, declarations, and context. It manages global and local symbol tables, validates assignments, return types, object property access, and function overloading. It also ensures that conditions in loops and if-statements are boolean, and that blocks are not empty.

[*AJS Language Compiler Repository*](https://github.com/celiapatricio/AJS_Language_Compiler.git)


### [2024] Prototype of a Ubiquitous Virtual Shopping Cart

This prototype tackles the challenge of replacing traditional physical shopping carts with a solution based on the mobile device as a ubiquitous interaction interface. It is inspired by a realistic scenario such as *Black Friday* at El Corte Inglés, where physical space becomes limited due to the large number of customers and carts.

The proposed solution integrates web technologies, mobile sensors (NFC, camera, accelerometer, microphone, vibration), and real-time communication via *socket.io*, turning the smartphone into a rich interaction device adapted to the physical store environment.

System structure:

- Client Web App (`/www/cliente`): allows the customer to perform all operations on the virtual cart (add, remove, pay, sort, etc.).
- Employee Web App (`/www/empleado`): allows the employee to view the customer’s products and manage the payment and questions.
- Node.js Server (`index.js`): handles connection logic, registration, real-time communication, and access to JSON data.
- JSON files (`empleados.json`, `registro.json`, `clientes.json`, etc.): simulate a small database for users, employees, products, and questions.

Implemented functionalities:

- Ubiquitous interactions:

    1. Add product to cart → Scan a QR code from the `QR` folder.
    2. Remove product → Tap product and shake the device.
    3. Mark as favorite → Double-click on a product.
    4. Sort cart → Drag products up/down with touch gestures.
    5. Proximity payment (NFC + Bluetooth LE) → Connect to a simulated checkout using *nRF Connect* with the `heart_rate` Bluetooth service. Payment occurs by bringing the phone close.

- Additional features:

    6. Login and registration for clients and employees → Password validation, persistence in `.json` files.
    7. Real-time Q&A system → Client sends questions by voice or text; employee responds and both interfaces sync via WebSocket.
    8. Coupons unlockable by motion → Coupons appear when the phone is shaken and apply automatically at checkout.
    9. Product search and indoor geolocation → Client searches for a product, it is displayed on a map, and its position updates as the device moves (simulated).

Technologies used:

- `Node.js` + `Express.js`

- `socket.io` for real-time communication

- Web Interaction APIs:
  - `DeviceMotion` and `TouchEvent` for gestures
  - `Web Speech API` for voice input
  - `Web NFC` and `Bluetooth Low Energy` for ubiquitous payment

- HTML5, CSS3, Vanilla JavaScript

- `.json` files for data persistence

[*Ubiquitous Virtual Shopping Cart Prototype Repository*](https://github.com/Belen-gomez/AplicacionCarritoCompra.git)


### [2024] Wind Power Production Prediction with Scikit-Learn

This project aims to build a machine learning system capable of predicting the electrical energy generated by a wind farm 24 hours in advance, using meteorological variables provided by the ECMWF model. The project follows a complete ML pipeline including exploratory data analysis, model selection and tuning, performance evaluation, and real predictions on new data.

Goals:

- Predict the energy output of the Sotavento wind farm (Galicia).
- Apply various regression models (KNN, decision trees, linear regression, Lasso, SVM).
- Conduct a full analysis: EDA, feature selection, cross-validation, hyperparameter tuning.
- Evaluate model performance and make predictions on unlabeled data.

Applied methodology:

1. EDA (Exploratory Data Analysis):
   - Remove irrelevant variables (only use those from grid position 13).
   - Detect null values, constant columns, normalize data.
   - Identify relevant numeric variables for regression.

2. Experimental evaluation:
   - Use double cross-validation (inner/outer loop).
   - Compare several base and optimized models.
   - Evaluate with metrics like MAE, MSE, and R².

3. Implemented models:
   - KNN
   - Decision trees
   - Linear regression and Lasso
   - SVM
   - Dummy regressors for baseline comparison

4. Hyperparameter tuning.

5. Final prediction and competition:
   - Train the best model on the full dataset.
   - Save the model (`modelo_final.pkl`) and generate predictions (`predicciones.csv`) for the competition dataset.

6. Additional analysis (classification):
   - Transform the problem into binary classification (high/low energy).
   - Compare classifier performance using new metrics (F1-score, accuracy, etc.).

[*Wind Energy Production Prediction Repository*](https://github.com/celiapatricio/Energy_Prediction_System.git)


### [2023] Cryptography and Information Security Application: Hailo

This project involves developing a real application in Python that applies modern cryptography concepts learned in theory. The developed application, called Hailo, allows users to register as drivers to publish their route and find passengers who want to join. The development includes cryptographic techniques for encrypting user messages, authenticating users, and maintaining data integrity.

Implemented functionalities:

1. User authentication
   - Registration with name, email, phone, and password.
   - Passwords securely derived using the *Scrypt* KDF algorithm with random `salt`.
   - Limit of 3 login attempts.
   - 50% chance of random `salt` and derived key rotation on successful login.
   - Local credential storage in `BaseDeUsuarios`.

2. Symmetric/asymmetric encryption
   - Asymmetric cryptography per user.
   - Automatic key pair generation at registration.
   - Keys stored in `usuarios/{email}/`.

3. MAC (Message Authentication Codes)
   - Use of HMAC functions to authenticate messages between entities.
   - Modular handling via `comunicacion.py` and `claves.py`.

4. Digital signature
   - Private keys are used to sign messages like ride requests.
   - Though `main.py` doesn't sign directly, it's considered in the system’s modular design.

5. PKI infrastructure (digital certificates)
   - Design of a certification authority hierarchy:
     - Root CA (main authority)
     - Table CA
     - Client CA
   - Messages include the chain of verification: 
     ```
     M, S(M), Ca, Cac1, Cacr
     ```

[*Hailo Cryptographic Application Repository*](https://github.com/Belen-gomez/AplicacionCriptografia.git)


### [2023] Website for the Fictional Restaurant Oasis Rosa

This project consists of building a static website for a fictional restaurant named Oasis Rosa, as part of a practical assignment in the User Interfaces course. The main goal is to learn how to structure and design websites using HTML5 and CSS3, following responsive design principles, semantic best practices, and W3C validation.

Technologies and features implemented:

- Semantic HTML5: proper use of header, nav, section, footer, etc.
- CSS3 (in external stylesheet): for layout, fonts, visual effects, and media queries.
- Responsive design: with breakpoints at 768px and 600px for mobile and tablet adaptation.
- Multimedia and interactivity:
    - Introductory video
    - Image carousels
    - Functional links (mailto, social media, map)
    - Feedback form

[*Oasis Rosa Restaurant Website Repository*](https://github.com/celiapatricio/restaurante-oasis.git)


### [2023] 2D Fluid Dynamics Simulation in C++

[PUBLIC] This project aims to develop a 2D fluid dynamics simulation that represents the motion and evolution of particles within a spatial grid over time. The program runs from the command line and takes a binary file as input, containing the initial configuration of the simulation domain and particles. It outputs another binary file with the results of the simulation.

[*Fluid Simulation Repository*](https://github.com/GLuis189/PracticaAC.git)


### [2023] Data Structures and Algorithms

This Data Structures and Algorithms project is divided into two complementary phases: the first expands the functionalities of singly linked lists with advanced operations such as sequence deletion, rotations, and loop detection; the second extends binary search trees with algorithms to calculate distances between nodes and to combine trees through set operations.

1. Phase 1: Operations on Singly Linked Lists (`SList2`)

In this first phase, the `SList2` class is developed as an extension of the singly linked list (`SList`), incorporating advanced methods to manipulate and fix the list structure.

Implemented functionalities:
- `delLargestSeq()`

    Removes the longest sequence of consecutive elements with the same value. It traverses the list looking for repeated sequences, deletes the longest one, and correctly updates the list size.

- `fix_loop()`

    Detects and removes loops in the linked list. It checks whether any node points back to a previous one. If a cycle is detected, it cuts the reference to break the loop. Returns True if a loop was found and corrected, False otherwise.

- `create_loop(position)`

    Auxiliary method to force an artificial loop in the list by linking the last node to an intermediate one. Useful for testing the previous method.

- `leftrightShift(left, n)`

    Rotates the list: If `left=True`, it moves the first `n` nodes to the end. If `left=False`, it moves the last `n` nodes to the beginning. Uses an auxiliary list and updates pointers efficiently.

2. Phase 2: Operations on Binary Search Trees (`BST2`)

In this second phase, the `BST2` class is implemented as an extension of the binary search tree (`BinarySearchTree`), adding advanced methods for tree analysis and manipulation, such as computing distances between nodes and combining trees via set operations. AVL trees are used as output to ensure balance.

Implemented functionalities:
- `find_dist_k(n, k)`

    Returns a list of all nodes in the tree that are exactly `k` links away from the node with value `n`. The method locates the target node and computes the distance to each other node by determining their Lowest Common Ancestor (LCA) and summing relative depths. It uses recursive search and helper functions.

- `create_tree(input_tree1, input_tree2, opc)`

    Generates a new AVL tree by applying a set operation between two input trees (`input_tree1`, `input_tree2`) based on the `opc` parameter. Supported operations are:
  
    - `merge`: Returns a tree containing the union of elements from both trees.
    - `intersection`: Returns a tree with elements common to both trees.
    - `difference`: Returns a tree with elements present in the first tree but not in the second.

    Each operation recursively traverses the input nodes and inserts the appropriate elements into the resulting AVL tree.

[*Data Structures and Algorithms Repository*](https://github.com/celiapatricio/estructura-datos-algoritmos.git)
