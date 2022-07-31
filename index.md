12 reglas de Codd

Las 12 reglas de Codd son un sistema de 13 reglas —numeradas del 0 al 12— propuestas por el creador del modelo relacional de bases de datos, Edgar F. Codd, para definir los requerimientos que un sistema de administración de base de datos ha de cumplir para poder ser considerado relacional1 como lo son, por ejemplo, las bases de datos relacionales.

Reglas:
Regla 0: Regla fundamental. Todo sistema que se defina como sistema de gestión de base de datos relacional, o se anuncie como tal, ha de poder gestionar las bases de datos exclusivamente con sus capacidades relacionales.

Regla 1: Regla de la información. Toda la información en una base de datos relacional se representa de forma explícita en el nivel lógico de una manera exactamente: con valores en tablas.

Regla 2: Regla del acceso garantizado. Se garantiza que todos y cada uno de los datos (valor atómico) de una base de datos relacional son accesibles lógicamente mediante una combinación de nombre de tabla, valor de clave primaria y nombre de columna.

Todos los datos deben ser accesibles sin ambigüedad. Esta regla es esencialmente una nueva exposición del requisito fundamental para las claves primarias. Dice que cada valor escalar individual en la base de datos debe ser lógicamente direccionable especificando el nombre de la tabla, la columna que lo contiene y la clave primaria.

Regla 3: Regla del tratamiento sistemático de valores nulos. Los sistemas de gestión de base de datos plenamente relacionales admiten los valores nulos (distintos de la cadena vacía, los blancos, los ceros o cualquier otro número) para representar la información desconocida y la inaplicable de manera sistemática e independiente del tipo de dato .

Regla 4: Catálogo dinámico en línea basado en el modelo relacional. La descripción de la base de datos se representa a nivel lógico igual que los datos comunes, de modo que los usuarios autorizados pueden utilizar el mismo lenguaje relacional en su consulta que el que aplican a los datos comunes.

El sistema debe soportar un catálogo en línea, el catálogo relacional, que da acceso a la estructura de la base de datos y que debe ser accesible a los usuarios autorizados.

Regla 5: Regla del sublenguaje de datos completo. Un sistema relacional debe permitir varios lenguajes y varios modos de uso terminal (como rellenar formularios, por ejemplo). Sin embargo, debe haber al menos un lenguaje cuyas declaraciones se puedan expresar, mediante una sintaxis bien definida, como cadenas de caracteres y que respalde de forma integral los siguientes aspectos:

Definición de datos
Definición de vistas
Manipulación de datos (interactiva y por programa)
Restricciones de integridad
Límites de transacción (begin, commit y rollback).
Regla 6: Regla de actualización de vistas. Todas las vistas que son teóricamente actualizables son también actualizables por el sistema.

Regla 7: Inserción, actualización y borrado de alto nivel. La capacidad de gestionar una relación base o una relación derivada como un solo operando no solo se aplica no a la recuperación de los datos, sino también a la inserción, actualización y eliminación de datos.

El sistema debe permitir la manipulación de alto nivel en los datos, es decir, sobre conjuntos de tuplas. Esto significa que los datos no solo se pueden recuperar de una base de datos relacional a partir de filas múltiples y/o de tablas múltiples, sino que también pueden realizarse inserciones, actualizaciones y borrados sobre varias tuplas y/o tablas al mismo tiempo y no solo sobre registros individuales.

Regla 8: Independencia física de los datos. Los programas de aplicación y actividades terminales permanecen inalterados a nivel lógico cuando se realizan cambios en las representaciones de almacenamiento o en los métodos de acceso.

Regla 9: Independencia lógica de los datos. Los programas de aplicación y actividades terminales permanecen inalterados a nivel lógico cuando se realizan cambios en las tablas base que preservan la información.

La independencia de datos lógica es más difícil de lograr que la independencia física de datos.

Regla 10: Independencia de la integridad. Las restricciones de integridad específicas para una determinada base de datos relacional se deben poder definir en el sublenguaje de datos relacional y almacenar en el catálogo, no en los programas de aplicación.

Las restricciones de integridad se deben especificar por separado de los programas de aplicación y almacenarse en la base de datos. Debe ser posible cambiar esas restricciones sin afectar innecesariamente a las aplicaciones existentes.

Regla 11: Independencia de la distribución. El usuario final no ha de ver que los datos están distribuidos en varias ubicaciones. Los usuarios deben tener siempre la impresión de que los datos se encuentran en un solo lugar.

La distribución de porciones de base de datos en distintas localizaciones debe ser transparente para los usuarios de la base de datos. Los usos existentes deben continuar funcionando con éxito:

cuando una versión distribuida del SGBD se carga por primera vez
cuando los datos existentes se redistribuyen en el sistema.
Regla 12: La regla de la no subversión. Si un sistema relacional tiene un lenguaje de bajo nivel (un registro cada vez), ese nivel bajo no puede utilizarse para subvertir o eludir las reglas y restricciones de integridad expresadas en el lenguaje relacional de alto nivel (varios registros cada vez).

Si el sistema proporciona una interfaz de bajo nivel de registro, aparte de una interfaz relacional, esa interfaz de bajo nivel no debe permitir su utilización para subvertir el sistema. Por ejemplo para sortear las reglas de seguridad relacional o las restricciones de integridad. Esto es debido a que a algunos sistemas no relacionales previamente existentes se les añadió una interfaz relacional pero, al mantener la interfaz nativa, seguía existiendo la posibilidad de trabajar no relacionalmente.
