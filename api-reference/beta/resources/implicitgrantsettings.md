---
title: tipo de recurso implicitGrantSettings
description: Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita. Están disponibles para solicitar los tokens de acceso y el identificador como parte del flujo implícita de propiedades independientes. Para habilitar el flujo implícita, al menos una de las siguientes propiedades debe estar establecida en true.
ms.openlocfilehash: 018cd422b56724811e1913ff0e94aea16d7c68f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085474"
---
# <a name="implicitgrantsettings-resource-type"></a>tipo de recurso implicitGrantSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita. Están disponibles para solicitar los tokens de acceso y el identificador como parte del flujo implícita de propiedades independientes. Para habilitar el flujo implícita, al menos una de las siguientes propiedades debe estar establecida en true.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------|:-----|:------------|
|enableIdTokenIssuance| Booleano | Especifica si esta aplicación web puede solicitar un token de identificador con el flujo de OAuth 2.0 implícita.|
|enableAccessTokenIssuance| Booleano | Especifica si esta aplicación web puede solicitar un token de acceso con el flujo de OAuth 2.0 implícita.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

```json
{
  "enableIdTokenIssuance": "Boolean",
  "enableAccessTokenIssuance": "Boolean"
}

```
