---
title: recursos de educationPowerSchoolDataProvider
description: Se usa para configurar el perfil de sincronización de datos de school cuando PowerSchool se utiliza como el origen de entrada.
author: mmast-msft
ms.openlocfilehash: 714866d03c70aae8ea03a27b63fb3efbb4fa5ba4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27312806"
---
# <a name="educationpowerschooldataprovider-resource"></a><span data-ttu-id="c8698-103">recursos de educationPowerSchoolDataProvider</span><span class="sxs-lookup"><span data-stu-id="c8698-103">educationPowerSchoolDataProvider resource</span></span>

> <span data-ttu-id="c8698-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c8698-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c8698-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c8698-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c8698-106">Se usa para configurar el perfil de sincronización de datos de school cuando [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) se utiliza como el origen de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8698-106">Used to set up the school data synchronization profile when [PowerSchool](https://www.powerschool.com/solutions/student-information-system-sis/) is used as the input source.</span></span>

<span data-ttu-id="c8698-107">Deriva de [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span><span class="sxs-lookup"><span data-stu-id="c8698-107">Derived from [educationSynchronizationDataProvider](educationsynchronizationdataprovider.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c8698-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8698-108">Properties</span></span>

| <span data-ttu-id="c8698-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8698-109">Property</span></span> | <span data-ttu-id="c8698-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8698-110">Type</span></span> | <span data-ttu-id="c8698-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8698-111">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="c8698-112">**connectionUrl**</span><span class="sxs-lookup"><span data-stu-id="c8698-112">**connectionUrl**</span></span> | <span data-ttu-id="c8698-113">String</span><span class="sxs-lookup"><span data-stu-id="c8698-113">String</span></span> | <span data-ttu-id="c8698-114">La dirección URL de conexión a la instancia de PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="c8698-114">The connection URL to the PowerSchool instance.</span></span> |
| <span data-ttu-id="c8698-115">**clientId**</span><span class="sxs-lookup"><span data-stu-id="c8698-115">**clientId**</span></span> | <span data-ttu-id="c8698-116">String</span><span class="sxs-lookup"><span data-stu-id="c8698-116">String</span></span> |  <span data-ttu-id="c8698-117">El identificador de cliente que se usa para conectarse a PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="c8698-117">The client ID used to connect to PowerSchool.</span></span> |
| <span data-ttu-id="c8698-118">**clientSecret**</span><span class="sxs-lookup"><span data-stu-id="c8698-118">**clientSecret**</span></span> | <span data-ttu-id="c8698-119">String</span><span class="sxs-lookup"><span data-stu-id="c8698-119">String</span></span> |  <span data-ttu-id="c8698-120">El secreto de cliente para autenticar la conexión a la instancia de PowerSchool.</span><span class="sxs-lookup"><span data-stu-id="c8698-120">The client secret to authenticate the connection to the PowerSchool instance.</span></span> |
| <span data-ttu-id="c8698-121">**schoolsIds**</span><span class="sxs-lookup"><span data-stu-id="c8698-121">**schoolsIds**</span></span> | <span data-ttu-id="c8698-122">Colección String</span><span class="sxs-lookup"><span data-stu-id="c8698-122">String collection</span></span> |  <span data-ttu-id="c8698-123">La lista de escuelas para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="c8698-123">The list of schools to sync.</span></span> |
| <span data-ttu-id="c8698-124">**schoolYear**</span><span class="sxs-lookup"><span data-stu-id="c8698-124">**schoolYear**</span></span> | <span data-ttu-id="c8698-125">String</span><span class="sxs-lookup"><span data-stu-id="c8698-125">String</span></span> |  <span data-ttu-id="c8698-126">El año escolar para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="c8698-126">The school year to sync.</span></span> |
| <span data-ttu-id="c8698-127">**allowTeachersInMultipleSchools**</span><span class="sxs-lookup"><span data-stu-id="c8698-127">**allowTeachersInMultipleSchools**</span></span> | <span data-ttu-id="c8698-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="c8698-128">Boolean</span></span> |  <span data-ttu-id="c8698-129">Indica si el origen tiene varios identificadores para un solo alumno o profesor.</span><span class="sxs-lookup"><span data-stu-id="c8698-129">Indicates whether the source has multiple identifiers for a single student or teacher.</span></span> |
| <span data-ttu-id="c8698-130">**personalizaciones**</span><span class="sxs-lookup"><span data-stu-id="c8698-130">**customizations**</span></span> | [<span data-ttu-id="c8698-131">educationSynchronizationCustomizations</span><span class="sxs-lookup"><span data-stu-id="c8698-131">educationSynchronizationCustomizations</span></span>](educationsynchronizationcustomizations.md) | <span data-ttu-id="c8698-132">Personalización opcional que se aplicará a los perfiles de sincronización.</span><span class="sxs-lookup"><span data-stu-id="c8698-132">Optional customization to be applied to the synchronization profile.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="c8698-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c8698-133">JSON representation</span></span>
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
