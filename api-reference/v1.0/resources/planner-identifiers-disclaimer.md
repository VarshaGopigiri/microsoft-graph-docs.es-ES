---
title: Identificadores de Planner
description: 'Identificadores de objetos en Organizador son valores de cadena generados por el servicio. Los valores son 28 caracteres de longitud y distinguen mayúsculas de minúsculas. Cuando se pasan como en, el servicio realizará una validación de formato básico del identificador, si el error de validación de formato, los llamadores recibirá una respuesta de error de solicitud incorrecta (400), que indica que este problema. Recibir este error indica un error en la aplicación que llama, tales como:'
ms.openlocfilehash: a4b2eed7dafbd289da877ed64a74093cbf64781d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031913"
---
# <a name="identifiers-in-planner"></a>Identificadores de Planner

Identificadores de objetos en Organizador son valores de cadena generados por el servicio. Los valores son 28 caracteres de longitud y distinguen mayúsculas de minúsculas. Cuando se pasan como en, el servicio realizará una validación de formato básico del identificador, si el error de validación de formato, los llamadores recibirá una respuesta de error de solicitud incorrecta (400), que indica que este problema. Recibir este error indica un error en la aplicación que llama, tales como:

- La aplicación de llamada ha procesado el identificador como una cadena que no distingue mayúsculas de minúsculas. Los identificadores de tareas distinguen mayúsculas de minúsculas.
- La aplicación de llamada ha truncado el identificador. Los identificadores de tareas tienen una longitud de 28 caracteres.
- La aplicación de llamada ha intentado generar un valor de identificador para un objeto en las tareas. No se aceptan los identificadores generados por el cliente. Todos los identificadores se generan con el servicio tras la creación de objetos.

Esta validación **no representa ninguna característica de seguridad**. Solo está pensada para informar a las aplicaciones de los problemas comunes relacionados con el identificador durante el desarrollo de la aplicación, que en caso contrario son difíciles de identificar.