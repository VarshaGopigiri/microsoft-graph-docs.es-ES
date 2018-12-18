---
title: tipo de recurso educationSubmissionIndividualRecipient
description: 'Una subclase de educationSubmissionRecipient que indica que se ha asignado un envío a una persona en la clase.  '
author: dipakboyed
ms.openlocfilehash: 3447c91fe4f387508a3afdf80a7337786d46f860
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318805"
---
# <a name="educationsubmissionindividualrecipient-resource-type"></a>tipo de recurso educationSubmissionIndividualRecipient

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una subclase de [educationSubmissionRecipient](educationsubmissionrecipient.md) que indica que se ha asignado un envío a una persona en la clase.  


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|userId|String|Identificador de usuario del usuario a quien se asigna el envío.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSubmissionIndividualRecipient"
}-->

```json
{
  "userId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSubmissionIndividualRecipient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->