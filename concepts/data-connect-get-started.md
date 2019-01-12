---
title: Introducción a la conexión a los datos de Microsoft Graph (versión preliminar)
description: 'Para poder usar la conexión a los datos de Microsoft Graph, un administrador de Office 365 debe realizar dos acciones; ambas habilitan al administrador a controlar el movimiento de datos a través de una administración con privilegios de acceso (PAM). '
author: ajacks-msft
localization_priority: Priority
ms.prod: data-connect
ms.openlocfilehash: f7426147908a2ded298bee065c05afffc182cd4b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914447"
---
# <a name="get-started-with-microsoft-graph-data-connect-preview"></a>Introducción a la conexión a los datos de Microsoft Graph (versión preliminar)

Para poder usar la conexión a los datos de Microsoft Graph, un administrador de Office 365 debe realizar dos acciones; ambas habilitan al administrador a controlar el movimiento de datos a través de una administración con privilegios de acceso (PAM). 

1. Conceder permisos para participar en la conexión a los datos de Microsoft Graph a través del Portal de administración de Microsoft 365, en la página**Servicios y complementos**. Esto permitirá las solicitudes de movimiento de datos a Microsoft Azure (esto es, mantener pleno control sobre los datos, pero permitir que los recursos de Azure accedan a ellos). No se transferirán datos a menos que se conceda la aprobación de una canalización específica más adelante.
2. Establecer un grupo aprobador dentro de la suscripción de Office 365. Asegúrese de que el grupo aprobador no esté vacío. Solo los usuarios del grupo pueden aprobar solicitudes de movimiento de datos.

Para obtener instrucciones detalladas, consulte el [módulo de formación de conexión a los datos de Microsoft Graph](https://github.com/microsoftgraph/msgraph-training-dataconnect/blob/master/Lab.md).

## <a name="next-steps"></a>Pasos siguientes

¡Enhorabuena! Ya puede empezar a crear aplicaciones inteligentes con herramientas de Azure. Para una aplicación de ejemplo y documentación adicional, consulte el [repositorio de GitHub de conexión a los datos de Microsoft Graph](https://github.com/OfficeDev/MS-Graph-Data-Connect/wiki). 
