---
title: insightIdentity
description: " tipo de recurso"
ms.openlocfilehash: e13d08eb111844896c96b02ab22c52d2f598ce58
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087751"
---
# <a name="insightidentity"></a>insightIdentity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

 tipo de recurso

Tipo complejo que contiene las propiedades de los elementos [compartidos](insights-shared.md) . 

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso

```json
{
  "displayName": "string",
  "id": "string",
  "address": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo          | Descripción  |
| -------------         |-----------    | -------------|
| displayName       | String          | El nombre para mostrar del usuario que comparte el elemento. |
| id              | String        | El identificador del usuario que comparte el elemento.     |
| address             | String      | La dirección de correo electrónico del usuario que comparte el elemento.  |