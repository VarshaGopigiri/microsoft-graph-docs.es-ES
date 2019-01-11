---
title: tipo de recurso governancePermission
description: 'Representa el permiso de acceso que tiene un governanceSubject para un governanceResource específica.  '
localization_priority: Normal
ms.openlocfilehash: e082ca50e5642e865b3e30859eea607df63a03b4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882877"
---
# <a name="governancepermission-resource-type"></a>tipo de recurso governancePermission

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el permiso de acceso que tiene un [governanceSubject](../resources/governancesubject.md) para un específico [governanceResource](../resources/governanceresource.md).  


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|accessLevel|Cadena|El nivel de acceso. Valores válidos: ``None``, ``UserRead``, ``AdminRead``, y ``AdminReadWrite``.|
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
