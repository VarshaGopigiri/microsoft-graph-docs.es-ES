---
title: tipo de recurso implicitGrantSettings
description: Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita. Están disponibles para solicitar los tokens de acceso y el identificador como parte del flujo implícita de propiedades independientes. Para habilitar el flujo implícita, al menos una de las siguientes propiedades debe estar establecida en true.
localization_priority: Normal
ms.openlocfilehash: 93a54ac0c0e4c6c32ebb99c9747d44d75f98af07
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834268"
---
# <a name="implicitgrantsettings-resource-type"></a>tipo de recurso implicitGrantSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica si esta aplicación web puede solicitar tokens con el flujo de OAuth 2.0 implícita. Están disponibles para solicitar los tokens de acceso y el identificador como parte del flujo implícita de propiedades independientes. Para habilitar el flujo implícita, al menos una de las siguientes propiedades debe estar establecida en true.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
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
