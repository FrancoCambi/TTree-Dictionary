# 🌳 T-Trees en Haskell

Este proyecto es una implementación de **T-Trees** (árboles tipo trie) en **Haskell**, que permite insertar, buscar, eliminar y extraer claves utilizando listas como claves compuestas. El árbol está diseñado para almacenar claves como secuencias y se comporta como un diccionario gracias a una typeclass.

---

## 🧠 Descripción

Un `TTree` puede ser:

- Una **Hoja (Leaf)**: un par clave-valor  
- Un **Nodo (Node)**: con una clave, un valor opcional, y tres subárboles:
  - Izquierdo: para claves menores a la actual
  - Medio: para continuar claves compuestas
  - Derecho: para claves mayores a la actual  
- O **E**: un árbol vacío

La implementación soporta:

- Búsqueda de valores a través de listas de claves (`search`)  
- Inserción de pares clave-valor (`insert`)  
- Eliminación de entradas (`delete`)  
- Obtención de todas las claves (`keys`)  
- Una **typeclass `Dic`** que abstrae estas operaciones y trata al `TTree` como un diccionario con claves de tipo `[k]`

---

## 🛠️ Tecnologías utilizadas

- **Haskell**
- **GHC (Glasgow Haskell Compiler)**

---

## 📦 Estructura del Proyecto

- `TTree k v`: Estructura de datos principal  
- `search`: Busca un valor dado una lista de claves  
- `insert`: Inserta o actualiza un valor en una ruta de claves  
- `delete`: Elimina un valor del árbol  
- `keys`: Devuelve todas las claves compuestas del árbol  
- `Dic`: Typeclass que provee una interfaz de diccionario para `TTree`

---

## ✅ Estado del Proyecto

- 🔧 Funcionalidad principal completa  
- 📚 Bien estructurado para extender o probar  
- 🧪 Fácil de integrar en programas funcionales más grandes

---

## ▶️ Cómo usarlo

1. Asegurate de tener **GHC** instalado.  
2. Guardá el código en un archivo, por ejemplo `TTree.hs`.  
3. Cargalo en GHCi:
   ```bash
   ghci TTree.hs
   ```
