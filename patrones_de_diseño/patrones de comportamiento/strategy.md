PATRÓN STRATEGY

Introducción al Patrón Strategy

El patrón Strategy, un patrón de comportamiento que permite encapsular algoritmos dentro de clases, facilitando el cambio de algoritmo o comportamiento durante la ejecución del programa.

Objetivo del Patrón Strategy:

El patrón Strategy tiene como meta ofrecer flexibilidad en la elección de algoritmos utilizados por una aplicación. Permite cambiar el comportamiento de un objeto en tiempo de ejecución, seleccionando entre una familia de algoritmos o estrategias.

Ejemplo Práctico: Videojuego de Pokémon

Imagina un videojuego de Pokémon donde existen varios tipos de ataques: especiales, físicos, y aquellos que cambian el clima o el estado del enemigo. Sin Strategy, el código para manejar estos ataques se volvería complejo y difícil de mantener, especialmente si consideramos la existencia de cientos de ataques diferentes.
Implementación con Strategy

Para gestionar esta complejidad, se puede utilizar el patrón Strategy:

    Se define una interfaz para los ataques, por ejemplo, IEstrategiaAtaque.
    Cada tipo de ataque implementa esta interfaz, encapsulando su comportamiento específico.
    En tiempo de ejecución, el juego puede cambiar la estrategia de ataque de un Pokémon según sea necesario, sin alterar el código que utiliza los ataques.

Ventajas del Patrón Strategy

    Flexibilidad: Facilita la adición de nuevos algoritmos sin modificar el código existente.
    Desacoplamiento: Separa la selección de algoritmos de su ejecución, reduciendo la dependencia entre el código cliente y los algoritmos.
    Reutilización: Los algoritmos encapsulados como estrategias pueden reutilizarse en diferentes partes de la aplicación.

Otro Ejemplo: Sistemas de Logging

Considera una aplicación que necesita registrar información en diferentes destinos (consola, archivo, servidor remoto). Sin Strategy, el código para determinar dónde y cómo logear sería rígido y difícil de cambiar.

Implementación con Strategy para Logging

    Se define una interfaz ILogger con un método Log.
    Se implementan diversas estrategias para el logging: ConsoleLogger, FileLogger, RemoteLogger.
    La aplicación puede cambiar dinámicamente dónde y cómo se logea la información, simplemente cambiando la estrategia de logging utilizada.

Diagrama UML del Patrón Strategy

El patrón se compone de tres partes principales:

    Contexto: Mantiene una referencia a una estrategia y puede definirse para permitir el cambio de estrategia en tiempo de ejecución.
    Estrategia (Interfaz): Define una interfaz común para todas las estrategias concretas.
    Estrategias Concretas: Implementan diferentes algoritmos siguiendo la interfaz de estrategia.

Conclusión

El patrón Strategy es un poderoso aliado en el diseño de software, especialmente útil cuando necesitamos variabilidad en los algoritmos o comportamientos de nuestros objetos. Proporciona una solución elegante para mantener nuestro código flexible, mantenible y extensible.