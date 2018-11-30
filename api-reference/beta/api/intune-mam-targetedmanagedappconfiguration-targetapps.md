---
title: Acción targetApps
description: Todavía no documentado
ms.openlocfilehash: 51873703688c8731f41cd3ef85c30c9566477645
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083689"
---
# <a name="targetapps-action"></a><span data-ttu-id="95119-103">Acción targetApps</span><span class="sxs-lookup"><span data-stu-id="95119-103">targetApps action</span></span>

> <span data-ttu-id="95119-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="95119-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="95119-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="95119-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="95119-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="95119-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="95119-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="95119-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="95119-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="95119-108">Prerequisites</span></span>
<span data-ttu-id="95119-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="95119-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="95119-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="95119-111">Permission type</span></span>|<span data-ttu-id="95119-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="95119-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="95119-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="95119-113">Delegated (work or school account)</span></span>|<span data-ttu-id="95119-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="95119-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="95119-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="95119-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="95119-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="95119-116">Not supported.</span></span>|
|<span data-ttu-id="95119-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="95119-117">Application</span></span>|<span data-ttu-id="95119-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="95119-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="95119-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="95119-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/targetApps
```

## <a name="request-headers"></a><span data-ttu-id="95119-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="95119-120">Request headers</span></span>
|<span data-ttu-id="95119-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95119-121">Header</span></span>|<span data-ttu-id="95119-122">Valor</span><span class="sxs-lookup"><span data-stu-id="95119-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="95119-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="95119-123">Authorization</span></span>|<span data-ttu-id="95119-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="95119-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="95119-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="95119-125">Accept</span></span>|<span data-ttu-id="95119-126">application/json</span><span class="sxs-lookup"><span data-stu-id="95119-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="95119-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="95119-127">Request body</span></span>
<span data-ttu-id="95119-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="95119-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="95119-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="95119-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="95119-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95119-130">Property</span></span>|<span data-ttu-id="95119-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="95119-131">Type</span></span>|<span data-ttu-id="95119-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="95119-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="95119-133">aplicaciones</span><span class="sxs-lookup"><span data-stu-id="95119-133">apps</span></span>|<span data-ttu-id="95119-134">Colección [managedMobileApp](../resources/intune-mam-managedmobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="95119-134">[managedMobileApp](../resources/intune-mam-managedmobileapp.md) collection</span></span>|<span data-ttu-id="95119-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="95119-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="95119-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95119-136">Response</span></span>
<span data-ttu-id="95119-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="95119-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="95119-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95119-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="95119-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="95119-139">Request</span></span>
<span data-ttu-id="95119-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="95119-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/targetApps

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

### <a name="response"></a><span data-ttu-id="95119-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95119-141">Response</span></span>
<span data-ttu-id="95119-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="95119-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





