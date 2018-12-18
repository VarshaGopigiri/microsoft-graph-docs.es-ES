---
title: insightIdentity
description: Tipo complejo que contiene las propiedades de los elementos compartidos.
author: simonhult
ms.openlocfilehash: 648242b827c0390029522955b0fe6347b98100c4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331336"
---
# <a name="insightidentity"></a>insightIdentity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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