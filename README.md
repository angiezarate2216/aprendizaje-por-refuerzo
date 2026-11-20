# Optimización de Gestión de Inventario mediante Q-Learning 

Implementación de un modelo de **Aprendizaje por Refuerzo (Reinforcement Learning)** utilizando el algoritmo **Q-Learning** para resolver el problema dinámico de reposición de inventario bajo demanda. 

Proyecto desarrollado como entregable práctico para la Semana 14 de la Especialización en Analítica y Ciencia de Datos (Universidad de Cundinamarca).

---
Autores:
- Angie Chipatecua
- Kevin Díaz
## Descripción del Problema

La gestión de inventarios enfrenta un dilema operativo constante entre mantener disponibilidad de producto y minimizar costos logísticos:
* **Exceso de inventario:** Genera costos elevados de almacenamiento y capital inmovilizado.
* **Escasez de inventario:** Produce penalizaciones económicas directas, ventas perdidas y pérdida de clientes.

El objetivo de este proyecto es entrenar un agente inteligente capaz de aprender una **política óptima de reposición** que decida cuántas unidades ordenar en cada periodo, maximizando la recompensa acumulada (minimizando los costos totales operativos).

---

## Diseño del Modelo 

El entorno se modeló con los siguientes componentes:

| Componente | Definición en el Proyecto |
| :--- | :--- |
| **Agente** | Sistema automatizado de gestión de compras y reposición. |
| **Entorno (`InventoryEnv`)** | Almacén con capacidad máxima de `10` unidades y demanda diaria estocástica (`0` a `5` unidades). |
| **Espacio de Estados ** | Nivel actual de inventario al inicio del periodo: 0 a 10  (11 estados). |
| **Espacio de Acciones** | Cantidad de unidades a ordenar al proveedor: 0 a 6 (7 acciones). |
| **Sistema de Recompensas ** | Valor negativo de la suma de costos operativos en el periodo:<br>|
| **Algoritmo** | **Q-Learning **  con estrategia de exploración **epsilon-greedy** y decaimiento exponencial. |

---

## Estructura del Repositorio

```text
├── REINFORCEMENT_LEARNING.ipynb  # Script principal con el entorno MDP, entrenamiento Q-Learning y gráficas
└── README.md                 # Documentación del repositorio
