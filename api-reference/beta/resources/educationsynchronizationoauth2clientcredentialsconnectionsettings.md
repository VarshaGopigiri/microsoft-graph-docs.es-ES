---
title: recursos de educationSynchronizationOAuth2ClientCredentialsConnectionSettings
description: Al conceder de credenciales de cliente de OAuth2 es que se usará para conectarse al proveedor de datos, debe usarse este tipo de configuración de conexión para configurar el perfil.
ms.openlocfilehash: 901fabb802d4ed5fa0c99538e52b9a07199eb298
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088875"
---
# <a name="educationsynchronizationoauth2clientcredentialsconnectionsettings-resource"></a><span data-ttu-id="ff3da-103">recursos de educationSynchronizationOAuth2ClientCredentialsConnectionSettings</span><span class="sxs-lookup"><span data-stu-id="ff3da-103">educationSynchronizationOAuth2ClientCredentialsConnectionSettings resource</span></span>

> <span data-ttu-id="ff3da-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff3da-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff3da-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff3da-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ff3da-106">Al [Conceder de credenciales de cliente de OAuth2](https://tools.ietf.org/html/rfc6749#section-4.4) es que se usará para conectarse al proveedor de datos, debe usarse este tipo de configuración de conexión para configurar el perfil.</span><span class="sxs-lookup"><span data-stu-id="ff3da-106">When [OAuth2 Client Credentials Grant](https://tools.ietf.org/html/rfc6749#section-4.4) is to be used to connect to the data provider, this connection settings type should be used to set up the profile.</span></span>

<span data-ttu-id="ff3da-107">Deriva de [educationSynchronizationConnectionSettings](educationsynchronizationconnectionsettings.md).</span><span class="sxs-lookup"><span data-stu-id="ff3da-107">Derived from [educationSynchronizationConnectionSettings](educationsynchronizationconnectionsettings.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ff3da-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff3da-108">Properties</span></span>

| <span data-ttu-id="ff3da-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff3da-109">Property</span></span> | <span data-ttu-id="ff3da-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff3da-110">Type</span></span> | <span data-ttu-id="ff3da-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff3da-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="ff3da-112">**tokenUrl**</span><span class="sxs-lookup"><span data-stu-id="ff3da-112">**tokenUrl**</span></span> | <span data-ttu-id="ff3da-113">String</span><span class="sxs-lookup"><span data-stu-id="ff3da-113">String</span></span> | <span data-ttu-id="ff3da-114">La dirección URL para obtener los tokens de acceso para el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="ff3da-114">The URL to get access tokens for the data provider.</span></span> |
| <span data-ttu-id="ff3da-115">**ámbito**</span><span class="sxs-lookup"><span data-stu-id="ff3da-115">**scope**</span></span> | <span data-ttu-id="ff3da-116">String</span><span class="sxs-lookup"><span data-stu-id="ff3da-116">String</span></span> | <span data-ttu-id="ff3da-117">[El ámbito de la solicitud de acceso](https://tools.ietf.org/html/rfc6749#section-3.3).</span><span class="sxs-lookup"><span data-stu-id="ff3da-117">[The scope of the access request](https://tools.ietf.org/html/rfc6749#section-3.3).</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ff3da-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ff3da-118">JSON representation</span></span>
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
