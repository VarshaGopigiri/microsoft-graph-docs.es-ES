---
title: acción sendCustomNotificationToCompanyPortal
description: Todavía no documentado
ms.openlocfilehash: bf19f87c385568a38407fff0df144c6df165fbc0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085720"
---
# <a name="sendcustomnotificationtocompanyportal-action"></a><span data-ttu-id="606ea-103">acción sendCustomNotificationToCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="606ea-103">sendCustomNotificationToCompanyPortal action</span></span>

> <span data-ttu-id="606ea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="606ea-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="606ea-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="606ea-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="606ea-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="606ea-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="606ea-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="606ea-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="606ea-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="606ea-108">Prerequisites</span></span>
<span data-ttu-id="606ea-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="606ea-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="606ea-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="606ea-111">Permission type</span></span>|<span data-ttu-id="606ea-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="606ea-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="606ea-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="606ea-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="606ea-114">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="606ea-114">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="606ea-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="606ea-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="606ea-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="606ea-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="606ea-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="606ea-117">Not supported.</span></span>|
|<span data-ttu-id="606ea-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="606ea-118">Application</span></span>|<span data-ttu-id="606ea-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="606ea-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="606ea-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="606ea-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/sendCustomNotificationToCompanyPortal
```

## <a name="request-headers"></a><span data-ttu-id="606ea-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="606ea-121">Request headers</span></span>
|<span data-ttu-id="606ea-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="606ea-122">Header</span></span>|<span data-ttu-id="606ea-123">Valor</span><span class="sxs-lookup"><span data-stu-id="606ea-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="606ea-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="606ea-124">Authorization</span></span>|<span data-ttu-id="606ea-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="606ea-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="606ea-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="606ea-126">Accept</span></span>|<span data-ttu-id="606ea-127">application/json</span><span class="sxs-lookup"><span data-stu-id="606ea-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="606ea-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="606ea-128">Request body</span></span>
<span data-ttu-id="606ea-129">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="606ea-129">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="606ea-130">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="606ea-130">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="606ea-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="606ea-131">Property</span></span>|<span data-ttu-id="606ea-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="606ea-132">Type</span></span>|<span data-ttu-id="606ea-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="606ea-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="606ea-134">notificationTitle</span><span class="sxs-lookup"><span data-stu-id="606ea-134">notificationTitle</span></span>|<span data-ttu-id="606ea-135">String</span><span class="sxs-lookup"><span data-stu-id="606ea-135">String</span></span>|<span data-ttu-id="606ea-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="606ea-136">Not yet documented</span></span>|
|<span data-ttu-id="606ea-137">notificationBody</span><span class="sxs-lookup"><span data-stu-id="606ea-137">notificationBody</span></span>|<span data-ttu-id="606ea-138">String</span><span class="sxs-lookup"><span data-stu-id="606ea-138">String</span></span>|<span data-ttu-id="606ea-139">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="606ea-139">Not yet documented</span></span>|
|<span data-ttu-id="606ea-140">groupsToNotify</span><span class="sxs-lookup"><span data-stu-id="606ea-140">groupsToNotify</span></span>|<span data-ttu-id="606ea-141">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="606ea-141">String collection</span></span>|<span data-ttu-id="606ea-142">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="606ea-142">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="606ea-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="606ea-143">Response</span></span>
<span data-ttu-id="606ea-144">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="606ea-144">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="606ea-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="606ea-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="606ea-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="606ea-146">Request</span></span>
<span data-ttu-id="606ea-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="606ea-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/sendCustomNotificationToCompanyPortal

Content-type: application/json
Content-length: 164

{
  "notificationTitle": "Notification Title value",
  "notificationBody": "Notification Body value",
  "groupsToNotify": [
    "Groups To Notify value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="606ea-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="606ea-148">Response</span></span>
<span data-ttu-id="606ea-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="606ea-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






