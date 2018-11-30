---
title: Acción wipeManagedAppRegistrationsByDeviceTag
description: Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.
ms.openlocfilehash: d6f56fa50b3162ecaebc0bb1adb02af3b4b0e9f6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031140"
---
# <a name="wipemanagedappregistrationsbydevicetag-action"></a><span data-ttu-id="e228b-103">Acción wipeManagedAppRegistrationsByDeviceTag</span><span class="sxs-lookup"><span data-stu-id="e228b-103">wipeManagedAppRegistrationsByDeviceTag action</span></span>



> <span data-ttu-id="e228b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e228b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e228b-105">Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e228b-105">Issues a wipe operation on an app registration with specified device tag.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e228b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e228b-106">Prerequisites</span></span>
<span data-ttu-id="e228b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e228b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e228b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e228b-109">Permission type</span></span>|<span data-ttu-id="e228b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e228b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e228b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e228b-111">Delegated (work or school account)</span></span>| <span data-ttu-id="e228b-112">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="e228b-112">_varies by context_</span></span> |
| <span data-ttu-id="e228b-113">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="e228b-113">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="e228b-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e228b-114">DeviceManagementApps.ReadWrite.All</span></span> |
|<span data-ttu-id="e228b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e228b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e228b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e228b-116">Not supported.</span></span>|
|<span data-ttu-id="e228b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e228b-117">Application</span></span>|<span data-ttu-id="e228b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e228b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e228b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e228b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/wipeManagedAppRegistrationsByDeviceTag
```

## <a name="request-headers"></a><span data-ttu-id="e228b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e228b-120">Request headers</span></span>
|<span data-ttu-id="e228b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e228b-121">Header</span></span>|<span data-ttu-id="e228b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e228b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e228b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e228b-123">Authorization</span></span>|<span data-ttu-id="e228b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e228b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e228b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e228b-125">Accept</span></span>|<span data-ttu-id="e228b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e228b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e228b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e228b-127">Request body</span></span>
<span data-ttu-id="e228b-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="e228b-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="e228b-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="e228b-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="e228b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e228b-130">Property</span></span>|<span data-ttu-id="e228b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e228b-131">Type</span></span>|<span data-ttu-id="e228b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e228b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e228b-133">deviceTag</span><span class="sxs-lookup"><span data-stu-id="e228b-133">deviceTag</span></span>|<span data-ttu-id="e228b-134">String</span><span class="sxs-lookup"><span data-stu-id="e228b-134">String</span></span>|<span data-ttu-id="e228b-135">etiqueta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e228b-135">device tag</span></span>|

## <a name="response"></a><span data-ttu-id="e228b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e228b-136">Response</span></span>
<span data-ttu-id="e228b-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="e228b-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="e228b-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e228b-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="e228b-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e228b-139">Request</span></span>
<span data-ttu-id="e228b-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e228b-140">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/users/{usersId}/wipeManagedAppRegistrationsByDeviceTag

Content-type: application/json
Content-length: 39

{
  "deviceTag": "Device Tag value"
}
```

### <a name="response"></a><span data-ttu-id="e228b-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e228b-141">Response</span></span>
<span data-ttu-id="e228b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e228b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



