---
title: Acción targetApps
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f9e7ceaa79021b1fe3dea5ff9fb0d0080201a3cd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887363"
---
# <a name="targetapps-action"></a><span data-ttu-id="fc3c5-103">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="fc3c5-103">targetApps action</span></span>

> <span data-ttu-id="fc3c5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fc3c5-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fc3c5-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fc3c5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fc3c5-106">Prerequisites</span></span>
<span data-ttu-id="fc3c5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc3c5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc3c5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc3c5-109">Permission type</span></span>|<span data-ttu-id="fc3c5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc3c5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fc3c5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc3c5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fc3c5-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc3c5-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="fc3c5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc3c5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fc3c5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-114">Not supported.</span></span>|
|<span data-ttu-id="fc3c5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc3c5-115">Application</span></span>|<span data-ttu-id="fc3c5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fc3c5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc3c5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/targetApps
```

## <a name="request-headers"></a><span data-ttu-id="fc3c5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc3c5-118">Request headers</span></span>
|<span data-ttu-id="fc3c5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc3c5-119">Header</span></span>|<span data-ttu-id="fc3c5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fc3c5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fc3c5-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fc3c5-121">Authorization</span></span>|<span data-ttu-id="fc3c5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fc3c5-123">Accept</span><span class="sxs-lookup"><span data-stu-id="fc3c5-123">Accept</span></span>|<span data-ttu-id="fc3c5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fc3c5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fc3c5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc3c5-125">Request body</span></span>
<span data-ttu-id="fc3c5-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="fc3c5-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="fc3c5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc3c5-128">Property</span></span>|<span data-ttu-id="fc3c5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc3c5-129">Type</span></span>|<span data-ttu-id="fc3c5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc3c5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fc3c5-131">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="fc3c5-131">apps</span></span>|<span data-ttu-id="fc3c5-132">Colección [managedMobileApp](../resources/intune-mam-managedmobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="fc3c5-132">[managedMobileApp](../resources/intune-mam-managedmobileapp.md) collection</span></span>|<span data-ttu-id="fc3c5-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fc3c5-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="fc3c5-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc3c5-134">Response</span></span>
<span data-ttu-id="fc3c5-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="fc3c5-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc3c5-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="fc3c5-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc3c5-137">Request</span></span>
<span data-ttu-id="fc3c5-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/targetApps

Content-type: application/json
Content-length: 286

{
  "apps": [
    {
      "@odata.type": "#microsoft.graph.managedMobileApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.mobileAppIdentifier"
      },
      "id": "0a129715-9715-0a12-1597-120a1597120a",
      "version": "Version value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="fc3c5-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc3c5-139">Response</span></span>
<span data-ttu-id="fc3c5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc3c5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



