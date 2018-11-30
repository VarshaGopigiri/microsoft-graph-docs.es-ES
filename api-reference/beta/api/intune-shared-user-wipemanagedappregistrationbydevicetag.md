---
title: acción wipeManagedAppRegistrationByDeviceTag
description: Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.
ms.openlocfilehash: 7ea037eecb0a581dd55d212fe541391f24d0819f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090891"
---
# <a name="wipemanagedappregistrationbydevicetag-action"></a><span data-ttu-id="f5986-103">acción wipeManagedAppRegistrationByDeviceTag</span><span class="sxs-lookup"><span data-stu-id="f5986-103">wipeManagedAppRegistrationByDeviceTag action</span></span>

> <span data-ttu-id="f5986-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f5986-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f5986-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f5986-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f5986-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f5986-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f5986-107">Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f5986-107">Issues a wipe operation on an app registration with specified device tag.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f5986-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f5986-108">Prerequisites</span></span>

<span data-ttu-id="f5986-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5986-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f5986-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5986-111">Permission type</span></span>|<span data-ttu-id="f5986-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5986-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f5986-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5986-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="f5986-114">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="f5986-114">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="f5986-115">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f5986-115">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f5986-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5986-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f5986-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5986-117">Not supported.</span></span>|
|<span data-ttu-id="f5986-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5986-118">Application</span></span>|<span data-ttu-id="f5986-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5986-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f5986-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5986-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/wipeManagedAppRegistrationByDeviceTag
```

## <a name="request-headers"></a><span data-ttu-id="f5986-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5986-121">Request headers</span></span>

|<span data-ttu-id="f5986-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5986-122">Header</span></span>|<span data-ttu-id="f5986-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f5986-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f5986-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5986-124">Authorization</span></span>|<span data-ttu-id="f5986-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f5986-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f5986-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f5986-126">Accept</span></span>|<span data-ttu-id="f5986-127">application/json</span><span class="sxs-lookup"><span data-stu-id="f5986-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f5986-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5986-128">Request body</span></span>

<span data-ttu-id="f5986-129">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="f5986-129">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="f5986-130">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="f5986-130">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="f5986-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f5986-131">Property</span></span>|<span data-ttu-id="f5986-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5986-132">Type</span></span>|<span data-ttu-id="f5986-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5986-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f5986-134">deviceTag</span><span class="sxs-lookup"><span data-stu-id="f5986-134">deviceTag</span></span>|<span data-ttu-id="f5986-135">String</span><span class="sxs-lookup"><span data-stu-id="f5986-135">String</span></span>|<span data-ttu-id="f5986-136">etiqueta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f5986-136">device tag</span></span>|

## <a name="response"></a><span data-ttu-id="f5986-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5986-137">Response</span></span>

<span data-ttu-id="f5986-138">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f5986-138">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f5986-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5986-139">Example</span></span>

### <a name="request"></a><span data-ttu-id="f5986-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5986-140">Request</span></span>

<span data-ttu-id="f5986-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5986-141">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/users/{usersId}/wipeManagedAppRegistrationByDeviceTag

Content-type: application/json
Content-length: 39

{
  "deviceTag": "Device Tag value"
}
```

### <a name="response"></a><span data-ttu-id="f5986-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5986-142">Response</span></span>

<span data-ttu-id="f5986-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f5986-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```






