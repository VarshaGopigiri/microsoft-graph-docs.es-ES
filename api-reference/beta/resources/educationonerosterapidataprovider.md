---
title: recursos de educationOneRosterApiDataProvider
description: Se usa para configurar el perfil de sincronización de datos de school cuando se usa la API OneRoster como el origen de entrada.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: a99343ed8026eda9ecf56925986f4a0bfe10b3ef
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858159"
---
# <a name="educationonerosterapidataprovider-resource"></a><span data-ttu-id="99581-103">recursos de educationOneRosterApiDataProvider</span><span class="sxs-lookup"><span data-stu-id="99581-103">educationOneRosterApiDataProvider resource</span></span>

> <span data-ttu-id="99581-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99581-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99581-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99581-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="99581-106">Se usa para configurar el perfil de sincronización de datos de school cuando se usa la [API de OneRoster](https://www.imsglobal.org/activity/onerosterlis) como el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="99581-106">Used to set up the school data synchronization profile when the [OneRoster API](https://www.imsglobal.org/activity/onerosterlis) is used as the input source.</span></span>

<span data-ttu-id="99581-107">Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="99581-107">Derived from [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span></span>

## <a name="properties"></a><span data-ttu-id="99581-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="99581-108">Properties</span></span>

| <span data-ttu-id="99581-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99581-109">Property</span></span> | <span data-ttu-id="99581-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="99581-110">Type</span></span> | <span data-ttu-id="99581-111">Description</span><span class="sxs-lookup"><span data-stu-id="99581-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="99581-112">**connectionUrl**</span><span class="sxs-lookup"><span data-stu-id="99581-112">**connectionUrl**</span></span> | <span data-ttu-id="99581-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="99581-113">String</span></span> | <span data-ttu-id="99581-114">La dirección URL de conexión a la instancia de OneRoster.</span><span class="sxs-lookup"><span data-stu-id="99581-114">The connection URL to the OneRoster instance.</span></span> |
| <span data-ttu-id="99581-115">**schoolsIds**</span><span class="sxs-lookup"><span data-stu-id="99581-115">**schoolsIds**</span></span> | <span data-ttu-id="99581-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="99581-116">String collection</span></span> |  <span data-ttu-id="99581-117">La lista de sourcedIds school para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="99581-117">The list of school sourcedIds to sync.</span></span> |
| <span data-ttu-id="99581-118">**providerName**</span><span class="sxs-lookup"><span data-stu-id="99581-118">**providerName**</span></span> | <span data-ttu-id="99581-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="99581-119">String</span></span> | <span data-ttu-id="99581-120">El nombre del proveedor de servicio de OneRoster tal y como se define en la [especificación de OneRoster](https://www.imsglobal.org/oneroster-v11-final-best-practice-and-implementation-guide#AppA).</span><span class="sxs-lookup"><span data-stu-id="99581-120">The OneRoster Service Provider name as defined by the [OneRoster specification](https://www.imsglobal.org/oneroster-v11-final-best-practice-and-implementation-guide#AppA).</span></span> |
| <span data-ttu-id="99581-121">**connectionSettings**</span><span class="sxs-lookup"><span data-stu-id="99581-121">**connectionSettings**</span></span> | [<span data-ttu-id="99581-122">educationSynchronizationConnectionSettings</span><span class="sxs-lookup"><span data-stu-id="99581-122">educationSynchronizationConnectionSettings</span></span>](educationsynchronizationconnectionsettings.md) | <span data-ttu-id="99581-123">Configuración de conexión para la instancia de OneRoster.</span><span class="sxs-lookup"><span data-stu-id="99581-123">Connection settings for the OneRoster instance.</span></span> <span data-ttu-id="99581-124">Debe ser del tipo [educationSynchronizationOAuth1ConnectionSettings](educationsynchronizationoauth1connectionsettings.md) o [educationSynchronizationOAuth2ClientCredentialsConnectionSettings](educationsynchronizationoauth2clientcredentialsconnectionsettings.md).</span><span class="sxs-lookup"><span data-stu-id="99581-124">Should be of type [educationSynchronizationOAuth1ConnectionSettings](educationsynchronizationoauth1connectionsettings.md) or [educationSynchronizationOAuth2ClientCredentialsConnectionSettings](educationsynchronizationoauth2clientcredentialsconnectionsettings.md).</span></span> |
| <span data-ttu-id="99581-125">**personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="99581-125">**customizations**</span></span> | [<span data-ttu-id="99581-126">educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="99581-126">educationSynchronizationCustomizations</span></span>](educationsynchronizationcustomizations.md) | <span data-ttu-id="99581-127">Personalización opcional que se aplicará a los perfiles de sincronización.</span><span class="sxs-lookup"><span data-stu-id="99581-127">Optional customization to be applied to the synchronization profile.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="99581-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="99581-128">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationoneRosterApiDataProvider"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationoneRosterApiDataProvider",
    "connectionUrl": "String",
    "providerName": "String",
    "schoolsIds": [
        "String"
    ],
    "connectionSettings": {
        "@odata.type": "#microsoft.graph.educationSynchronizationOAuth1ConnectionSettings",
        "clientId": "String",
        "clientSecret": "String",
    },
    "customizations": { "@odata.type": "microsoft.graph.educationSynchronizationCustomizations" }
}
```
