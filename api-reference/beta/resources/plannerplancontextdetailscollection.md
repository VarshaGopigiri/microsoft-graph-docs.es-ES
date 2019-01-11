---
title: tipo de recurso plannerPlanContextDetailsCollection
description: " el valor es el objeto plannerPlanContextDetails."
author: TarkanSevilmis
localization_priority: Normal
ms.openlocfilehash: 0020ff8e8fd0d2e8dfd783e282e2bd648c16ec6a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828241"
---
# <a name="plannerplancontextdetailscollection-resource-type"></a>tipo de recurso plannerPlanContextDetailsCollection

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.


El recurso **plannerPlanContextDetailsCollection** representa la colección de contextos externos al que está vinculado un plan. Este recurso es un tipo abierto y forma parte del objeto [plannerPlanDetails](plannerplandetails.md) . El nombre de la propiedad en el par de valor de la propiedad es un identificador específicas de la aplicación del contexto. el valor es el objeto [plannerPlanContextDetails](plannerplancontextdetails.md) .


## <a name="properties"></a>Propiedades
Las propiedades de un tipo abierto pueden definirse por el cliente. En este caso, el cliente debe utilizar un identificador distintivo que representa el contexto externo como el nombre de la propiedad. Los valores de propiedad deben ser [plannerPlanContextDetails](plannerplancontextdetails.md) objetos. En función de OData, nombres de propiedad de tipos abiertos no pueden contener los siguientes caracteres: `.`, `:`, `@`, `%`. Estos caracteres que deba estar codificado con el formato de codificación de dirección URL. Para quitar un elemento en la lista de favoritos, el valor debe quitarse de la colección [plannerPlanContextCollection](plannerplancontextcollection.md) en su lugar, que quitará automáticamente la entrada en este objeto.


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanContextDetailsCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
