---
title: recursos de educationOneRosterApiDataProvider
description: Se usa para configurar el perfil de sincronización de datos de school cuando se usa la API OneRoster como el origen de entrada.
ms.openlocfilehash: 0fd9c87c9934fc86d4e6788a5db42eb036fdb04f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086757"
---
# <a name="educationonerosterapidataprovider-resource"></a><span data-ttu-id="fa440-103">recursos de educationOneRosterApiDataProvider</span><span class="sxs-lookup"><span data-stu-id="fa440-103">educationOneRosterApiDataProvider resource</span></span>

> <span data-ttu-id="fa440-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fa440-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fa440-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fa440-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fa440-106">Se usa para configurar el perfil de sincronización de datos de school cuando se usa la [API de OneRoster](https://www.imsglobal.org/activity/onerosterlis) como el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="fa440-106">Used to set up the school data synchronization profile when the [OneRoster API](https://www.imsglobal.org/activity/onerosterlis) is used as the input source.</span></span>

<span data-ttu-id="fa440-107">Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="fa440-107">Derived from [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fa440-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fa440-108">Properties</span></span>

| <span data-ttu-id="fa440-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fa440-109">Property</span></span> | <span data-ttu-id="fa440-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa440-110">Type</span></span> | <span data-ttu-id="fa440-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa440-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="fa440-112">**connectionUrl**</span><span class="sxs-lookup"><span data-stu-id="fa440-112">**connectionUrl**</span></span> | <span data-ttu-id="fa440-113">String</span><span class="sxs-lookup"><span data-stu-id="fa440-113">String</span></span> | <span data-ttu-id="fa440-114">La dirección URL de conexión a la instancia de OneRoster.</span><span class="sxs-lookup"><span data-stu-id="fa440-114">The connection URL to the OneRoster instance.</span></span> |
| <span data-ttu-id="fa440-115">**schoolsIds**</span><span class="sxs-lookup"><span data-stu-id="fa440-115">**schoolsIds**</span></span> | <span data-ttu-id="fa440-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="fa440-116">String collection</span></span> |  <span data-ttu-id="fa440-117">La lista de sourcedIds school para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="fa440-117">The list of school sourcedIds to sync.</span></span> |
| <span data-ttu-id="fa440-118">**providerName**</span><span class="sxs-lookup"><span data-stu-id="fa440-118">**providerName**</span></span> | <span data-ttu-id="fa440-119">String</span><span class="sxs-lookup"><span data-stu-id="fa440-119">String</span></span> | <span data-ttu-id="fa440-120">El nombre del proveedor de servicio de OneRoster tal y como se define en la [especificación de OneRoster](https://www.imsglobal.org/oneroster-v11-final-best-practice-and-implementation-guide#AppA).</span><span class="sxs-lookup"><span data-stu-id="fa440-120">The OneRoster Service Provider name as defined by the [OneRoster specification](https://www.imsglobal.org/oneroster-v11-final-best-practice-and-implementation-guide#AppA).</span></span> |
| <span data-ttu-id="fa440-121">**connectionSettings**</span><span class="sxs-lookup"><span data-stu-id="fa440-121">**connectionSettings**</span></span> | [<span data-ttu-id="fa440-122">educationSynchronizationConnectionSettings</span><span class="sxs-lookup"><span data-stu-id="fa440-122">educationSynchronizationConnectionSettings</span></span>](educationsynchronizationconnectionsettings.md) | <span data-ttu-id="fa440-123">Configuración de conexión para la instancia de OneRoster.</span><span class="sxs-lookup"><span data-stu-id="fa440-123">Connection settings for the OneRoster instance.</span></span> <span data-ttu-id="fa440-124">Debe ser del tipo [educationSynchronizationOAuth1ConnectionSettings](educationsynchronizationoauth1connectionsettings.md) o [educationSynchronizationOAuth2ClientCredentialsConnectionSettings](educationsynchronizationoauth2clientcredentialsconnectionsettings.md).</span><span class="sxs-lookup"><span data-stu-id="fa440-124">Should be of type [educationSynchronizationOAuth1ConnectionSettings](educationsynchronizationoauth1connectionsettings.md) or [educationSynchronizationOAuth2ClientCredentialsConnectionSettings](educationsynchronizationoauth2clientcredentialsconnectionsettings.md).</span></span> |
| <span data-ttu-id="fa440-125">**personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="fa440-125">**customizations**</span></span> | [<span data-ttu-id="fa440-126">educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="fa440-126">educationSynchronizationCustomizations</span></span>](educationsynchronizationcustomizations.md) | <span data-ttu-id="fa440-127">Personalización opcional que se aplicará a los perfiles de sincronización.</span><span class="sxs-lookup"><span data-stu-id="fa440-127">Optional customization to be applied to the synchronization profile.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fa440-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fa440-128">JSON representation</span></span>
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
