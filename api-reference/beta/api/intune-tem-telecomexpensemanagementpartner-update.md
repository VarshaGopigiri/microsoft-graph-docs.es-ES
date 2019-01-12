---
title: Actualizar telecomExpenseManagementPartner
description: Actualice las propiedades de un objeto telecomExpenseManagementPartner.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7d48b92068e98e1768630845046a2eb4129167e1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924667"
---
# <a name="update-telecomexpensemanagementpartner"></a><span data-ttu-id="bd6b3-103">Actualizar telecomExpenseManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bd6b3-103">Update telecomExpenseManagementPartner</span></span>

> <span data-ttu-id="bd6b3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bd6b3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bd6b3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bd6b3-107">Actualice las propiedades de un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="bd6b3-107">Update the properties of a [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bd6b3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bd6b3-108">Prerequisites</span></span>
<span data-ttu-id="bd6b3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bd6b3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bd6b3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd6b3-111">Permission type</span></span>|<span data-ttu-id="bd6b3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd6b3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bd6b3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd6b3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bd6b3-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bd6b3-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="bd6b3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd6b3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bd6b3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-116">Not supported.</span></span>|
|<span data-ttu-id="bd6b3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd6b3-117">Application</span></span>|<span data-ttu-id="bd6b3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bd6b3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd6b3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/telecomExpenseManagementPartners/{telecomExpenseManagementPartnerId}
```

## <a name="request-headers"></a><span data-ttu-id="bd6b3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd6b3-120">Request headers</span></span>
|<span data-ttu-id="bd6b3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd6b3-121">Header</span></span>|<span data-ttu-id="bd6b3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bd6b3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bd6b3-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bd6b3-123">Authorization</span></span>|<span data-ttu-id="bd6b3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bd6b3-125">Accept</span><span class="sxs-lookup"><span data-stu-id="bd6b3-125">Accept</span></span>|<span data-ttu-id="bd6b3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bd6b3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bd6b3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd6b3-127">Request body</span></span>
<span data-ttu-id="bd6b3-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="bd6b3-128">In the request body, supply a JSON representation for the [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object.</span></span>

<span data-ttu-id="bd6b3-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="bd6b3-129">The following table shows the properties that are required when you create the [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span></span>

|<span data-ttu-id="bd6b3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bd6b3-130">Property</span></span>|<span data-ttu-id="bd6b3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd6b3-131">Type</span></span>|<span data-ttu-id="bd6b3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd6b3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bd6b3-133">id</span><span class="sxs-lookup"><span data-stu-id="bd6b3-133">id</span></span>|<span data-ttu-id="bd6b3-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="bd6b3-134">String</span></span>|<span data-ttu-id="bd6b3-135">Identificador único del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-135">Unique identifier of the TEM partner.</span></span>|
|<span data-ttu-id="bd6b3-136">displayName</span><span class="sxs-lookup"><span data-stu-id="bd6b3-136">displayName</span></span>|<span data-ttu-id="bd6b3-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="bd6b3-137">String</span></span>|<span data-ttu-id="bd6b3-138">Nombre para mostrar del partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-138">Display name of the TEM partner.</span></span>|
|<span data-ttu-id="bd6b3-139">url</span><span class="sxs-lookup"><span data-stu-id="bd6b3-139">url</span></span>|<span data-ttu-id="bd6b3-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="bd6b3-140">String</span></span>|<span data-ttu-id="bd6b3-141">Dirección URL del panel de control administrativo del partner de TEM, donde un administrador puede configurar el servicio de su TEM.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-141">URL of the TEM partner's administrative control panel, where an administrator can configure their TEM service.</span></span>|
|<span data-ttu-id="bd6b3-142">appAuthorized</span><span class="sxs-lookup"><span data-stu-id="bd6b3-142">appAuthorized</span></span>|<span data-ttu-id="bd6b3-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="bd6b3-143">Boolean</span></span>|<span data-ttu-id="bd6b3-144">Si se ha autorizado a la aplicación de AAD del partner para que obtenga acceso a Intune.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-144">Whether the partner's AAD app has been authorized to access Intune.</span></span>|
|<span data-ttu-id="bd6b3-145">enabled</span><span class="sxs-lookup"><span data-stu-id="bd6b3-145">enabled</span></span>|<span data-ttu-id="bd6b3-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="bd6b3-146">Boolean</span></span>|<span data-ttu-id="bd6b3-147">Si la conexión de Intune al servicio de TEM está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-147">Whether Intune's connection to the TEM service is currently enabled or disabled.</span></span>|
|<span data-ttu-id="bd6b3-148">lastConnectionDateTime</span><span class="sxs-lookup"><span data-stu-id="bd6b3-148">lastConnectionDateTime</span></span>|<span data-ttu-id="bd6b3-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bd6b3-149">DateTimeOffset</span></span>|<span data-ttu-id="bd6b3-150">Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-150">Timestamp of the last request sent to Intune by the TEM partner.</span></span>|



## <a name="response"></a><span data-ttu-id="bd6b3-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd6b3-151">Response</span></span>
<span data-ttu-id="bd6b3-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-152">If successful, this method returns a `200 OK` response code and an updated [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bd6b3-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd6b3-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="bd6b3-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd6b3-154">Request</span></span>
<span data-ttu-id="bd6b3-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/telecomExpenseManagementPartners/{telecomExpenseManagementPartnerId}
Content-type: application/json
Content-length: 178

{
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```

### <a name="response"></a><span data-ttu-id="bd6b3-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd6b3-156">Response</span></span>
<span data-ttu-id="bd6b3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bd6b3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 297

{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "id": "47a3b399-b399-47a3-99b3-a34799b3a347",
  "displayName": "Display Name value",
  "url": "Url value",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
}
```





