---
title: Tipo de recurso auditActor
description: Una clase que contiene las propiedades del actor de auditoría.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4c6dddd2863f881c026eb848c643bdc55cbbb372
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873916"
---
# <a name="auditactor-resource-type"></a><span data-ttu-id="8cb16-103">Tipo de recurso auditActor</span><span class="sxs-lookup"><span data-stu-id="8cb16-103">auditActor resource type</span></span>

> <span data-ttu-id="8cb16-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8cb16-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8cb16-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8cb16-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8cb16-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8cb16-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8cb16-107">Una clase que contiene las propiedades del actor de auditoría.</span><span class="sxs-lookup"><span data-stu-id="8cb16-107">A class containing the properties for Audit Actor.</span></span>
## <a name="properties"></a><span data-ttu-id="8cb16-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8cb16-108">Properties</span></span>
|<span data-ttu-id="8cb16-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8cb16-109">Property</span></span>|<span data-ttu-id="8cb16-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8cb16-110">Type</span></span>|<span data-ttu-id="8cb16-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cb16-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8cb16-112">type</span><span class="sxs-lookup"><span data-stu-id="8cb16-112">type</span></span>|<span data-ttu-id="8cb16-113">cadena</span><span class="sxs-lookup"><span data-stu-id="8cb16-113">String</span></span>|<span data-ttu-id="8cb16-114">Tipo de actor.</span><span class="sxs-lookup"><span data-stu-id="8cb16-114">Actor Type.</span></span>|
|<span data-ttu-id="8cb16-115">userPermissions</span><span class="sxs-lookup"><span data-stu-id="8cb16-115">userPermissions</span></span>|<span data-ttu-id="8cb16-116">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="8cb16-116">String collection</span></span>|<span data-ttu-id="8cb16-117">Lista de los permisos de usuario cuando se ha realizado la auditoría.</span><span class="sxs-lookup"><span data-stu-id="8cb16-117">List of user permissions when the audit was performed.</span></span>|
|<span data-ttu-id="8cb16-118">applicationId</span><span class="sxs-lookup"><span data-stu-id="8cb16-118">applicationId</span></span>|<span data-ttu-id="8cb16-119">cadena</span><span class="sxs-lookup"><span data-stu-id="8cb16-119">String</span></span>|<span data-ttu-id="8cb16-120">Id. de aplicación de AAD</span><span class="sxs-lookup"><span data-stu-id="8cb16-120">AAD Application Id.</span></span>|
|<span data-ttu-id="8cb16-121">applicationDisplayName</span><span class="sxs-lookup"><span data-stu-id="8cb16-121">applicationDisplayName</span></span>|<span data-ttu-id="8cb16-122">cadena</span><span class="sxs-lookup"><span data-stu-id="8cb16-122">String</span></span>|<span data-ttu-id="8cb16-123">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cb16-123">Name of the Application.</span></span>|
|<span data-ttu-id="8cb16-124">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8cb16-124">userPrincipalName</span></span>|<span data-ttu-id="8cb16-125">cadena</span><span class="sxs-lookup"><span data-stu-id="8cb16-125">String</span></span>|<span data-ttu-id="8cb16-126">Nombre principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="8cb16-126">User Principal Name (UPN).</span></span>|
|<span data-ttu-id="8cb16-127">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8cb16-127">servicePrincipalName</span></span>|<span data-ttu-id="8cb16-128">cadena</span><span class="sxs-lookup"><span data-stu-id="8cb16-128">String</span></span>|<span data-ttu-id="8cb16-129">Nombre de entidad de seguridad de servicio (SPN).</span><span class="sxs-lookup"><span data-stu-id="8cb16-129">Service Principal Name (SPN).</span></span>|
|<span data-ttu-id="8cb16-130">ipAddress</span><span class="sxs-lookup"><span data-stu-id="8cb16-130">ipAddress</span></span>|<span data-ttu-id="8cb16-131">cadena</span><span class="sxs-lookup"><span data-stu-id="8cb16-131">String</span></span>|<span data-ttu-id="8cb16-132">IPAddress.</span><span class="sxs-lookup"><span data-stu-id="8cb16-132">IPAddress.</span></span>|
|<span data-ttu-id="8cb16-133">userId</span><span class="sxs-lookup"><span data-stu-id="8cb16-133">userId</span></span>|<span data-ttu-id="8cb16-134">cadena</span><span class="sxs-lookup"><span data-stu-id="8cb16-134">String</span></span>|<span data-ttu-id="8cb16-135">Id. de usuario.</span><span class="sxs-lookup"><span data-stu-id="8cb16-135">User Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8cb16-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8cb16-136">Relationships</span></span>
<span data-ttu-id="8cb16-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8cb16-137">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8cb16-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8cb16-138">JSON Representation</span></span>
<span data-ttu-id="8cb16-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8cb16-139">Here is a JSON representation of the resource.</span></span>
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





