---
title: Tipo de recurso auditActor
description: Una clase que contiene las propiedades del actor de auditoría.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 14b4ce53d46897a84da8fab468ba2ad6aa99b30e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820051"
---
# <a name="auditactor-resource-type"></a><span data-ttu-id="20d18-103">Tipo de recurso auditActor</span><span class="sxs-lookup"><span data-stu-id="20d18-103">auditActor resource type</span></span>

> <span data-ttu-id="20d18-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="20d18-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="20d18-105">Una clase que contiene las propiedades del actor de auditoría.</span><span class="sxs-lookup"><span data-stu-id="20d18-105">A class containing the properties for Audit Actor.</span></span>
## <a name="properties"></a><span data-ttu-id="20d18-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20d18-106">Properties</span></span>
|<span data-ttu-id="20d18-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="20d18-107">Property</span></span>|<span data-ttu-id="20d18-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="20d18-108">Type</span></span>|<span data-ttu-id="20d18-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="20d18-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="20d18-110">type</span><span class="sxs-lookup"><span data-stu-id="20d18-110">type</span></span>|<span data-ttu-id="20d18-111">cadena</span><span class="sxs-lookup"><span data-stu-id="20d18-111">String</span></span>|<span data-ttu-id="20d18-112">Tipo de actor.</span><span class="sxs-lookup"><span data-stu-id="20d18-112">Actor Type.</span></span>|
|<span data-ttu-id="20d18-113">userPermissions</span><span class="sxs-lookup"><span data-stu-id="20d18-113">userPermissions</span></span>|<span data-ttu-id="20d18-114">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="20d18-114">String collection</span></span>|<span data-ttu-id="20d18-115">Lista de los permisos de usuario cuando se ha realizado la auditoría.</span><span class="sxs-lookup"><span data-stu-id="20d18-115">List of user permissions when the audit was performed.</span></span>|
|<span data-ttu-id="20d18-116">applicationId</span><span class="sxs-lookup"><span data-stu-id="20d18-116">applicationId</span></span>|<span data-ttu-id="20d18-117">cadena</span><span class="sxs-lookup"><span data-stu-id="20d18-117">String</span></span>|<span data-ttu-id="20d18-118">Id. de aplicación de AAD</span><span class="sxs-lookup"><span data-stu-id="20d18-118">AAD Application Id.</span></span>|
|<span data-ttu-id="20d18-119">applicationDisplayName</span><span class="sxs-lookup"><span data-stu-id="20d18-119">applicationDisplayName</span></span>|<span data-ttu-id="20d18-120">cadena</span><span class="sxs-lookup"><span data-stu-id="20d18-120">String</span></span>|<span data-ttu-id="20d18-121">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="20d18-121">Name of the Application.</span></span>|
|<span data-ttu-id="20d18-122">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="20d18-122">userPrincipalName</span></span>|<span data-ttu-id="20d18-123">cadena</span><span class="sxs-lookup"><span data-stu-id="20d18-123">String</span></span>|<span data-ttu-id="20d18-124">Nombre principal de usuario (UPN).</span><span class="sxs-lookup"><span data-stu-id="20d18-124">User Principal Name (UPN).</span></span>|
|<span data-ttu-id="20d18-125">servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="20d18-125">servicePrincipalName</span></span>|<span data-ttu-id="20d18-126">cadena</span><span class="sxs-lookup"><span data-stu-id="20d18-126">String</span></span>|<span data-ttu-id="20d18-127">Nombre de entidad de seguridad de servicio (SPN).</span><span class="sxs-lookup"><span data-stu-id="20d18-127">Service Principal Name (SPN).</span></span>|
|<span data-ttu-id="20d18-128">ipAddress</span><span class="sxs-lookup"><span data-stu-id="20d18-128">ipAddress</span></span>|<span data-ttu-id="20d18-129">cadena</span><span class="sxs-lookup"><span data-stu-id="20d18-129">String</span></span>|<span data-ttu-id="20d18-130">IPAddress.</span><span class="sxs-lookup"><span data-stu-id="20d18-130">IPAddress.</span></span>|
|<span data-ttu-id="20d18-131">userId</span><span class="sxs-lookup"><span data-stu-id="20d18-131">userId</span></span>|<span data-ttu-id="20d18-132">cadena</span><span class="sxs-lookup"><span data-stu-id="20d18-132">String</span></span>|<span data-ttu-id="20d18-133">Id. de usuario.</span><span class="sxs-lookup"><span data-stu-id="20d18-133">User Id.</span></span>|

## <a name="relationships"></a><span data-ttu-id="20d18-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="20d18-134">Relationships</span></span>
<span data-ttu-id="20d18-135">Ninguna</span><span class="sxs-lookup"><span data-stu-id="20d18-135">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="20d18-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="20d18-136">JSON Representation</span></span>
<span data-ttu-id="20d18-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="20d18-137">Here is a JSON representation of the resource.</span></span>
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



