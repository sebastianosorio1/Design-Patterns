PATRÓN FACTORY

Introducción al Patrón Factory

El patrón Factory, uno de los patrones de diseño más demandados y útiles en el desarrollo de software, especialmente en la programación orientada a objetos.

Problema que Resuelve:

Imaginemos el desarrollo de un videojuego donde los enemigos son una parte crucial. Para mantener el juego interesante, es esencial tener una variedad de enemigos y que su aparición sea impredecible para el jugador. Aquí es donde surge el problema: ¿cómo generar diferentes tipos de enemigos de manera aleatoria sin complicar el código?

Solución: Patrón Factory

El patrón Factory ofrece una solución elegante a este problema. La idea es encapsular la lógica de creación de enemigos en una "fábrica" dedicada, permitiendo la generación de enemigos de forma aleatoria o bajo ciertos criterios específicos sin afectar el resto del código.

Ejemplos de Implementación

    Random Enemy Factory: Genera enemigos aleatoriamente.
    Random Difficult Enemy Factory: Genera solo enemigos difíciles, adecuado para jugadores que buscan un mayor desafío.
    Bomba Factory: Genera un tipo específico de enemigo, como Bombas, siempre.

Cada una de estas fábricas hereda de una abstracción común que define el método para crear enemigos, permitiendo el uso de polimorfismo. Esto significa que podemos cambiar la estrategia de generación de enemigos sin alterar el código que utiliza estas fábricas.

Ventajas del Patrón Factory

    Flexibilidad: Permite cambiar fácilmente la estrategia de generación de enemigos sin modificar el código que depende de la fábrica.
    Reusabilidad: Encapsula la lógica de creación en un solo lugar, facilitando la reutilización y mantenimiento del código.
    Polimorfismo: Gracias a la abstracción común, se pueden utilizar diferentes fábricas de manera intercambiable.

Diagrama UML del Patrón Factory

El patrón se compone de la clase abstracta Producto (nuestra clase Entidad) y las clases ConcretoProducto (los diferentes tipos de enemigos). La clase Creador es el padre de todas nuestras fábricas, cada una implementando el método createEnemy.

Conclusión

El patrón Factory es fundamental cuando se necesita generar objetos de diversas clases bajo ciertos criterios sin complicar el código. Es especialmente útil en situaciones donde la flexibilidad y la reusabilidad son prioritarias. Con este patrón, podemos adaptar nuestro juego a diferentes niveles de dificultad y preferencias de los jugadores sin afectar la estructura general del código.