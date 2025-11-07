# Laboratorio No. 12 - Programación Funcional con Haskell


## Descripción del Proyecto

Este repositorio contiene la implementación de cuatro ejercicios desarrollados en **Haskell**, como parte del Laboratorio No. 12 de Teoría de la Computación. 

### Nota sobre Puntos Extra

**Este laboratorio fue implementado completamente en Haskell** 



## Estructura del Repositorio

```
Lab-12-CC2019/
│
├── README.md                    # Este archivo
├── Lab12TeoriaChet.ipynb        # Notebook de Jupyter con todos los ejercicios
├── Laboratorio_No_12.txt        # Instrucciones originales del laboratorio
└── Lab12.mkv                    # Video de demostración
```

---

## Ejercicios Implementados

### Ejercicio 1: Ordenamiento de Estructuras de Datos (25%)

**Objetivo:** Ordenar una lista de tuplas que representan dispositivos móviles, basándose en el campo del modelo.

**Entrada:**
```haskell
[("Nokia", 216, "Black"), ("Apple", 2, "Silver"), ("Huawei", 50, "Gold"), ("Samsung", 7, "Blue")]
```

**Salida:**
```haskell
[("Apple", 2, "Silver"), ("Samsung", 7, "Blue"), ("Huawei", 50, "Gold"), ("Nokia", 216, "Black")]
```

- Función lambda para extraer el campo de comparación
- `sortBy` con `comparing` de `Data.Ord`

---

### Ejercicio 2: Potencia N-ésima de Elementos (25%)

**Objetivo:** Calcular la potencia n-ésima de cada elemento en una lista de enteros.

**Entrada:**
```haskell
n = 3
lista = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

**Salida:**
```haskell
[1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]
```

- Función lambda `(\x -> x ^ n)`
- Función `map` para aplicar la transformación
- Aplicación parcial de funciones

---

### Ejercicio 3: Transposición de Matrices (25%)

**Objetivo:** Calcular la matriz transpuesta Xᵀ de una matriz X dada.

**Entrada:**
```haskell
X = [[1, 2, 3, 1],
     [4, 5, 6, 0],
     [7, 8, 9, -1]]
```

**Salida:**
```haskell
Xᵀ = [[1, 4, 7],
      [2, 5, 8],
      [3, 6, 9],
      [1, 0, -1]]
```

- `foldr` para reducción/acumulación
- `zipWith` con operador de construcción `(:)`
- Polimorfismo paramétrico

---

### Ejercicio 4: Filtrado de Elementos en Listas (25%)

**Objetivo:** Eliminar elementos específicos de una lista.

**Entrada:**
```haskell
lista_original = ["rojo", "verde", "azul", "amarillo", "gris", "blanco", "negro"]
elementos_a_borrar = ["amarillo", "café", "blanco"]
```

**Salida:**
```haskell
["rojo", "verde", "azul", "gris", "negro"]
```

- Función lambda con `not` y `elem`
- Función `filter` para selección condicional
- Restricción de tipo `Eq a`

---

## Instrucciones de Ejecución

### Prerrequisitos

1. **GHC (Glasgow Haskell Compiler)** instalado
2. **Python 3.x** (para ejecutar el notebook)
3. **Jupyter Notebook** o **Jupyter Lab**

### Opción 1: Ejecutar el Notebook de Jupyter

1. Abrir el archivo `Lab12TeoriaChet.ipynb` en Jupyter Notebook o VS Code
2. Ejecutar las celdas en orden secuencial
3. El notebook compilará y ejecutará automáticamente cada ejercicio


---

## Video de Demostración

https://github.com/Dcextrim/Lab-12-CC2019/Lab12.mp4

> El video demuestra la ejecución de los cuatro ejercicios, mostrando todos los casos de prueba y la correcta funcionalidad de cada implementación.

**Duración:** Menos de 10 minutos  
**Contenido:**
- Explicación de cada ejercicio
- Demostración de compilación con GHC
- Ejecución y verificación de resultados
- Casos de prueba adicionales

---

## Referencias

- [Haskell Documentation](https://www.haskell.org/documentation/)
- [Learn You a Haskell for Great Good!](http://learnyouahaskell.com/)
- [Haskell Wiki - Lambda Functions](https://wiki.haskell.org/Lambda_abstraction)
- [Data.List Documentation](https://hackage.haskell.org/package/base/docs/Data-List.html)

---