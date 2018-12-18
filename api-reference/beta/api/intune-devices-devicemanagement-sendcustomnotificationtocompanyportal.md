---
title: acción sendCustomNotificationToCompanyPortal
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 549aff553416e6e8c5fa03382b7a4e513a4ede83
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305246"
---
# <a name="sendcustomnotificationtocompanyportal-action"></a><span data-ttu-id="b5306-103">acción sendCustomNotificationToCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="b5306-103">sendCustomNotificationToCompanyPortal action</span></span>

> <span data-ttu-id="b5306-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b5306-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b5306-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b5306-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b5306-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b5306-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b5306-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b5306-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b5306-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b5306-108">Prerequisites</span></span>
<span data-ttu-id="b5306-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b5306-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b5306-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b5306-111">Permission type</span></span>|<span data-ttu-id="b5306-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b5306-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b5306-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b5306-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b5306-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b5306-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="b5306-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b5306-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b5306-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5306-116">Not supported.</span></span>|
|<span data-ttu-id="b5306-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b5306-117">Application</span></span>|<span data-ttu-id="b5306-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5306-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b5306-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5306-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/sendCustomNotificationToCompanyPortal
```

## <a name="request-headers"></a><span data-ttu-id="b5306-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5306-120">Request headers</span></span>
|<span data-ttu-id="b5306-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5306-121">Header</span></span>|<span data-ttu-id="b5306-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b5306-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b5306-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b5306-123">Authorization</span></span>|<span data-ttu-id="b5306-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b5306-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b5306-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b5306-125">Accept</span></span>|<span data-ttu-id="b5306-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b5306-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b5306-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5306-127">Request body</span></span>
<span data-ttu-id="b5306-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="b5306-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="b5306-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="b5306-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="b5306-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5306-130">Property</span></span>|<span data-ttu-id="b5306-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5306-131">Type</span></span>|<span data-ttu-id="b5306-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5306-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b5306-133">notificationTitle</span><span class="sxs-lookup"><span data-stu-id="b5306-133">notificationTitle</span></span>|<span data-ttu-id="b5306-134">String</span><span class="sxs-lookup"><span data-stu-id="b5306-134">String</span></span>|<span data-ttu-id="b5306-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b5306-135">Not yet documented</span></span>|
|<span data-ttu-id="b5306-136">notificationBody</span><span class="sxs-lookup"><span data-stu-id="b5306-136">notificationBody</span></span>|<span data-ttu-id="b5306-137">String</span><span class="sxs-lookup"><span data-stu-id="b5306-137">String</span></span>|<span data-ttu-id="b5306-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b5306-138">Not yet documented</span></span>|
|<span data-ttu-id="b5306-139">groupsToNotify</span><span class="sxs-lookup"><span data-stu-id="b5306-139">groupsToNotify</span></span>|<span data-ttu-id="b5306-140">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="b5306-140">String collection</span></span>|<span data-ttu-id="b5306-141">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b5306-141">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="b5306-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5306-142">Response</span></span>
<span data-ttu-id="b5306-143">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b5306-143">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b5306-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5306-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="b5306-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b5306-145">Request</span></span>
<span data-ttu-id="b5306-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5306-146">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="b5306-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5306-147">Response</span></span>
<span data-ttu-id="b5306-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b5306-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





