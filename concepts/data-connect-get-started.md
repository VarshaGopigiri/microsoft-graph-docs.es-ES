---
title: Introducción a la conexión a los datos de Microsoft Graph (versión preliminar)
description: 'Para poder usar la conexión a los datos de Microsoft Graph, un administrador de Office 365 debe realizar dos acciones; ambas habilitan al administrador a controlar el movimiento de datos a través de una administración con privilegios de acceso (PAM). '
author: ajacks-msft
ms.openlocfilehash: 1cd8d5734b0fd8b48df8a49fe0a833583c21148d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27312085"
---
# <a name="get-started-with-microsoft-graph-data-connect-preview"></a>Introducción a la conexión a los datos de Microsoft Graph (versión preliminar)

Para poder usar la conexión a los datos de Microsoft Graph, un administrador de Office 365 debe realizar dos acciones; ambas habilitan al administrador a controlar el movimiento de datos a través de una administración con privilegios de acceso (PAM). 

1. Conceder permisos para participar en la conexión a los datos de Microsoft Graph a través del Portal de administración de Microsoft 365, en la página**Servicios y complementos**. Esto permitirá las solicitudes de movimiento de datos a Microsoft Azure (esto es, mantener pleno control sobre los datos, pero permitir que los recursos de Azure accedan a ellos). No se transferirán datos a menos que se conceda la aprobación de una canalización específica más adelante.
2. Establecer un grupo aprobador dentro de la suscripción de Office 365. Asegúrese de que el grupo aprobador no esté vacío. Solo los usuarios del grupo pueden aprobar solicitudes de movimiento de datos.

Para obtener instrucciones detalladas, consulte el [módulo de formación de conexión a los datos de Microsoft Graph](https://github.com/microsoftgraph/msgraph-training-dataconnect/blob/master/Lab.md).

## <a name="next-steps"></a>Pasos siguientes

¡Enhorabuena! Ya puede empezar a crear aplicaciones inteligentes con herramientas de Azure. Para una aplicación de ejemplo y documentación adicional, consulte el [repositorio de GitHub de conexión a los datos de Microsoft Graph](https://github.com/OfficeDev/MS-Graph-Data-Connect/wiki). 
