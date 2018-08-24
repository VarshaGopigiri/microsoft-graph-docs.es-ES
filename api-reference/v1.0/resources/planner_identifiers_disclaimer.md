# <a name="identifiers-in-planner"></a>Identificadores en Planner

Los identificadores de objetos en Planner son valores de cadena generados por el servicio. Los valores son 28 caracteres de longitud y distinguen mayúsculas de minúsculas. Si se pasa tal cual, el servicio efectuará una validación de formato simple del identificador. Si se produce un error en la validación del formato, los llamadores recibirán una respuesta de error Bad Request (400) indicando este problema. Este error indica un error en la aplicación de llamada como, por ejemplo:

- La aplicación de llamada ha procesado el identificador como una cadena que no distingue mayúsculas de minúsculas. Los identificadores de tareas distinguen mayúsculas de minúsculas.
- La aplicación de llamada ha truncado el identificador. Los identificadores de tareas tienen una longitud de 28 caracteres.
- La aplicación de llamada ha intentado generar un valor de identificador para un objeto en las tareas. No se aceptan los identificadores generados por el cliente. Todos los identificadores se generan con el servicio tras la creación de objetos.

Esta validación **no representa ninguna característica de seguridad**. Solo está pensada para informar a las aplicaciones de los problemas comunes relacionados con el identificador durante el desarrollo de la aplicación, que en caso contrario son difíciles de identificar.