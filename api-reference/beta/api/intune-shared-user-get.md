---
title: Obtener usuario
description: Lea las propiedades y las relaciones del objeto user.
author: tfitzmac
ms.openlocfilehash: cf0ee7b2c6d9cf13176f65c174ee4b6ac986984b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359692"
---
# <a name="get-user"></a><span data-ttu-id="ce614-103">Obtener usuario</span><span class="sxs-lookup"><span data-stu-id="ce614-103">Get user</span></span>

> <span data-ttu-id="ce614-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce614-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce614-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce614-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ce614-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce614-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ce614-107">Lea las propiedades y las relaciones del objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="ce614-107">Read properties and relationships of the [user](../resources/intune-shared-user.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ce614-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ce614-108">Prerequisites</span></span>

<span data-ttu-id="ce614-109">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ce614-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="ce614-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ce614-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="ce614-111">El permiso específico depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="ce614-111">The specific permission depends on the context.</span></span>

|<span data-ttu-id="ce614-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce614-112">Permission type</span></span>|<span data-ttu-id="ce614-113">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce614-113">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ce614-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce614-114">Delegated (work or school account)</span></span>||
| <span data-ttu-id="ce614-115">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="ce614-115">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="ce614-116">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="ce614-116">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="ce614-117">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="ce614-117">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="ce614-118">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="ce614-118">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="ce614-119">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="ce614-119">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="ce614-120">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="ce614-120">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="ce614-121">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="ce614-121">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="ce614-122">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="ce614-122">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="ce614-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce614-123">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ce614-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce614-124">Not supported.</span></span>|
|<span data-ttu-id="ce614-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce614-125">Application</span></span>|<span data-ttu-id="ce614-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce614-126">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ce614-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce614-127">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ce614-128">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ce614-128">Optional query parameters</span></span>

<span data-ttu-id="ce614-129">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce614-129">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ce614-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce614-130">Request headers</span></span>

|<span data-ttu-id="ce614-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce614-131">Header</span></span>|<span data-ttu-id="ce614-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ce614-132">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ce614-133">Autorización</span><span class="sxs-lookup"><span data-stu-id="ce614-133">Authorization</span></span>|<span data-ttu-id="ce614-134">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ce614-134">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ce614-135">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ce614-135">Accept</span></span>|<span data-ttu-id="ce614-136">application/json</span><span class="sxs-lookup"><span data-stu-id="ce614-136">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ce614-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce614-137">Request body</span></span>

<span data-ttu-id="ce614-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ce614-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ce614-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce614-139">Response</span></span>

<span data-ttu-id="ce614-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce614-140">If successful, this method returns a `200 OK` response code and [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ce614-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce614-141">Example</span></span>

### <a name="request"></a><span data-ttu-id="ce614-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce614-142">Request</span></span>

<span data-ttu-id="ce614-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce614-143">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="ce614-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce614-144">Response</span></span>

<span data-ttu-id="ce614-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ce614-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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



