---
title: Tipo de recurso auditActor
description: Una clase que contiene las propiedades del actor de auditoría.
author: tfitzmac
ms.openlocfilehash: de2fc78bcc02565da102beb57c077646effc443b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27325021"
---
# <a name="auditactor-resource-type"></a><span data-ttu-id="2a8f3-103">Tipo de recurso auditActor</span><span class="sxs-lookup"><span data-stu-id="2a8f3-103">auditActor resource type</span></span>

> <span data-ttu-id="2a8f3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2a8f3-105">Una clase que contiene las propiedades del actor de auditoría.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-105">A class containing the properties for Audit Actor.</span></span>
## <a name="properties"></a><span data-ttu-id="2a8f3-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a8f3-106">Properties</span></span>
|<span data-ttu-id="2a8f3-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2a8f3-107">Property</span></span>|<span data-ttu-id="2a8f3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a8f3-108">Type</span></span>|<span data-ttu-id="2a8f3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a8f3-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a8f3-110">type</span><span class="sxs-lookup"><span data-stu-id="2a8f3-110">type</span></span>|<span data-ttu-id="2a8f3-111">cadena</span><span class="sxs-lookup"><span data-stu-id="2a8f3-111">String</span></span>|<span data-ttu-id="2a8f3-112">Tipo de actor.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-112">Actor Type.</span></span>|
|<span data-ttu-id="2a8f3-113">userPermissions</span><span class="sxs-lookup"><span data-stu-id="2a8f3-113">userPermissions</span></span>|<span data-ttu-id="2a8f3-114">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="2a8f3-114">String collection</span></span>|<span data-ttu-id="2a8f3-115">Lista de los permisos de usuario cuando se ha realizado la auditoría.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-115">List of user permissions when the audit was performed.</span></span>|
|<span data-ttu-id="2a8f3-116">applicationId</span><span class="sxs-lookup"><span data-stu-id="2a8f3-116">applicationId</span></span>|<span data-ttu-id="2a8f3-117">cadena</span><span class="sxs-lookup"><span data-stu-id="2a8f3-117">String</span></span>|<span data-ttu-id="2a8f3-118">Id. de aplicación de AAD</span><span class="sxs-lookup"><span data-stu-id="2a8f3-118">AAD Application Id.</span></span>|
|<span data-ttu-id="2a8f3-119">applicationDisplayName</span><span class="sxs-lookup"><span data-stu-id="2a8f3-119">applicationDisplayName</span></span>|<span data-ttu-id="2a8f3-120">cadena</span><span class="sxs-lookup"><span data-stu-id="2a8f3-120">String</span></span>|<span data-ttu-id="2a8f3-121">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-121">Name of the Application.</span></span>|
|<span data-ttu-id="2a8f3-122">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2a8f3-122">userPrincipalName</span></span>|<span data-ttu-id="2a8f3-123">cadena</span><span class="sxs-lookup"><span data-stu-id="2a8f3-123">String</span></span>|<span data-ttu-id="2a8f3-124">Nombre principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="2a8f3-124">User Principal Name (UPN).</span></span>|
|<span data-ttu-id="2a8f3-125">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2a8f3-125">servicePrincipalName</span></span>|<span data-ttu-id="2a8f3-126">cadena</span><span class="sxs-lookup"><span data-stu-id="2a8f3-126">String</span></span>|<span data-ttu-id="2a8f3-127">Nombre de entidad de seguridad de servicio (SPN).</span><span class="sxs-lookup"><span data-stu-id="2a8f3-127">Service Principal Name (SPN).</span></span>|
|<span data-ttu-id="2a8f3-128">ipAddress</span><span class="sxs-lookup"><span data-stu-id="2a8f3-128">ipAddress</span></span>|<span data-ttu-id="2a8f3-129">cadena</span><span class="sxs-lookup"><span data-stu-id="2a8f3-129">String</span></span>|<span data-ttu-id="2a8f3-130">IPAddress.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-130">IPAddress.</span></span>|
|<span data-ttu-id="2a8f3-131">userId</span><span class="sxs-lookup"><span data-stu-id="2a8f3-131">userId</span></span>|<span data-ttu-id="2a8f3-132">cadena</span><span class="sxs-lookup"><span data-stu-id="2a8f3-132">String</span></span>|<span data-ttu-id="2a8f3-133">Id. de usuario.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-133">User Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2a8f3-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2a8f3-134">Relationships</span></span>
<span data-ttu-id="2a8f3-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2a8f3-135">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2a8f3-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2a8f3-136">JSON Representation</span></span>
<span data-ttu-id="2a8f3-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2a8f3-137">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditActor"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditActor",
  "type": "String",
  "userPermissions": [
    "String"
  ],
  "applicationId": "String",
  "applicationDisplayName": "String",
  "userPrincipalName": "String",
  "servicePrincipalName": "String",
  "ipAddress": "String",
  "userId": "String"
}
```



