---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 019abecc0f9d7560f907652166f8e2ba54cfa2c3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974753"
---
# <a name="assign-action"></a><span data-ttu-id="7d027-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="7d027-103">assign action</span></span>

> <span data-ttu-id="7d027-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7d027-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7d027-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7d027-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7d027-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7d027-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7d027-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7d027-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7d027-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7d027-108">Prerequisites</span></span>
<span data-ttu-id="7d027-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d027-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7d027-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d027-111">Permission type</span></span>|<span data-ttu-id="7d027-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d027-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7d027-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d027-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7d027-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d027-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="7d027-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d027-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7d027-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7d027-116">Not supported.</span></span>|
|<span data-ttu-id="7d027-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d027-117">Application</span></span>|<span data-ttu-id="7d027-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7d027-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7d027-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d027-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="7d027-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d027-120">Request headers</span></span>
|<span data-ttu-id="7d027-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d027-121">Header</span></span>|<span data-ttu-id="7d027-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7d027-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7d027-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7d027-123">Authorization</span></span>|<span data-ttu-id="7d027-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7d027-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7d027-125">Accept</span><span class="sxs-lookup"><span data-stu-id="7d027-125">Accept</span></span>|<span data-ttu-id="7d027-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7d027-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7d027-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d027-127">Request body</span></span>
<span data-ttu-id="7d027-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="7d027-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="7d027-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="7d027-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="7d027-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d027-130">Property</span></span>|<span data-ttu-id="7d027-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d027-131">Type</span></span>|<span data-ttu-id="7d027-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d027-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7d027-133">asignaciones</span><span class="sxs-lookup"><span data-stu-id="7d027-133">assignments</span></span>|<span data-ttu-id="7d027-134">Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="7d027-134">[managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md) collection</span></span>|<span data-ttu-id="7d027-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7d027-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="7d027-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d027-136">Response</span></span>
<span data-ttu-id="7d027-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="7d027-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="7d027-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d027-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="7d027-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d027-139">Request</span></span>
<span data-ttu-id="7d027-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d027-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/assign

Content-type: application/json
Content-length: 293

{
  "assignments": [
    {
      "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationAssignment",
      "id": "4df81c9c-1c9c-4df8-9c1c-f84d9c1cf84d",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="7d027-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d027-141">Response</span></span>
<span data-ttu-id="7d027-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7d027-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





