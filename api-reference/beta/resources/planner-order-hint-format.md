---
title: Uso de sugerencias de orden en Planner
description: '`)'
ms.openlocfilehash: b7edbcc22a297fc30a98c337daed266b2e599c70
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083266"
---
# <a name="using-order-hints-in-planner"></a>Uso de sugerencias de orden en Planner

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Los objetos de Planner identifican sus criterios de ordenación por sugerencias de ordenación. Los valores de sugerencias de ordenación son cadenas. Los clientes pueden ordenar las cadenas basándose en el valor ordinal de su caracteres para identificar el orden de los elementos. Se comparan los caracteres desde el principio de la cadena hasta que se detecta una diferencia en los valores ordinales de caracteres o termina una cadena, en cuyo caso se colocará la cadena más corta antes que la más larga. Los valores pueden contener cualquier carácter entre ordinales 32 (espacio) y 126 (`~`)

Por ejemplo, un elemento con la sugerencia de ordenación `a` (valor ordinal 97) se colocaría antes que otro con la sugerencia de ordenación `z` (valor ordinal 122). Por ejemplo, un elemento con la sugerencia de ordenación `abc` (valores ordinales 97, 98 y 99) se colocaría antes que otro con la sugerencia de ordenación `abd` (valores ordinales 97, 98, 100). Un elemento con la sugerencia de ordenación `a` se colocaría antes que otro con la sugerencia de ordenación `ab` puesto que todos los caracteres existentes son los mismos, y `a` es más corta.

Se calculan los valores de todas las sugerencias de ordenación por el servicio. Para reordenar elementos, el cliente puede especificar la sugerencia de ordenación para el elemento que se ha movido entre dos elementos. Para ello, debe establecer la sugerencia de ordenación en el valor siguiente: `<previous order hint> <next order hint>!`, donde `<previous order hint>` debe sustituirse por la sugerencia de ordenación del elemento que precede a la nueva ubicación deseada y `<next order hint>` debe sustituirse por la sugerencia de ordenación del elemento que viene después de la nueva localización deseada. Hay un carácter de espacio entre estos valores de sugerencia de ordenación, y el valor completo se añade como sufijo con `!`. Si un elemento no está presente, debe utilizarse una cadena vacía en su lugar. Este valor también puede estar compuesto de cálculos previos y puede utilizarse en el cliente para ordenar elementos de forma exacta como el servicio que devuelve sugerencias de ordenación. Una vez que el cliente envía estos valores en una actualización, el servicio calculará un valor pequeño que ordene en la ubicación deseada.

> **Nota:** En los ejemplos siguientes, los valores de sugerencia de orden real rodeados en caracteres de comillas simples (`'`) para mayor claridad, sin embargo estos no forman parte de los datos y no se debe enviar al servicio.
 
Como ejemplo, considere la siguiente lista de sugerencias de ordenación ya ordenadas:

1. Elemento 1 (sugerencia de ordenación: `'5637'`)
2. Elemento 2 (sugerencia de ordenación: `'adhg'`)

Colocar un elemento 3 antes del elemento 1, después, colocar un elemento 4 entre los elementos 1 y 2 y, luego, colocar un elemento 5 después de un elemento 2 crearía las siguientes sugerencias de ordenación en el cliente. 

1. Elemento 3 (sugerencia de ordenación: `' 5637!'`)
2. Elemento 1 (sugerencia de ordenación: `'5637'`)
3. Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)
4. Elemento 2 (sugerencia de ordenación: `'adhg'`)
5. Elemento 5 (sugerencia de ordenación: `'adhg !'`)

A continuación, mover un elemento 1 al final de la lista generaría:

1. Elemento 3 (sugerencia de ordenación: `' 5637!'`)
2. Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)
3. Elemento 2 (sugerencia de ordenación: `'adhg'`)
4. Elemento 5 (sugerencia de ordenación: `'adhg !'`)
5. Elemento 1 (sugerencia de ordenación: `'adhg ! !'`) 

Finalmente, mover un elemento 5 entre los elementos 3 y 4 generaría:

1. Elemento 3 (sugerencia de ordenación: `' 5637!'`)
2. Elemento 5 (sugerencia de ordenación: `' 5637! 5637 adhg!!'`)
3. Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)
4. Elemento 2 (sugerencia de ordenación: `'adhg'`)
5. Elemento 1 (sugerencia de ordenación: `'adhg ! !'`)

Cuando estos cambios a los valores de sugerencia de orden se envían al servicio de las solicitudes de revisión, el servicio calcularán los valores adecuados que mantener el orden previsto por el cliente. El cliente puede obtener la if inmediato valores el `Prefer: return=representation` encabezado de preferencia se especifica en el `PATCH` las solicitudes. Los valores para el caso anterior pueden tener la apariencia siguiente (los valores reales pueden diferir). 

1. Elemento 3 (sugerencia de ordenación: `'432b'`) 
2. Elemento 5 (sugerencia de ordenación: `'6F"#'`)
3. Elemento 4 (sugerencia de ordenación: `'7A$6'`)
4. Elemento 2 (sugerencia de ordenación: `'adhg'`)
5. Elemento 1 (sugerencia de ordenación: `'de5%'`)

Se pueden especificar las sugerencias de ordenación para crear el primer elemento en la lista como ` !`, puesto que en este caso no existe ni un elemento anterior ni uno posterior. Sin embargo, esto no es necesario dado que el servicio generará automáticamente todos los valores de sugerencia de ordenación de elementos si no se especifican durante la creación del elemento. El ejemplo siguiente muestra que las sugerencias de ordenación se deben utilizar al colocar elementos en una lista previamente vacía. Agregue el primer elemento:

1. Elemento 1 (sugerencia de ordenación: `' !'`)

Agregue el segundo elemento en la parte superior:

1. Elemento 2 (sugerencia de ordenación: `'  !!'`)
2. Elemento 1 (sugerencia de ordenación: `' !'`)

Agregar el tercer elemento en la parte inferior:

1. Elemento 2 (sugerencia de ordenación: `'  !!'`)
2. Elemento 1 (sugerencia de ordenación: `' !'`)
3. Elemento 3 (sugerencia de ordenación: `' ! !'`)







