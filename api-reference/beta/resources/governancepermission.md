---
title: tipo de recurso governancePermission
description: 'Representa el permiso de acceso que tiene un governanceSubject para un governanceResource específica.  '
ms.openlocfilehash: d7b3e1eb70c89c278ccc2a8b3e9a16e265e4ae97
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087740"
---
# <a name="governancepermission-resource-type"></a>tipo de recurso governancePermission

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el permiso de acceso que tiene un [governanceSubject](../resources/governancesubject.md) para un específico [governanceResource](../resources/governanceresource.md).  


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|accessLevel|String|El nivel de acceso. Valores válidos: ``None``, ``UserRead``, ``AdminRead``, y ``AdminReadWrite``.|
|isActive|Booleano|Indicar si el solicitante tiene cualquier asignación de rol activo para el nivel de acceso.|
|isEligible|Booleano|Indicar si el solicitante no tiene ninguna asignación de roles aptos para el nivel de acceso.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

```json
{
  "accessLevel": "String",
  "isActive": true,
  "isEligible": true
}

```