---
title: Obtener usuario
description: Lea las propiedades y las relaciones del objeto user.
ms.openlocfilehash: 619f35e5b7e8ffd75a8bcd2db32122dd69a9ac2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031189"
---
# <a name="get-user"></a><span data-ttu-id="f963e-103">Obtener usuario</span><span class="sxs-lookup"><span data-stu-id="f963e-103">Get user</span></span>

> <span data-ttu-id="f963e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f963e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f963e-105">Lea las propiedades y las relaciones del objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="f963e-105">Read properties and relationships of the [user](../resources/intune-shared-user.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f963e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f963e-106">Prerequisites</span></span>
<span data-ttu-id="f963e-107">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f963e-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f963e-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f963e-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="f963e-109">El permiso específico depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="f963e-109">The specific permission depends on the context.</span></span>

|<span data-ttu-id="f963e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f963e-110">Permission type</span></span>|<span data-ttu-id="f963e-111">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f963e-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f963e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f963e-112">Delegated (work or school account)</span></span>| <span data-ttu-id="f963e-113">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="f963e-113">_varies by context_</span></span>|
| <span data-ttu-id="f963e-114">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f963e-114">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="f963e-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="f963e-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="f963e-116">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="f963e-116">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="f963e-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="f963e-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="f963e-118">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="f963e-118">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="f963e-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="f963e-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="f963e-120">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="f963e-120">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="f963e-121">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="f963e-121">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="f963e-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f963e-122">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f963e-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f963e-123">Not supported.</span></span>|
|<span data-ttu-id="f963e-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f963e-124">Application</span></span>|<span data-ttu-id="f963e-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f963e-125">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f963e-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f963e-126">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f963e-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f963e-127">Optional query parameters</span></span>
<span data-ttu-id="f963e-128">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f963e-128">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f963e-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f963e-129">Request headers</span></span>
|<span data-ttu-id="f963e-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f963e-130">Header</span></span>|<span data-ttu-id="f963e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f963e-131">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f963e-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="f963e-132">Authorization</span></span>|<span data-ttu-id="f963e-133">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f963e-133">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f963e-134">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f963e-134">Accept</span></span>|<span data-ttu-id="f963e-135">application/json</span><span class="sxs-lookup"><span data-stu-id="f963e-135">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f963e-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f963e-136">Request body</span></span>
<span data-ttu-id="f963e-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f963e-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f963e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f963e-138">Response</span></span>
<span data-ttu-id="f963e-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f963e-139">If successful, this method returns a `200 OK` response code and [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f963e-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f963e-140">Example</span></span>

### <a name="request"></a><span data-ttu-id="f963e-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f963e-141">Request</span></span>
<span data-ttu-id="f963e-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f963e-142">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="f963e-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f963e-143">Response</span></span>
<span data-ttu-id="f963e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f963e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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



