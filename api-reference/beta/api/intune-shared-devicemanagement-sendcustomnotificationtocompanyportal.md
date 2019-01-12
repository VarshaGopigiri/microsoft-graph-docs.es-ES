---
title: acción sendCustomNotificationToCompanyPortal
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7314f833fb5e11cdbf447b748a12634210c4d6f1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940515"
---
# <a name="sendcustomnotificationtocompanyportal-action"></a><span data-ttu-id="e7596-103">acción sendCustomNotificationToCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="e7596-103">sendCustomNotificationToCompanyPortal action</span></span>

> <span data-ttu-id="e7596-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e7596-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e7596-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e7596-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e7596-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e7596-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7596-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e7596-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e7596-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7596-108">Prerequisites</span></span>
<span data-ttu-id="e7596-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e7596-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e7596-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7596-111">Permission type</span></span>|<span data-ttu-id="e7596-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7596-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e7596-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7596-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="e7596-114">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="e7596-114">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="e7596-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7596-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="e7596-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7596-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e7596-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7596-117">Not supported.</span></span>|
|<span data-ttu-id="e7596-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7596-118">Application</span></span>|<span data-ttu-id="e7596-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e7596-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e7596-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7596-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/sendCustomNotificationToCompanyPortal
```

## <a name="request-headers"></a><span data-ttu-id="e7596-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7596-121">Request headers</span></span>
|<span data-ttu-id="e7596-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7596-122">Header</span></span>|<span data-ttu-id="e7596-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e7596-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e7596-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="e7596-124">Authorization</span></span>|<span data-ttu-id="e7596-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e7596-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e7596-126">Accept</span><span class="sxs-lookup"><span data-stu-id="e7596-126">Accept</span></span>|<span data-ttu-id="e7596-127">application/json</span><span class="sxs-lookup"><span data-stu-id="e7596-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e7596-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7596-128">Request body</span></span>
<span data-ttu-id="e7596-129">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="e7596-129">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="e7596-130">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="e7596-130">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="e7596-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7596-131">Property</span></span>|<span data-ttu-id="e7596-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7596-132">Type</span></span>|<span data-ttu-id="e7596-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7596-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7596-134">notificationTitle</span><span class="sxs-lookup"><span data-stu-id="e7596-134">notificationTitle</span></span>|<span data-ttu-id="e7596-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7596-135">String</span></span>|<span data-ttu-id="e7596-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e7596-136">Not yet documented</span></span>|
|<span data-ttu-id="e7596-137">notificationBody</span><span class="sxs-lookup"><span data-stu-id="e7596-137">notificationBody</span></span>|<span data-ttu-id="e7596-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="e7596-138">String</span></span>|<span data-ttu-id="e7596-139">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e7596-139">Not yet documented</span></span>|
|<span data-ttu-id="e7596-140">groupsToNotify</span><span class="sxs-lookup"><span data-stu-id="e7596-140">groupsToNotify</span></span>|<span data-ttu-id="e7596-141">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="e7596-141">String collection</span></span>|<span data-ttu-id="e7596-142">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e7596-142">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="e7596-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7596-143">Response</span></span>
<span data-ttu-id="e7596-144">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="e7596-144">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="e7596-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7596-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="e7596-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7596-146">Request</span></span>
<span data-ttu-id="e7596-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7596-147">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="e7596-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7596-148">Response</span></span>
<span data-ttu-id="e7596-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7596-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```






