---
title: El flujo de datos de la API de seguridad de Microsoft Graph
description: La API de seguridad de Microsoft Graph federa solicitudes a todos los proveedores en el ecosistema de seguridad de Microsoft Graph. Esto se basa en el consentimiento del proveedor de seguridad proporcionado por la aplicación, como se muestra en el siguiente diagrama. El flujo de trabajo de consentimiento solo se aplica a los proveedores que no son de Microsoft.
ms.openlocfilehash: 1e8b074e3cf4589ca67364ed7e225a62f40300fd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092865"
---
# <a name="microsoft-graph-security-api-data-flow"></a>El flujo de datos de la API de seguridad de Microsoft Graph

La API de seguridad de Microsoft Graph federa solicitudes a todos los proveedores en el ecosistema de seguridad de Microsoft Graph. Esto se basa en el consentimiento del proveedor de seguridad proporcionado por la aplicación, como se muestra en el siguiente diagrama. El flujo de trabajo de consentimiento solo se aplica a los proveedores que no son de Microsoft.

![security_dataflow_1.png](./images/security-dataflow-1.png)

A continuación se describe el flujo:

1. El usuario de la aplicación inicia sesión en la aplicación del proveedor para ver el formulario de consentimiento. La experiencia de este formulario de consentimiento o su interfaz de usuario son propiedad de proveedor y se aplican a los proveedores que no son de Microsoft solo para obtener un consentimiento explícito de sus clientes para enviar solicitudes a la API de seguridad de Microsoft Graph.
2. El consentimiento del cliente se almacena en el lado del proveedor.
3. El servicio de consentimiento del proveedor llama a la API de seguridad de Microsoft Graph para informar sobre la aprobación del consentimiento del cliente correspondiente.
4. La aplicación envía una solicitud a la API de seguridad de Microsoft Graph.
5. La API de seguridad de Microsoft Graph comprueba la información del consentimiento para este cliente asignado a varios proveedores.
6. La API de seguridad de Microsoft Graph llama a todos los proveedores a los que el cliente ha dado un consentimiento explícito mediante el consentimiento del proveedor.
7. Todos los proveedores con el consentimiento de ese cliente devuelven la respuesta.
8. La respuesta del conjunto de resultados se devuelve a la aplicación.
9. Si el cliente no ha dado el consentimiento a ningún proveedor, la respuesta no incluirá los resultados de dichos proveedores.
