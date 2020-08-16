# Desafio1 Maraton IBM

## Alestra, Asistente-virtual

### Objetivo:

La idea del desafío es ayudar a los empleados del área de soporte de una empresa a realizar un servicio más rápido y objetivo, para que quienes necesitan soporte hablen primero con un Asistente Virtual y así identificar la demanda generando al final un ticket que deberá ser resuelto por soporte.

Este desafío debe resolverse con Watson Assistant y tu tarea será implementar el Asistente Virtual con inteligencia artificial para identificar las demandas del usuario para la generación de tickets.

### **Desarrollo:**

Watson Assistant es la herramienta creada por IBM para crear asistentes virtuales. A través de ejemplos de formas en que el usuario se comunica y utilizando inteligencia artificial, es capaz de identificar lo que se está escribiendo. Watson no es una herramienta que lo sepa todo, funciona dentro de cierto ámbito. Por lo tanto, al interactuar con él sobre otro tema, no estará seguro de responder correctamente.

Watson Assistant funciona sobre la base de `intents`. Identifican lo que el usuario quiere hacer y podemos asociarlos con verbos, por ejemplo: 'Quiero un café' y 'Un jugo de naranja por favor' son ejemplos de cómo pedir una bebida y podemos definir la `intent` de ordenar bebidas. Es importante dejar en claro que la inteligencia artificial se aplica a las `intents` y que al insertar ejemplos sobre una determinada `intent`, Watson creará un modelo de lenguaje natural capaz de identificar lo que el usuario está buscando.

Es común que una `intent` sea genérica hasta el punto de que Watson solo identifique la acción del usuario. 'Quiero un café' y 'Un jugo de naranja por favor' indican a Watson que el usuario quiere una bebida, pero no especifica cuál. Para llevar a cabo esta diferenciación de objetos existen `entities` que funcionan como una clase que agrega sus objetos. Para los ejemplos citados es posible distinguir la `entity` 'Bebida' cuyos objetos son 'café' y 'jugo de naranja'. De esta forma Watson podrá identificar la acción del usuario y a qué objeto se refiere.

Con las `intents` y las `entities` creadas, es posible establecer un diálogo. El diálogo sigue la estructura computacional del árbol y se accede a sus nodos a través de las condiciones establecidas por el desarrollador, y estas condiciones son `intents` y `entities`. En otras palabras, el diálogo no es más que la respuesta proporcionada por Watson al identificar la condición de un nodo.

En este repositorio, en el directorio [dataset](https://github.com/sergio2526/desafio-1-2020/blob/master/dataset) hay una 'Skill' que debe usarse como punto de partida para desarrollar la solución. Ella ya tiene todas las `intents` y `entities` necesarias para resolver el desafío.

- Intents
    - Saludo
    - Adios
    - Problem_report
    - Request
- Entites
    - application
    - problem
    - request
    - Afirmacion

Aunque las `intents` y las `entities` ya están completadas, el diálogo no está completo. Solo tiene el nodo inicial, otros casos y Problem_report implementados, faltando el nodo Saludo, Adios y Request. Su tarea es implementar los tres nodos que faltan para que sea posible mantener un flujo de diálogo consistente, donde a partir de la identificación de la demanda del usuario se brinde la respuesta adecuada.

Al identificar la `intent` de Saludo, su asistente debe responder con un saludo.

Al identificar la `intent` de Adios, su asistente debe terminar la conversación con una despedida.

Al identificar la Solicitud de `intent`, su asistente debe identificar la solicitud (`Request intent`), el tipo de solicitud (`request entity`) y la aplicación correspondiente (`application entity`) . El asistente debe responder informando el tipo de solicitud y aplicación, junto con un número de ticket generado para esta solicitud. Adicionalmente el asistente debe preguntar si el usuario quiere acceso al reporte de la solicitud en el futuro (Si o No). Para este nodo es recomendable utilizar el nodo Problem_report como ejemplo.

Las `intents` ya están completadas, pero eso no significa que no puedas agregar o eliminar ejemplos, ya que estas modificaciones pueden mejorar la confianza en la identificación del modelo. No dudes en realizar los cambios que consideres necesarios siempre que el resultado sea el especificado anteriormente.

### **Solución:**

En el siguiente enlace se podrá interactuar en tiempo real con el asistente virtual,

[Asistente Virtual Alestra](https://web-chat.global.assistant.watson.cloud.ibm.com/preview.html?region=us-south&integrationID=963a2abc-bd2f-4e30-ade7-e1a533555bfd&serviceInstanceID=58205d42-dbd5-424f-bc9b-584ccb31b5fa) 

Se trabajo en el asistente los 3 nodos que le faltaban a la conversación, estos son:

- Saludo
- Solocitud
- Adios (despedida)

Nodo Saludo:

![https://res.cloudinary.com/xaiop/image/upload/v1597596158/desafio1-alestra/giphy_lwlqbm.gif](https://res.cloudinary.com/xaiop/image/upload/v1597596158/desafio1-alestra/giphy_lwlqbm.gif)

Nodo Solicitud:

Agregar información

![https://res.cloudinary.com/xaiop/image/upload/v1597596554/desafio1-alestra/giphy_yi4664.gif](https://res.cloudinary.com/xaiop/image/upload/v1597596554/desafio1-alestra/giphy_yi4664.gif)

Modificar información:

![https://res.cloudinary.com/xaiop/image/upload/v1597596691/desafio1-alestra/giphy_urakv4.gif](https://res.cloudinary.com/xaiop/image/upload/v1597596691/desafio1-alestra/giphy_urakv4.gif)

Eliminar información:

![https://res.cloudinary.com/xaiop/image/upload/v1597596798/desafio1-alestra/giphy_urrwuv.gif](https://res.cloudinary.com/xaiop/image/upload/v1597596798/desafio1-alestra/giphy_urrwuv.gif)

Nodo adiós (Despedida):

![https://res.cloudinary.com/xaiop/image/upload/v1597596435/desafio1-alestra/giphy_jj8evo.gif](https://res.cloudinary.com/xaiop/image/upload/v1597596435/desafio1-alestra/giphy_jj8evo.gif)

Flujo general :

![https://res.cloudinary.com/xaiop/image/upload/c_scale,w_200/v1597595864/desafio1-alestra/giphy_uo1hhv.gif](https://res.cloudinary.com/xaiop/image/upload/c_scale,w_200/v1597595864/desafio1-alestra/giphy_uo1hhv.gif)