---
title: Tipo de recurso plannerExternalReferences
description: El recurso **plannerExternalReferences** representa la colección de referencias de una tarea. Este es un tipo abierto. Forma parte del objeto task details. El valor del par propiedad-valor es el objeto externalReference.
localization_priority: Normal
ms.openlocfilehash: 7f32c0d7acc54f4bd96fd3b34478f80c882d55da
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888791"
---
# <a name="plannerexternalreferences-resource-type"></a><span data-ttu-id="ec56a-106">Tipo de recurso plannerExternalReferences</span><span class="sxs-lookup"><span data-stu-id="ec56a-106">plannerExternalReferences resource type</span></span>

> <span data-ttu-id="ec56a-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec56a-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec56a-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec56a-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ec56a-p103">El recurso **plannerExternalReferences** representa la colección de referencias de una tarea. Este es un tipo abierto. Forma parte del objeto [task details](plannertaskdetails.md). El valor del par propiedad-valor es el objeto [externalReference](plannerexternalreference.md).</span><span class="sxs-lookup"><span data-stu-id="ec56a-p103">The **plannerExternalReferences** resource represents the collection of references on a task. This is an Open Type. It is part of the [task details](plannertaskdetails.md) object. The value in the property-value pair is the [externalReference](plannerexternalreference.md) object.</span></span>


## <a name="properties"></a><span data-ttu-id="ec56a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec56a-113">Properties</span></span>
<span data-ttu-id="ec56a-p104">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar **direcciones URL válidas** a partir de protocolos **HTTP/HTTPS** como propiedades y sus valores deben ser los objetos [externalReference](plannerexternalreference.md). De acuerdo con OData, los nombres de propiedad de los tipos abiertos no pueden contener los caracteres siguientes: `.`, `:` y `%`. Por este motivo, deberán codificarse. A continuación se muestra un ejemplo. Para quitar una referencia, establezca el valor de la propiedad en `null`.</span><span class="sxs-lookup"><span data-stu-id="ec56a-p104">Properties of an Open Type can be defined by the client. In this case, the client must provide **valid URLs** based on the **HTTP/HTTPS** protocols as properties and their values must be the [externalReference](plannerexternalreference.md) objects. Based on OData, property names in Open Types cannot contain the following characters: `.`, `:`, `%`  so they need to be encoded. Example is shown below. To remove a reference, set the value of the property to `null`.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ec56a-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ec56a-119">JSON representation</span></span>

<span data-ttu-id="ec56a-120">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ec56a-120">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerExternalReferences"
}-->


```json
{
  "String-value":
  {
    "alias": "String-value",
    "lastModifiedBy": "String-value",
    "lastModifiedDateTime": "String(timestamp)",
    "previewPriority": "String-value",
    "type": "String-value"
  }
}
```

<span data-ttu-id="ec56a-121">// Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec56a-121">// Example</span></span>

```json
{
  "https%3A//contoso%2Esharepoint%2Ecom/teams/agile/documents/AnnualReport%2Epptx":
  {
    "@odata.type": "microsoft.graph.externalReference", // required in PATCH requests to edit the references on a task
    "alias": "Agile Team Annual Report",
    "lastModifiedBy": {
      "user": {
        "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
      }
    },
    "lastModifiedDateTime": "2015-09-21T17:45:12.039Z",
    "previewPriority": "0009005756397228702",
    "type": "PowerPoint"
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerExternalReferences resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
