---
title: Obtener eventos de Outlook en un calendario compartido o delegado
description: En Outlook, los clientes pueden compartir un calendario con otros usuarios y permitirles ver o modificar los eventos de ese calendario. Los clientes también pueden nominar un delegado que actúe en su nombre, para recibir o responder a convocatorias de reunión y crear o cambiar elementos en el calendario.
ms.openlocfilehash: e05352e164b127adca1305dded5cbb00840eed52
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092841"
---
# <a name="get-outlook-events-in-a-shared-or-delegated-calendar"></a>Obtener eventos de Outlook en un calendario compartido o delegado

En Outlook, los clientes pueden compartir un calendario con otros usuarios y permitirles ver o modificar los eventos de ese calendario. Los clientes también pueden nominar un delegado que actúe en su nombre, para recibir o responder a convocatorias de reunión y crear o cambiar elementos en el calendario.


Mediante programación, Microsoft Graph admite obtener eventos en calendarios que se han compartido con otros usuarios, así como obtener calendarios compartidos. El soporte también se aplica a los calendarios que se han delegado.

Por ejemplo, Garth ha compartido con John su calendario predeterminado y le ha concedido el acceso de lectura. Si John ha iniciado sesión en la aplicación y ha proporcionado permisos delegados (Calendars.Read.Shared o Calendars.ReadWrite.Shared), la aplicación podrá acceder al calendario predeterminado de Garth y a los eventos en dicho calendario, tal y como se describe a continuación.

## <a name="get-an-event-in-the-shared-calendar"></a>Obtener un evento en el calendario compartido

Puede obtener un evento específico en el calendario compartido predeterminado de Garth:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar/events/{id}
```

Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [event](/graph/api/resources/event?view=graph-rest-1.0) identificada por `{id}` desde el calendario predeterminado de Garth.

## <a name="get-all-the-events-in-the-shared-calendar"></a>Obtener todos los eventos del calendario compartido

Obtenga todos los eventos en el calendario predeterminado que Garth ha compartido con John:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar/events
```

Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias [event](/graph/api/resources/event?view=graph-rest-1.0) en el calendario predeterminado de Garth.

## <a name="get-the-shared-calendar"></a>Obtener el calendario compartido

Obtenga el calendario predeterminado que Garth ha compartido con John:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar
```

Cuando se complete correctamente, verá HTTP 200 OK y la instancia [calendar](/graph/api/resources/calendar?view=graph-rest-1.0) que representa la carpeta predeterminada de Garth.

Se aplican las mismas capacidades de GET si Garth ha delegado a John más acceso a su calendario predeterminado o si ha delegado a John todo su buzón de correo.

Si Garth no ha compartido su calendario predeterminado con John, ni ha delegado su buzón de correo a John, especificar el identificador de usuario de Garth o el nombre principal de usuario en esas operaciones GET devolverá un error. 


## <a name="next-steps"></a>Pasos siguientes

Obtenga más información sobre:

- [¿Por qué debería realizar la integración con el calendario de Outlook?](outlook-calendar-concept-overview.md)
- La [API de calendario](/graph/api/resources/calendar?view=graph-rest-1.0) en la versión 1.0 de Microsoft Graph.