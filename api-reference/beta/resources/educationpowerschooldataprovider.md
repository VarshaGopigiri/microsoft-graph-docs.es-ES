---
title: recursos de educationPowerSchoolDataProvider
description: Se usa para configurar el perfil de sincronización de datos de school cuando PowerSchool se utiliza como el origen de entrada.
ms.openlocfilehash: 4c58d3b8baf1569aaeff68375b2dd3643db8b063
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088538"
---
# <a name="educationpowerschooldataprovider-resource"></a><span data-ttu-id="ce033-103">recursos de educationPowerSchoolDataProvider</span><span class="sxs-lookup"><span data-stu-id="ce033-103">educationPowerSchoolDataProvider resource</span></span>

> <span data-ttu-id="ce033-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce033-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce033-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce033-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ce033-106">Se usa para configurar el perfil de sincronización de datos de school cuando [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) se utiliza como el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="ce033-106">Used to set up the school data synchronization profile when [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) is used as the input source.</span></span>

<span data-ttu-id="ce033-107">Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="ce033-107">Derived from [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ce033-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce033-108">Properties</span></span>

| <span data-ttu-id="ce033-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce033-109">Property</span></span> | <span data-ttu-id="ce033-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce033-110">Type</span></span> | <span data-ttu-id="ce033-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce033-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="ce033-112">**connectionUrl**</span><span class="sxs-lookup"><span data-stu-id="ce033-112">**connectionUrl**</span></span> | <span data-ttu-id="ce033-113">String</span><span class="sxs-lookup"><span data-stu-id="ce033-113">String</span></span> | <span data-ttu-id="ce033-114">La dirección URL de conexión a la instancia de PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="ce033-114">The connection URL to the PowerSchool instance.</span></span> |
| <span data-ttu-id="ce033-115">**clientId**</span><span class="sxs-lookup"><span data-stu-id="ce033-115">**clientId**</span></span> | <span data-ttu-id="ce033-116">String</span><span class="sxs-lookup"><span data-stu-id="ce033-116">String</span></span> |  <span data-ttu-id="ce033-117">El identificador de cliente que se usa para conectarse a PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="ce033-117">The client ID used to connect to PowerSchool.</span></span> |
| <span data-ttu-id="ce033-118">**clientSecret**</span><span class="sxs-lookup"><span data-stu-id="ce033-118">**clientSecret**</span></span> | <span data-ttu-id="ce033-119">String</span><span class="sxs-lookup"><span data-stu-id="ce033-119">String</span></span> |  <span data-ttu-id="ce033-120">El secreto de cliente para autenticar la conexión a la instancia de PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="ce033-120">The client secret to authenticate the connection to the PowerSchool instance.</span></span> |
| <span data-ttu-id="ce033-121">**schoolsIds**</span><span class="sxs-lookup"><span data-stu-id="ce033-121">**schoolsIds**</span></span> | <span data-ttu-id="ce033-122">Colección String</span><span class="sxs-lookup"><span data-stu-id="ce033-122">String collection</span></span> |  <span data-ttu-id="ce033-123">La lista de escuelas para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="ce033-123">The list of schools to sync.</span></span> |
| <span data-ttu-id="ce033-124">**schoolYear**</span><span class="sxs-lookup"><span data-stu-id="ce033-124">**schoolYear**</span></span> | <span data-ttu-id="ce033-125">String</span><span class="sxs-lookup"><span data-stu-id="ce033-125">String</span></span> |  <span data-ttu-id="ce033-126">El año escolar para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="ce033-126">The school year to sync.</span></span> |
| <span data-ttu-id="ce033-127">**allowTeachersInMultipleSchools**</span><span class="sxs-lookup"><span data-stu-id="ce033-127">**allowTeachersInMultipleSchools**</span></span> | <span data-ttu-id="ce033-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="ce033-128">Boolean</span></span> |  <span data-ttu-id="ce033-129">Indica si el origen tiene varios identificadores para un solo alumno o profesor.</span><span class="sxs-lookup"><span data-stu-id="ce033-129">Indicates whether the source has multiple identifiers for a single student or teacher.</span></span> |
| <span data-ttu-id="ce033-130">**personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="ce033-130">**customizations**</span></span> | [<span data-ttu-id="ce033-131">educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="ce033-131">educationSynchronizationCustomizations</span></span>](educationsynchronizationcustomizations.md) | <span data-ttu-id="ce033-132">Personalización opcional que se aplicará a los perfiles de sincronización.</span><span class="sxs-lookup"><span data-stu-id="ce033-132">Optional customization to be applied to the synchronization profile.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ce033-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ce033-133">JSON representation</span></span>
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationPowerSchoolDataProvider"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationPowerSchoolDataProvider",
    "connectionUrl": "String",
    "clientId": "String",
    "clientSecret": "String",
    "schoolsids": ["String"],
    "schoolYear": "String",
    "allowTeachersInMultipleSchools": "Boolean",
    "customizations": { "@odata.type": "microsoft.graph.educationSynchronizationCustomizations" }
}
```
