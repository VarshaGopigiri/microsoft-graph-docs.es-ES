---
title: Introducción a la conexión a los datos de Microsoft Graph (versión preliminar)
description: 'Microsoft Graph contiene datos enriquecidos sobre los trabajadores y su lugar de trabajo, incluida información sobre cómo trabajan y cómo se comunican, colaboran o gestionan su tiempo. La conexión a los datos de Microsoft Graph transfiere estos datos a Microsoft Azure, proporcionándote así acceso a las mejores herramientas de desarrollo y hospedaje para trabajar dichos datos. Esto permite a los clientes beneficiarse de aplicaciones innovadoras o específicas del sector que aumentan la productividad, pero sin dejar de mantener pleno control sobre sus datos de Microsoft Graph. Microsoft ofrece lo que desea cualquier cliente: el control más seguro.'
ms.openlocfilehash: cce6046c9ed9b57171e998b1cb17c4e92fa0fcb5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092854"
---
# <a name="overview-of-microsoft-graph-data-connect-preview"></a>Introducción a la conexión a los datos de Microsoft Graph (versión preliminar)
Microsoft Graph contiene datos enriquecidos sobre los trabajadores y su lugar de trabajo, incluida información sobre cómo trabajan y cómo se comunican, colaboran o gestionan su tiempo. La conexión a los datos de Microsoft Graph transfiere estos datos a Microsoft Azure, proporcionándote así acceso a las mejores herramientas de desarrollo y hospedaje para trabajar dichos datos. Esto permite a los clientes beneficiarse de aplicaciones innovadoras o específicas del sector que aumentan la productividad, pero sin dejar de mantener pleno control sobre sus datos de Microsoft Graph. Microsoft ofrece lo que desea cualquier cliente: el control más seguro.

## <a name="why-use-microsoft-graph-data-connect"></a>Por qué usar la conexión a los datos de Microsoft Graph
Los administradores de Office 365 deben tener en cuenta los desafíos que conlleva mover y administrar grandes cantidades de datos de la organización. La conexión a los datos de Microsoft Graph está diseñada para ofrecer a los administradores nuevos controles sobre los datos. Puede usar esos datos para desarrollar aplicaciones que creen recomendaciones basadas en datos. 

### <a name="enable-granular-consent"></a>Habilitar el consentimiento pormenorizado

En el modelo de permisos de Microsoft Graph, un administrador o usuario solo puede permitir o denegar la solicitud de una aplicación para acceder a conjuntos de entidades predefinidos específicos. Por ejemplo, una solicitud de Mail.Read incluye el acceso de lectura a un conjunto de entidades fijas que admiten correo de Outlook, como por ejemplo, instancias completas de [mensaje](/graph/api/resources/message?view=graph-rest-1.0) con todas sus propiedades. En cambio, la conexión a los datos de Microsoft Graph permite un consentimiento más pormenorizado y deja que las aplicaciones soliciten acceso a las propiedades específicas de una entidad o que filtren los datos de dichas propiedades. Los administradores deben expresar su aprobación de manera explícita para que se conceda el acceso a los datos de Microsoft Graph. La solicitud debe especificar el nivel de acceso solicitado y describir la aplicación de directivas de datos, el motivo de la solicitud y el esquema de los datos solicitados. Como resultado, las aplicaciones pueden utilizar únicamente los datos que sean esenciales para sus funciones, por lo que se excluye el contenido no relacionado. Por ejemplo, una aplicación puede utilizar los encabezados de correo electrónico, pero no los datos adjuntos y el contenido del cuerpo. 

### <a name="provide-data-governance"></a>Administrar el gobierno de datos
Microsoft facilita una comunicación completa y bien conectada entre Microsoft Graph y Azure en relación con el estado de los datos de clientes. Al crear aplicaciones con la conexión a los datos de Microsoft Graph, puede especificar un conjunto de directivas detalladas que piensa cumplir. Después, los administradores de Office 365 pueden revisarlas y dar su consentimiento. Este procedimiento reduce la sobrecarga de administración de cumplimiento. Cuando se da el consentimiento, Microsoft supervisa el cumplimiento de las directivas por parte de la aplicación. Si una aplicación infringe (o intenta infringir) una directiva establecida por la organización, Microsoft cesa el flujo de datos a esa aplicación. 

### <a name="get-access-to-data-at-scale"></a>Obtener acceso a datos a escala
Las aplicaciones enriquecidas requieren acceso a grandes cantidades de datos, a menudo de muchos usuarios de su organización al mismo tiempo. Con el modelo de datos transaccional tradicional, deberá crear una infraestructura compleja y realizar miles de llamadas a la API para organizar la entrega de los datos. La conexión a los datos de Microsoft Graph usa las características avanzadas de Azure Data Factory para entregar datos de Office 365 desde la organización a la aplicación, de modo reiterativo y en unos sencillos pasos.

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para este servicio?

[Configure](data-connect-get-started.md) la conexión a los datos de Microsoft Graph y vea [Usar el análisis de Azure y los datos de Office 365 para crear aplicaciones inteligentes](https://github.com/OfficeDev/MS-Graph-Data-Connect/wiki).


## <a name="next-steps"></a>Pasos siguientes
Para empezar, vea [Introducción a la conexión a los datos con Microsoft Graph](data-connect-get-started.md).
