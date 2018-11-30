---
title: Identificadores de tareas
description: 'Identificadores de objetos en las tareas son valores de cadena generados por el servicio. . Los valores son 28 caracteres de longitud y distinguen mayúsculas de minúsculas. Cuando se pasan como en, el servicio realizará una validación de formato básico del identificador, si el error de validación de formato, los llamadores recibirá una respuesta de error de solicitud incorrecta (400), que indica que este problema. Recibir este error indica un error en la aplicación que llama, tales como:'
ms.openlocfilehash: d57ca282de87c2bce42b37d0be6d08dbe128c522
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090799"
---
# <a name="identifiers-in-tasks"></a>Identificadores de tareas

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Identificadores de objetos en las tareas son valores de cadena generados por el servicio. . Los valores son 28 caracteres de longitud y distinguen mayúsculas de minúsculas. Cuando se pasan como en, el servicio realizará una validación de formato básico del identificador, si el error de validación de formato, los llamadores recibirá una respuesta de error de solicitud incorrecta (400), que indica que este problema. Recibir este error indica un error en la aplicación que llama, tales como:

- La aplicación de llamada ha procesado el identificador como una cadena que no distingue mayúsculas de minúsculas. Los identificadores de tareas distinguen mayúsculas de minúsculas.
- La aplicación de llamada ha truncado el identificador. Los identificadores de tareas tienen una longitud de 28 caracteres.
- La aplicación de llamada ha intentado generar un valor de identificador para un objeto en las tareas. No se aceptan los identificadores generados por el cliente. Todos los identificadores se generan con el servicio tras la creación de objetos.

Esta validación **no representa ninguna característica de seguridad**. Solo está pensada para informar a las aplicaciones de los problemas comunes relacionados con el identificador durante el desarrollo de la aplicación, que en caso contrario son difíciles de identificar.