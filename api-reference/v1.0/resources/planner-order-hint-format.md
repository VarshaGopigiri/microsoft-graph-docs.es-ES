---
title: Uso de sugerencias de orden en Planner
description: '`)'
author: TarkanSevilmis
localization_priority: Normal
ms.prod: planner
ms.openlocfilehash: 03b2ec61d267e0c04c6ba6360bb28bb04bffda54
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923484"
---
# <a name="using-order-hints-in-planner"></a>Uso de sugerencias de orden en Planner

Los objetos de Planner identifican sus criterios de ordenación por sugerencias de ordenación. Los valores de sugerencias de ordenación son cadenas. Los clientes pueden ordenar las cadenas basándose en el valor ordinal de su caracteres para identificar el orden de los elementos. Se comparan los caracteres desde el principio de la cadena hasta que se detecta una diferencia en los valores ordinales de caracteres o termina una cadena, en cuyo caso se colocará la cadena más corta antes que la más larga. Los valores pueden contener cualquier carácter entre ordinales 32 (espacio) y 126 (`~`)

Por ejemplo, un elemento con la sugerencia de ordenación `a` (valor ordinal 97) se colocaría antes que otro con la sugerencia de ordenación `z` (valor ordinal 122). Por ejemplo, un elemento con la sugerencia de ordenación `abc` (valores ordinales 97, 98 y 99) se colocaría antes que otro con la sugerencia de ordenación `abd` (valores ordinales 97, 98, 100). Un elemento con la sugerencia de ordenación `a` se colocaría antes que otro con la sugerencia de ordenación `ab` puesto que todos los caracteres existentes son los mismos, y `a` es más corta.

Se calculan los valores de todas las sugerencias de ordenación por el servicio. Para reordenar elementos, el cliente puede especificar la sugerencia de ordenación para el elemento que se ha movido entre dos elementos. Para ello, debe establecer la sugerencia de ordenación en el valor siguiente: `<previous order hint> <next order hint>!`, donde `<previous order hint>` debe sustituirse por la sugerencia de ordenación del elemento que precede a la nueva ubicación deseada y `<next order hint>` debe sustituirse por la sugerencia de ordenación del elemento que viene después de la nueva localización deseada. Hay un carácter de espacio entre estos valores de sugerencia de ordenación, y el valor completo se añade como sufijo con `!`. Si un elemento no está presente, debe utilizarse una cadena vacía en su lugar. Este valor también puede estar compuesto de cálculos previos y puede utilizarse en el cliente para ordenar elementos de forma exacta como el servicio que devuelve sugerencias de ordenación. Una vez que el cliente envía estos valores en una actualización, el servicio calculará un valor pequeño que ordene en la ubicación deseada.

**Tenga en cuenta** que, en los ejemplos siguientes, los valores actuales de sugerencia de ordenación se sitúan entre comillas simples (`'`) para mayor claridad, sin embargo estas no forman parte de los datos y no se deben enviar al servicio.
 
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

Una vez que estos cambios en los valores de sugerencia de ordenación se envíen al servicio mediante solicitudes de revisión, el servicio calculará los valores adecuados que mantengan el orden pretendido por el cliente. El cliente puede obtener de inmediato los valores si se especifica la preferencia `return=representation` en las solicitudes `PATCH`. Los valores para el caso anterior pueden tener la apariencia siguiente (los valores reales pueden diferir). 

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







