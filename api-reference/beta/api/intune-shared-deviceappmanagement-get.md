---
title: Obtener deviceAppManagement
description: Lea las propiedades y las relaciones del objeto deviceAppManagement.
ms.openlocfilehash: b73e616735ca3f096c01a9f7eba8a7d751bb7160
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084339"
---
# <a name="get-deviceappmanagement"></a><span data-ttu-id="06648-103">Obtener deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="06648-103">Get deviceAppManagement</span></span>

> <span data-ttu-id="06648-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="06648-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="06648-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="06648-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="06648-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="06648-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="06648-107">Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="06648-107">Read properties and relationships of the [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="06648-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="06648-108">Prerequisites</span></span>

<span data-ttu-id="06648-109">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="06648-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="06648-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06648-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="06648-111">Tenga en cuenta que el permiso adecuado varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="06648-111">Note that the appropriate permission varies according to the workflow.</span></span>

|<span data-ttu-id="06648-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06648-112">Permission type</span></span>|<span data-ttu-id="06648-113">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06648-113">Permissions (from most to least privileged)</span></span>|
|:---|:---|
| <span data-ttu-id="06648-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06648-114">Delegated (work or school account)</span></span> | |
| <span data-ttu-id="06648-115">&nbsp;&nbsp; **Aplicaciones**, **libros**o **incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="06648-115">&nbsp; &nbsp; **Apps**, **books**, or **onboarding**</span></span> | <span data-ttu-id="06648-116">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.ReadW.All</span><span class="sxs-lookup"><span data-stu-id="06648-116">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.ReadW.All</span></span> |
| <span data-ttu-id="06648-117">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="06648-117">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="06648-118">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="06648-118">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="06648-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06648-119">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="06648-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06648-120">Not supported.</span></span>|
|<span data-ttu-id="06648-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06648-121">Application</span></span>|<span data-ttu-id="06648-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06648-122">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="06648-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06648-123">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="06648-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="06648-124">Optional query parameters</span></span>

<span data-ttu-id="06648-125">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06648-125">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="06648-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06648-126">Request headers</span></span>

|<span data-ttu-id="06648-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06648-127">Header</span></span>|<span data-ttu-id="06648-128">Valor</span><span class="sxs-lookup"><span data-stu-id="06648-128">Value</span></span>|
|:---|:---|
|<span data-ttu-id="06648-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="06648-129">Authorization</span></span>|<span data-ttu-id="06648-130">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="06648-130">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="06648-131">Aceptar</span><span class="sxs-lookup"><span data-stu-id="06648-131">Accept</span></span>|<span data-ttu-id="06648-132">application/json</span><span class="sxs-lookup"><span data-stu-id="06648-132">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="06648-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06648-133">Request body</span></span>

<span data-ttu-id="06648-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="06648-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="06648-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06648-135">Response</span></span>

<span data-ttu-id="06648-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06648-136">If successful, this method returns a `200 OK` response code and [deviceAppManagement](../resources/intune-shared-deviceappmanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="06648-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06648-137">Example</span></span>

### <a name="request"></a><span data-ttu-id="06648-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06648-138">Request</span></span>

<span data-ttu-id="06648-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06648-139">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/deviceAppManagement
```

### <a name="response"></a><span data-ttu-id="06648-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06648-140">Response</span></span>

<span data-ttu-id="06648-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06648-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 133

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceAppManagement",
    "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
  }
}
```



