---
title: acción assignedAccessMultiModeProfiles
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 09183d5328b7dbbc92fa6052990e71b40df838ff
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828080"
---
# <a name="assignedaccessmultimodeprofiles-action"></a><span data-ttu-id="aa384-103">acción assignedAccessMultiModeProfiles</span><span class="sxs-lookup"><span data-stu-id="aa384-103">assignedAccessMultiModeProfiles action</span></span>

> <span data-ttu-id="aa384-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aa384-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aa384-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aa384-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="aa384-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aa384-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aa384-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="aa384-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aa384-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aa384-108">Prerequisites</span></span>
<span data-ttu-id="aa384-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa384-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aa384-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa384-111">Permission type</span></span>|<span data-ttu-id="aa384-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa384-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="aa384-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa384-113">Delegated (work or school account)</span></span>|<span data-ttu-id="aa384-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="aa384-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="aa384-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa384-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="aa384-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa384-116">Not supported.</span></span>|
|<span data-ttu-id="aa384-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa384-117">Application</span></span>|<span data-ttu-id="aa384-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa384-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="aa384-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa384-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignedAccessMultiModeProfiles
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration/assignedAccessMultiModeProfiles
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}/assignedAccessMultiModeProfiles
```

## <a name="request-headers"></a><span data-ttu-id="aa384-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa384-120">Request headers</span></span>
|<span data-ttu-id="aa384-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa384-121">Header</span></span>|<span data-ttu-id="aa384-122">Valor</span><span class="sxs-lookup"><span data-stu-id="aa384-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="aa384-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="aa384-123">Authorization</span></span>|<span data-ttu-id="aa384-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="aa384-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="aa384-125">Accept</span><span class="sxs-lookup"><span data-stu-id="aa384-125">Accept</span></span>|<span data-ttu-id="aa384-126">application/json</span><span class="sxs-lookup"><span data-stu-id="aa384-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="aa384-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa384-127">Request body</span></span>
<span data-ttu-id="aa384-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="aa384-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="aa384-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="aa384-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="aa384-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa384-130">Property</span></span>|<span data-ttu-id="aa384-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa384-131">Type</span></span>|<span data-ttu-id="aa384-132">Description</span><span class="sxs-lookup"><span data-stu-id="aa384-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aa384-133">assignedAccessMultiModeProfiles</span><span class="sxs-lookup"><span data-stu-id="aa384-133">assignedAccessMultiModeProfiles</span></span>|<span data-ttu-id="aa384-134">colección de [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md)</span><span class="sxs-lookup"><span data-stu-id="aa384-134">[windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) collection</span></span>|<span data-ttu-id="aa384-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="aa384-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="aa384-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa384-136">Response</span></span>
<span data-ttu-id="aa384-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="aa384-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="aa384-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa384-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="aa384-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa384-139">Request</span></span>
<span data-ttu-id="aa384-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa384-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignedAccessMultiModeProfiles

Content-type: application/json
Content-length: 528

{
  "assignedAccessMultiModeProfiles": [
    {
      "@odata.type": "#microsoft.graph.windowsAssignedAccessProfile",
      "id": "cfa70299-0299-cfa7-9902-a7cf9902a7cf",
      "profileName": "Profile Name value",
      "showTaskBar": true,
      "appUserModelIds": [
        "App User Model Ids value"
      ],
      "desktopAppPaths": [
        "Desktop App Paths value"
      ],
      "userAccounts": [
        "User Accounts value"
      ],
      "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="aa384-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa384-141">Response</span></span>
<span data-ttu-id="aa384-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa384-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





