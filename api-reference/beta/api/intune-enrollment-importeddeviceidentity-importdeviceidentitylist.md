---
title: acción importDeviceIdentityList
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: d3f719a9f2b7358acfa413810b6bd091d32f52f3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338167"
---
# <a name="importdeviceidentitylist-action"></a><span data-ttu-id="53534-103">acción importDeviceIdentityList</span><span class="sxs-lookup"><span data-stu-id="53534-103">importDeviceIdentityList action</span></span>

> <span data-ttu-id="53534-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53534-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53534-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53534-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="53534-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53534-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53534-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="53534-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="53534-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="53534-108">Prerequisites</span></span>
<span data-ttu-id="53534-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53534-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="53534-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53534-111">Permission type</span></span>|<span data-ttu-id="53534-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53534-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="53534-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53534-113">Delegated (work or school account)</span></span>|<span data-ttu-id="53534-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="53534-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="53534-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53534-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="53534-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53534-116">Not supported.</span></span>|
|<span data-ttu-id="53534-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53534-117">Application</span></span>|<span data-ttu-id="53534-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53534-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="53534-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53534-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/importedDeviceIdentities/importDeviceIdentityList
```

## <a name="request-headers"></a><span data-ttu-id="53534-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53534-120">Request headers</span></span>
|<span data-ttu-id="53534-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53534-121">Header</span></span>|<span data-ttu-id="53534-122">Valor</span><span class="sxs-lookup"><span data-stu-id="53534-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="53534-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="53534-123">Authorization</span></span>|<span data-ttu-id="53534-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="53534-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="53534-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="53534-125">Accept</span></span>|<span data-ttu-id="53534-126">application/json</span><span class="sxs-lookup"><span data-stu-id="53534-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="53534-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53534-127">Request body</span></span>
<span data-ttu-id="53534-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="53534-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="53534-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="53534-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="53534-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53534-130">Property</span></span>|<span data-ttu-id="53534-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="53534-131">Type</span></span>|<span data-ttu-id="53534-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="53534-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53534-133">importedDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="53534-133">importedDeviceIdentities</span></span>|<span data-ttu-id="53534-134">colección de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="53534-134">[importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) collection</span></span>|<span data-ttu-id="53534-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="53534-135">Not yet documented</span></span>|
|<span data-ttu-id="53534-136">overwriteImportedDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="53534-136">overwriteImportedDeviceIdentities</span></span>|<span data-ttu-id="53534-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="53534-137">Boolean</span></span>|<span data-ttu-id="53534-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="53534-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="53534-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53534-139">Response</span></span>
<span data-ttu-id="53534-140">Si tiene éxito, esta acción devuelve un `200 OK` código de respuesta y una colección de [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53534-140">If successful, this action returns a `200 OK` response code and a [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53534-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53534-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="53534-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53534-142">Request</span></span>
<span data-ttu-id="53534-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53534-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/importedDeviceIdentities/importDeviceIdentityList

Content-type: application/json
Content-length: 642

{
  "importedDeviceIdentities": [
    {
      "@odata.type": "#microsoft.graph.importedDeviceIdentity",
      "id": "9f70a12f-a12f-9f70-2fa1-709f2fa1709f",
      "importedDeviceIdentifier": "Imported Device Identifier value",
      "importedDeviceIdentityType": "imei",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
      "description": "Description value",
      "enrollmentState": "enrolled",
      "platform": "ios"
    }
  ],
  "overwriteImportedDeviceIdentities": true
}
```

### <a name="response"></a><span data-ttu-id="53534-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53534-144">Response</span></span>
<span data-ttu-id="53534-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53534-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 606

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.importedDeviceIdentityResult",
      "id": "9dfd3690-3690-9dfd-9036-fd9d9036fd9d",
      "importedDeviceIdentifier": "Imported Device Identifier value",
      "importedDeviceIdentityType": "imei",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
      "description": "Description value",
      "enrollmentState": "enrolled",
      "platform": "ios",
      "status": true
    }
  ]
}
```





