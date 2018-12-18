---
title: Enumerar deviceCategories
description: Enumere las propiedades y las relaciones de los objetos deviceCategory.
author: tfitzmac
ms.openlocfilehash: c5cc37f375a56d1e1ca005841af83936760deb69
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327163"
---
# <a name="list-devicecategories"></a><span data-ttu-id="2afb5-103">Enumerar deviceCategories</span><span class="sxs-lookup"><span data-stu-id="2afb5-103">List deviceCategories</span></span>

> <span data-ttu-id="2afb5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2afb5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2afb5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2afb5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2afb5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2afb5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2afb5-107">Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="2afb5-107">List properties and relationships of the [deviceCategory](../resources/intune-shared-devicecategory.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2afb5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2afb5-108">Prerequisites</span></span>
<span data-ttu-id="2afb5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2afb5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2afb5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2afb5-111">Permission type</span></span>|<span data-ttu-id="2afb5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2afb5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2afb5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2afb5-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="2afb5-114">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="2afb5-114">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="2afb5-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="2afb5-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="2afb5-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2afb5-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2afb5-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2afb5-117">Not supported.</span></span>|
|<span data-ttu-id="2afb5-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2afb5-118">Application</span></span>|<span data-ttu-id="2afb5-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2afb5-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2afb5-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2afb5-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCategories
```

## <a name="request-headers"></a><span data-ttu-id="2afb5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2afb5-121">Request headers</span></span>

|<span data-ttu-id="2afb5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2afb5-122">Header</span></span>|<span data-ttu-id="2afb5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2afb5-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2afb5-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="2afb5-124">Authorization</span></span>|<span data-ttu-id="2afb5-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2afb5-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2afb5-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2afb5-126">Accept</span></span>|<span data-ttu-id="2afb5-127">application/json</span><span class="sxs-lookup"><span data-stu-id="2afb5-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2afb5-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2afb5-128">Request body</span></span>

<span data-ttu-id="2afb5-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2afb5-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2afb5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2afb5-130">Response</span></span>

<span data-ttu-id="2afb5-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCategory](../resources/intune-shared-devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2afb5-131">If successful, this method returns a `200 OK` response code and a collection of [deviceCategory](../resources/intune-shared-devicecategory.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2afb5-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2afb5-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="2afb5-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2afb5-133">Request</span></span>

<span data-ttu-id="2afb5-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2afb5-134">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCategories
```

### <a name="response"></a><span data-ttu-id="2afb5-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2afb5-135">Response</span></span>

<span data-ttu-id="2afb5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2afb5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceCategory",
      "id": "f881b841-b841-f881-41b8-81f841b881f8",
      "displayName": "Display Name value",
      "description": "Description value"
    }
  ]
}
```



