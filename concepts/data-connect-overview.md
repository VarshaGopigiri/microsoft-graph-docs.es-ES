---
title: Conexión de datos de Microsoft Graph (versión preliminar)
description: 'La conexión de datos de Microsoft Graph muestra los datos de Office 365 y los recursos de Microsoft Azure a través de una canalización de datos principales. Puede usar la conexión de datos de Microsoft Graph para desarrollar aplicaciones inteligentes que accedan a datos importantes mediante el uso de las mejores herramientas de desarrollo provistas por Microsoft, todo esto dentro de la nube segura de Microsoft. Mejorar la productividad es un desafío de todas las empresas. Esto significa que crear productos que incrementen la productividad de los trabajadores del conocimiento representa una enorme oportunidad. '
author: ajacks-msft
ms.openlocfilehash: 283ad9044eb5ae5bc53bb4b72e4d6d1f2434cfee
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315270"
---
# <a name="microsoft-graph-data-connect-preview"></a>Conexión de datos de Microsoft Graph (versión preliminar)

La conexión de datos de Microsoft Graph muestra los datos de Office 365 y los recursos de Microsoft Azure a través de una canalización de datos principales. Puede usar la conexión de datos de Microsoft Graph para desarrollar aplicaciones inteligentes que accedan a datos importantes mediante el uso de las mejores herramientas de desarrollo provistas por Microsoft, todo esto dentro de la nube segura de Microsoft. Mejorar la productividad es un desafío de todas las empresas. Esto significa que crear productos que incrementen la productividad de los trabajadores del conocimiento representa una enorme oportunidad. 

Puede aprovechar la conexión de datos de Microsoft Graph si es:

- Un ISV que desarrolla aplicaciones inteligentes para todos los clientes de Office 365.
- Un desarrollador empresarial que crea aplicaciones inteligentes para todos los usuarios en una organización con acceso a los datos de Office 365.

## <a name="develop-a-pipeline-with-office-365-data"></a>Desarrollar una canalización con datos de Office 365
Puede usar la conexión de datos de Microsoft Graph para crear nuevos tipos de aplicaciones basadas en los datos de Office 365, al mismo tiempo que aprovecha las mejores herramientas de Microsoft Azure. Puede utilizar Azure Data Factory para mover los datos de Office 365 a las tiendas populares de Azure: Azure Data Lake Gen 1 o Gen 2 (versión preliminar) o Azure Blob Storage. Luego, puede procesar los datos (mediante Azure Data Lake Analytics, por ejemplo) o moverlos a otra tienda, como Azure SQL Database. A continuación, puede usar los datos para proveer el escenario del usuario final de la aplicación.

Antes de que la canalización de Azure Data Factory pueda mover datos desde Office 365, se envía un consentimiento de solicitud de datos a los aprobadores de datos designados por el administrador de Office 365 del cliente. Una vez que los aprobadores de datos aceptan la solicitud, comienza el movimiento de datos.

## <a name="publish-your-app-as-an-azure-managed-application"></a>Publicar la aplicación como una Azure Managed Application
Después de desarrollar una aplicación que usa la conexión de datos de Microsoft Graph, puede hacer que la aplicación esté disponible para otros usuarios (ya sea dentro o fuera de su organización). La conexión de datos de Microsoft Graph usa [Azure Managed Applications](https://docs.microsoft.com/es-ES/azure/managed-applications/overview) lo que permite que estas aplicaciones estén disponibles para otros usuarios en Microsoft Azure Marketplace. Azure Managed Applications permite a los ISV y a los desarrolladores empresariales ofrecer soluciones llave en mano a sus clientes. Los clientes implementan estas aplicaciones administradas en sus suscripciones, mientras que los proveedores (ISV y desarrolladores empresariales) se encargan de su administración y soporte. Además, los proveedores pueden aplicar [directivas](https://docs.microsoft.com/es-ES/azure/managed-applications/overview#azure-policy) a sus aplicaciones, como por ejemplo, el cifrado en reposo, para ofrecerles a sus clientes la tranquilidad de saber que sus datos se manipulan de forma segura. Las aplicaciones pueden ser publicadas en [Azure Marketplace](https://docs.microsoft.com/es-ES/azure/managed-applications/publish-marketplace-app) o en el [catálogo de servicios de Azure](https://docs.microsoft.com/es-ES/azure/managed-applications/publish-service-catalog-app).

Los clientes que instalen la aplicación podrán ver las condiciones del servicio, los datos que son necesarios, el precio del SKU de cada aplicación y el costo aproximado de consumo de recursos. Cuando el comprador especifica las propiedades, se aprovisionan los recursos. Esto incluye la canalización de Data Factory que comienza la extracción de datos. La aplicación debe contar con un archivo Léame que explique cuánto tiempo lleva completar la instalación, cómo usar la aplicación y cómo obtener soporte técnico.

## <a name="next-steps"></a>Pasos siguientes 
Para empezar a desarrollar aplicaciones con conexión de datos de Microsoft Graph, consulte [Introducción a la conexión de datos de Microsoft Graph](data-connect-concept-overview.md).
