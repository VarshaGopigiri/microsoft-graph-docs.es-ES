---
title: Obtener usuario
description: Lea las propiedades y las relaciones del objeto user.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4bca90bc1e42b6dde596d22d2bd1e42dcc5910db
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979470"
---
# <a name="get-user"></a><span data-ttu-id="8c1e2-103">Obtener usuario</span><span class="sxs-lookup"><span data-stu-id="8c1e2-103">Get user</span></span>

> <span data-ttu-id="8c1e2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8c1e2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8c1e2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8c1e2-107">Lea las propiedades y las relaciones del objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="8c1e2-107">Read properties and relationships of the [user](../resources/intune-shared-user.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8c1e2-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8c1e2-108">Prerequisites</span></span>

<span data-ttu-id="8c1e2-109">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="8c1e2-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8c1e2-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="8c1e2-111">El permiso específico depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-111">The specific permission depends on the context.</span></span>

|<span data-ttu-id="8c1e2-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8c1e2-112">Permission type</span></span>|<span data-ttu-id="8c1e2-113">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8c1e2-113">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8c1e2-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8c1e2-114">Delegated (work or school account)</span></span>||
| <span data-ttu-id="8c1e2-115">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="8c1e2-115">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="8c1e2-116">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="8c1e2-116">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="8c1e2-117">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="8c1e2-117">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="8c1e2-118">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="8c1e2-118">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="8c1e2-119">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="8c1e2-119">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="8c1e2-120">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="8c1e2-120">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="8c1e2-121">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="8c1e2-121">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="8c1e2-122">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="8c1e2-122">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="8c1e2-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8c1e2-123">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8c1e2-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-124">Not supported.</span></span>|
|<span data-ttu-id="8c1e2-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8c1e2-125">Application</span></span>|<span data-ttu-id="8c1e2-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-126">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8c1e2-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c1e2-127">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8c1e2-128">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8c1e2-128">Optional query parameters</span></span>

<span data-ttu-id="8c1e2-129">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-129">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8c1e2-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c1e2-130">Request headers</span></span>

|<span data-ttu-id="8c1e2-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c1e2-131">Header</span></span>|<span data-ttu-id="8c1e2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8c1e2-132">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8c1e2-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="8c1e2-133">Authorization</span></span>|<span data-ttu-id="8c1e2-134">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-134">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8c1e2-135">Accept</span><span class="sxs-lookup"><span data-stu-id="8c1e2-135">Accept</span></span>|<span data-ttu-id="8c1e2-136">application/json</span><span class="sxs-lookup"><span data-stu-id="8c1e2-136">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8c1e2-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8c1e2-137">Request body</span></span>

<span data-ttu-id="8c1e2-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8c1e2-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c1e2-139">Response</span></span>

<span data-ttu-id="8c1e2-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-140">If successful, this method returns a `200 OK` response code and [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8c1e2-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c1e2-141">Example</span></span>

### <a name="request"></a><span data-ttu-id="8c1e2-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c1e2-142">Request</span></span>

<span data-ttu-id="8c1e2-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-143">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="8c1e2-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c1e2-144">Response</span></span>

<span data-ttu-id="8c1e2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8c1e2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 118

{
  "value": {
    "@odata.type": "#microsoft.graph.user",
    "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
  }
}
```



