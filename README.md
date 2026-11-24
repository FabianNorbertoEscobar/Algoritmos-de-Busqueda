# Algoritmos de búsqueda

Proyecto de práctica para implementar y comparar dos algoritmos clásicos de búsqueda sobre arreglos de enteros: la búsqueda secuencial y la búsqueda binaria.

## Stack y herramientas

- **Lenguaje:** Java 8.
- **Entorno del proyecto:** Eclipse (incluye los archivos `.project`, `.classpath` y `.settings`).
- **Dependencias externas:** ninguna; solo se utiliza la biblioteca estándar de Java.

## Funcionalidades

- `Busqueda.secuencial(int[] v, int dato)` recorre el arreglo desde el inicio hasta encontrar el dato o llegar al final. No requiere que el arreglo esté ordenado.
- `Busqueda.binaria(int[] v, int dato)` divide repetidamente el intervalo de búsqueda a la mitad. **Requiere que el arreglo esté ordenado de menor a mayor.**
- Ambos métodos devuelven el índice del elemento encontrado, contando desde cero, o `-1` si no está presente.
- `Main` muestra un ejemplo de cada algoritmo buscando el valor `12`; presenta las posiciones en pantalla contando desde uno.

## Estructura

```text
.
├── src/
│   └── principalPackage/
│       ├── Busqueda.java  # Implementaciones de búsqueda
│       └── Main.java      # Ejemplos ejecutables
├── .classpath             # Configuración de Java 8 y carpetas del proyecto
├── .project               # Metadatos de Eclipse
└── .settings/             # Preferencias del compilador de Eclipse
```

## Compilar y ejecutar

Se necesita un JDK compatible con Java 8 o posterior. Desde la raíz del repositorio:

```bash
mkdir -p bin
javac -d bin src/principalPackage/*.java
java -cp bin principalPackage.Main
```

También se puede importar el repositorio en Eclipse como un proyecto existente y ejecutar `principalPackage.Main`.

## Prácticas y conceptos

La práctica permite observar cómo cambia el recorrido según la estrategia de búsqueda:

| Algoritmo | Requisito sobre los datos | Complejidad temporal | Complejidad espacial |
|---|---|---:|---:|
| Secuencial | Ninguno | O(n) | O(1) |
| Binaria | Arreglo ordenado | O(log n) | O(1) |

El ejemplo de búsqueda secuencial usa un arreglo desordenado; el de búsqueda binaria, uno ordenado. Para probar otros casos, se pueden cambiar los arreglos y el valor buscado en `Main`. Si se pasa un arreglo desordenado a `binaria`, el resultado no está garantizado.
