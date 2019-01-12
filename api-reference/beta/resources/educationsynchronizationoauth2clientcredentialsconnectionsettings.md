---
title: recursos de educationSynchronizationOAuth2ClientCredentialsConnectionSettings
description: Al conceder de credenciales de cliente de OAuth2 es que se usará para conectarse al proveedor de datos, debe usarse este tipo de configuración de conexión para configurar el perfil.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 8976c3a3a6088abd88cf70182040d4b3a6cc3f7d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912893"
---
# <a name="educationsynchronizationoauth2clientcredentialsconnectionsettings-resource"></a><span data-ttu-id="8e0a0-103">recursos de educationSynchronizationOAuth2ClientCredentialsConnectionSettings</span><span class="sxs-lookup"><span data-stu-id="8e0a0-103">educationSynchronizationOAuth2ClientCredentialsConnectionSettings resource</span></span>

> <span data-ttu-id="8e0a0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8e0a0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8e0a0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8e0a0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8e0a0-106">Al [Conceder de credenciales de cliente de OAuth2](https://tools.ietf.org/html/rfc6749#section-4.4) es que se usará para conectarse al proveedor de datos, debe usarse este tipo de configuración de conexión para configurar el perfil.</span><span class="sxs-lookup"><span data-stu-id="8e0a0-106">When [OAuth2 Client Credentials Grant](https://tools.ietf.org/html/rfc6749#section-4.4) is to be used to connect to the data provider, this connection settings type should be used to set up the profile.</span></span>

<span data-ttu-id="8e0a0-107">Deriva de [educationSynchronizationConnectionSettings](educationsynchronizationconnectionsettings.md).</span><span class="sxs-lookup"><span data-stu-id="8e0a0-107">Derived from [educationSynchronizationConnectionSettings](educationsynchronizationconnectionsettings.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8e0a0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e0a0-108">Properties</span></span>

| <span data-ttu-id="8e0a0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8e0a0-109">Property</span></span> | <span data-ttu-id="8e0a0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e0a0-110">Type</span></span> | <span data-ttu-id="8e0a0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e0a0-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="8e0a0-112">**tokenUrl**</span><span class="sxs-lookup"><span data-stu-id="8e0a0-112">**tokenUrl**</span></span> | <span data-ttu-id="8e0a0-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="8e0a0-113">String</span></span> | <span data-ttu-id="8e0a0-114">La dirección URL para obtener los tokens de acceso para el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="8e0a0-114">The URL to get access tokens for the data provider.</span></span> |
| <span data-ttu-id="8e0a0-115">**ámbito**</span><span class="sxs-lookup"><span data-stu-id="8e0a0-115">**scope**</span></span> | <span data-ttu-id="8e0a0-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="8e0a0-116">String</span></span> | <span data-ttu-id="8e0a0-117">[El ámbito de la solicitud de acceso](https://tools.ietf.org/html/rfc6749#section-3.3).</span><span class="sxs-lookup"><span data-stu-id="8e0a0-117">[The scope of the access request](https://tools.ietf.org/html/rfc6749#section-3.3).</span></span> |

## <a name="json-representation"></a><span data-ttu-id="8e0a0-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8e0a0-118">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "#microsoft.graph.educationSynchronizationOAuth2ClientCredentialsConnectionSettings"
}-->

```json
"connectionSettings": {
    "@odata.type": "#microsoft.graph.educationSynchronizationOAuth2ClientCredentialsConnectionSettings",
    "clientId": "String",
    "clientSecret": "String",
    "tokenUrl": "String",
    "scope": "String"
}
```
