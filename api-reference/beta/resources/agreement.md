---
title: tipo de recurso de contrato
description: Representa un condiciones de personalizable del inquilino de uso que se crean y administran con Azure Active Directory (AD Azure). Puede usar los siguientes métodos para crear y administrar la característica de Azure Active Directory condiciones de uso según su situación.
localization_priority: Normal
ms.openlocfilehash: 8c082ed6229b44cc3a3d4cba6dd8645feee5d07c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845349"
---
# <a name="agreement-resource-type"></a>tipo de recurso de contrato

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un condiciones de personalizable del inquilino de uso que se crean y administran con Azure Active Directory (AD Azure). Puede usar los siguientes métodos para crear y administrar la [característica de Azure Active Directory condiciones de uso](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-tou) de acuerdo con su escenario.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto | Descripción |
|:-------------|:------------|:------------|
| [Crear contratos](../api/agreement-post-agreements.md) | [contrato](agreement.md) | Crear un nuevo acuerdo de registro a la colección de contrato. |
| [Contratos de lista](../api/agreement-list.md) | colección de [contrato](agreement.md) | Obtener una colección de objetos de contrato. |
| [Obtener el contrato](../api/agreement-get.md) | [contrato](agreement.md) | Leer las propiedades y relaciones de un objeto de contrato. |
| [Contrato de actualización](../api/agreement-update.md) | [contrato](agreement.md) | Actualizar un objeto de contrato. |
| [Eliminar contrato](../api/agreement-delete.md) | Ninguno | Eliminación de un objeto de contrato. |
<!--
| [Create agreementFile](../api/agreement-post-files.md) | [agreementFile](agreementfile.md) | Create a new agreementFile by posting to the files collection. |
| [List files](../api/agreement-list-files.md) | [agreementFile](agreementfile.md) collection | Get an agreementFile object collection. |
-->

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo        | Descripción |
|:-------------|:------------|:------------|
|displayName|Cadena|Nombre para mostrar del contrato.|
|id|Cadena| Solo lectura.|
|isViewingBeforeAcceptanceRequired|Booleano|Indica si el usuario tiene que expandir y ver el contrato antes de Aceptar.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo        | Descripción |
|:-------------|:------------|:------------|
|archivos|colección de [agreementFile](agreementfile.md)|Solo lectura. Documentos PDF vinculan a este contrato.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreement"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "isViewingBeforeAcceptanceRequired": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "agreement resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
