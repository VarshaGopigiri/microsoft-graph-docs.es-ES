---
title: acción assignedAccessMultiModeProfiles
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 24ab12236044c08ab17b50acb5d7cc486fadcafa
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358145"
---
# <a name="assignedaccessmultimodeprofiles-action"></a><span data-ttu-id="1d4bd-103">acción assignedAccessMultiModeProfiles</span><span class="sxs-lookup"><span data-stu-id="1d4bd-103">assignedAccessMultiModeProfiles action</span></span>

> <span data-ttu-id="1d4bd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d4bd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1d4bd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d4bd-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1d4bd-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1d4bd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d4bd-108">Prerequisites</span></span>
<span data-ttu-id="1d4bd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d4bd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d4bd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d4bd-111">Permission type</span></span>|<span data-ttu-id="1d4bd-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d4bd-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1d4bd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d4bd-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1d4bd-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1d4bd-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1d4bd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d4bd-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1d4bd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-116">Not supported.</span></span>|
|<span data-ttu-id="1d4bd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d4bd-117">Application</span></span>|<span data-ttu-id="1d4bd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1d4bd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d4bd-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/assignedAccessMultiModeProfiles
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration/assignedAccessMultiModeProfiles
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}/assignedAccessMultiModeProfiles
```

## <a name="request-headers"></a><span data-ttu-id="1d4bd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d4bd-120">Request headers</span></span>
|<span data-ttu-id="1d4bd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d4bd-121">Header</span></span>|<span data-ttu-id="1d4bd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1d4bd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1d4bd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1d4bd-123">Authorization</span></span>|<span data-ttu-id="1d4bd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1d4bd-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1d4bd-125">Accept</span></span>|<span data-ttu-id="1d4bd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1d4bd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d4bd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d4bd-127">Request body</span></span>
<span data-ttu-id="1d4bd-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="1d4bd-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="1d4bd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d4bd-130">Property</span></span>|<span data-ttu-id="1d4bd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d4bd-131">Type</span></span>|<span data-ttu-id="1d4bd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d4bd-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1d4bd-133">assignedAccessMultiModeProfiles</span><span class="sxs-lookup"><span data-stu-id="1d4bd-133">assignedAccessMultiModeProfiles</span></span>|<span data-ttu-id="1d4bd-134">colección de [windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md)</span><span class="sxs-lookup"><span data-stu-id="1d4bd-134">[windowsAssignedAccessProfile](../resources/intune-deviceconfig-windowsassignedaccessprofile.md) collection</span></span>|<span data-ttu-id="1d4bd-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1d4bd-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="1d4bd-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d4bd-136">Response</span></span>
<span data-ttu-id="1d4bd-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="1d4bd-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d4bd-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="1d4bd-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d4bd-139">Request</span></span>
<span data-ttu-id="1d4bd-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-140">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="1d4bd-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d4bd-141">Response</span></span>
<span data-ttu-id="1d4bd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d4bd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





