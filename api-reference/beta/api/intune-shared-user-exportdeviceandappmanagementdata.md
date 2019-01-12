---
title: exportDeviceAndAppManagementData (función)
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5ab337ccca261dde98d609434fa7948bc07bcfca
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965113"
---
# <a name="exportdeviceandappmanagementdata-function"></a><span data-ttu-id="b4502-103">exportDeviceAndAppManagementData (función)</span><span class="sxs-lookup"><span data-stu-id="b4502-103">exportDeviceAndAppManagementData function</span></span>

> <span data-ttu-id="b4502-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b4502-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b4502-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b4502-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b4502-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b4502-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b4502-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b4502-107">Not yet documented</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b4502-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b4502-108">Prerequisites</span></span>

<span data-ttu-id="b4502-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b4502-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b4502-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4502-111">Permission type</span></span>|<span data-ttu-id="b4502-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4502-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b4502-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4502-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="b4502-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="b4502-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="b4502-115">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4502-115">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="b4502-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4502-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b4502-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4502-117">Not supported.</span></span>|
|<span data-ttu-id="b4502-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4502-118">Application</span></span>|<span data-ttu-id="b4502-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4502-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b4502-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4502-120">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/exportDeviceAndAppManagementData
```

## <a name="request-headers"></a><span data-ttu-id="b4502-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b4502-121">Request headers</span></span>

|<span data-ttu-id="b4502-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4502-122">Header</span></span>|<span data-ttu-id="b4502-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b4502-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b4502-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="b4502-124">Authorization</span></span>|<span data-ttu-id="b4502-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b4502-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b4502-126">Accept</span><span class="sxs-lookup"><span data-stu-id="b4502-126">Accept</span></span>|<span data-ttu-id="b4502-127">application/json</span><span class="sxs-lookup"><span data-stu-id="b4502-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b4502-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4502-128">Request body</span></span>

<span data-ttu-id="b4502-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="b4502-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="b4502-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4502-130">Property</span></span>|<span data-ttu-id="b4502-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4502-131">Type</span></span>|<span data-ttu-id="b4502-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4502-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b4502-133">skip</span><span class="sxs-lookup"><span data-stu-id="b4502-133">skip</span></span>|<span data-ttu-id="b4502-134">Int32</span><span class="sxs-lookup"><span data-stu-id="b4502-134">Int32</span></span>|<span data-ttu-id="b4502-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b4502-135">Not yet documented</span></span>|
|<span data-ttu-id="b4502-136">top</span><span class="sxs-lookup"><span data-stu-id="b4502-136">top</span></span>|<span data-ttu-id="b4502-137">Int32</span><span class="sxs-lookup"><span data-stu-id="b4502-137">Int32</span></span>|<span data-ttu-id="b4502-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b4502-138">Not yet documented</span></span>|

## <a name="response"></a><span data-ttu-id="b4502-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4502-139">Response</span></span>

<span data-ttu-id="b4502-140">Si tiene éxito, esta función devuelve una `200 OK` código de respuesta y un [deviceAndAppManagementData](../resources/intune-onboarding-deviceandappmanagementdata.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4502-140">If successful, this function returns a `200 OK` response code and a [deviceAndAppManagementData](../resources/intune-onboarding-deviceandappmanagementdata.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b4502-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4502-141">Example</span></span>

### <a name="request"></a><span data-ttu-id="b4502-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4502-142">Request</span></span>

<span data-ttu-id="b4502-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b4502-143">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/users/{usersId}/exportDeviceAndAppManagementData(skip=4,top=3)
```

### <a name="response"></a><span data-ttu-id="b4502-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4502-144">Response</span></span>

<span data-ttu-id="b4502-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4502-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 143

{
  "value": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementData",
    "content": "<Unknown Primitive Type Edm.Stream>"
  }
}
```



