---
title: acción wipeManagedAppRegistrationByDeviceTag
description: Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f597a33dff637a87a4071dadf1a4f16a6e7ef461
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974073"
---
# <a name="wipemanagedappregistrationbydevicetag-action"></a><span data-ttu-id="b72f6-103">acción wipeManagedAppRegistrationByDeviceTag</span><span class="sxs-lookup"><span data-stu-id="b72f6-103">wipeManagedAppRegistrationByDeviceTag action</span></span>

> <span data-ttu-id="b72f6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b72f6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b72f6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b72f6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b72f6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b72f6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b72f6-107">Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b72f6-107">Issues a wipe operation on an app registration with specified device tag.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b72f6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b72f6-108">Prerequisites</span></span>

<span data-ttu-id="b72f6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b72f6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b72f6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b72f6-111">Permission type</span></span>|<span data-ttu-id="b72f6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b72f6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b72f6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b72f6-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="b72f6-114">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="b72f6-114">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="b72f6-115">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b72f6-115">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b72f6-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b72f6-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b72f6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b72f6-117">Not supported.</span></span>|
|<span data-ttu-id="b72f6-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b72f6-118">Application</span></span>|<span data-ttu-id="b72f6-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b72f6-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b72f6-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b72f6-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/wipeManagedAppRegistrationByDeviceTag
```

## <a name="request-headers"></a><span data-ttu-id="b72f6-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b72f6-121">Request headers</span></span>

|<span data-ttu-id="b72f6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b72f6-122">Header</span></span>|<span data-ttu-id="b72f6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b72f6-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b72f6-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="b72f6-124">Authorization</span></span>|<span data-ttu-id="b72f6-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b72f6-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b72f6-126">Accept</span><span class="sxs-lookup"><span data-stu-id="b72f6-126">Accept</span></span>|<span data-ttu-id="b72f6-127">application/json</span><span class="sxs-lookup"><span data-stu-id="b72f6-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b72f6-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b72f6-128">Request body</span></span>

<span data-ttu-id="b72f6-129">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="b72f6-129">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="b72f6-130">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="b72f6-130">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="b72f6-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b72f6-131">Property</span></span>|<span data-ttu-id="b72f6-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="b72f6-132">Type</span></span>|<span data-ttu-id="b72f6-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="b72f6-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b72f6-134">deviceTag</span><span class="sxs-lookup"><span data-stu-id="b72f6-134">deviceTag</span></span>|<span data-ttu-id="b72f6-135">String</span><span class="sxs-lookup"><span data-stu-id="b72f6-135">String</span></span>|<span data-ttu-id="b72f6-136">etiqueta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b72f6-136">device tag</span></span>|

## <a name="response"></a><span data-ttu-id="b72f6-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b72f6-137">Response</span></span>

<span data-ttu-id="b72f6-138">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b72f6-138">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b72f6-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b72f6-139">Example</span></span>

### <a name="request"></a><span data-ttu-id="b72f6-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b72f6-140">Request</span></span>

<span data-ttu-id="b72f6-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b72f6-141">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/users/{usersId}/wipeManagedAppRegistrationByDeviceTag

Content-type: application/json
Content-length: 39

{
  "deviceTag": "Device Tag value"
}
```

### <a name="response"></a><span data-ttu-id="b72f6-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b72f6-142">Response</span></span>

<span data-ttu-id="b72f6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b72f6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```






