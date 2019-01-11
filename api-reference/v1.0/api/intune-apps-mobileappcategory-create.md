---
title: Crear mobileAppCategory
description: Cree un objeto mobileAppCategory.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c09b557da645767e090bfecca7974c0af41b17f5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870801"
---
# <a name="create-mobileappcategory"></a><span data-ttu-id="dcc5f-103">Crear mobileAppCategory</span><span class="sxs-lookup"><span data-stu-id="dcc5f-103">Create mobileAppCategory</span></span>

> <span data-ttu-id="dcc5f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dcc5f-105">Cree un objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md).</span><span class="sxs-lookup"><span data-stu-id="dcc5f-105">Create a new [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dcc5f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dcc5f-106">Prerequisites</span></span>
<span data-ttu-id="dcc5f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dcc5f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dcc5f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dcc5f-109">Permission type</span></span>|<span data-ttu-id="dcc5f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dcc5f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dcc5f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dcc5f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="dcc5f-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dcc5f-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="dcc5f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dcc5f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dcc5f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-114">Not supported.</span></span>|
|<span data-ttu-id="dcc5f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dcc5f-115">Application</span></span>|<span data-ttu-id="dcc5f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dcc5f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dcc5f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppCategories
POST /deviceAppManagement/mobileApps/{mobileAppId}/categories
```

## <a name="request-headers"></a><span data-ttu-id="dcc5f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dcc5f-118">Request headers</span></span>
|<span data-ttu-id="dcc5f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcc5f-119">Header</span></span>|<span data-ttu-id="dcc5f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dcc5f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dcc5f-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="dcc5f-121">Authorization</span></span>|<span data-ttu-id="dcc5f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dcc5f-123">Accept</span><span class="sxs-lookup"><span data-stu-id="dcc5f-123">Accept</span></span>|<span data-ttu-id="dcc5f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="dcc5f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dcc5f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dcc5f-125">Request body</span></span>
<span data-ttu-id="dcc5f-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-126">In the request body, supply a JSON representation for the mobileAppCategory object.</span></span>

<span data-ttu-id="dcc5f-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-127">The following table shows the properties that are required when you create the mobileAppCategory.</span></span>

|<span data-ttu-id="dcc5f-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dcc5f-128">Property</span></span>|<span data-ttu-id="dcc5f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="dcc5f-129">Type</span></span>|<span data-ttu-id="dcc5f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcc5f-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dcc5f-131">id</span><span class="sxs-lookup"><span data-stu-id="dcc5f-131">id</span></span>|<span data-ttu-id="dcc5f-132">String</span><span class="sxs-lookup"><span data-stu-id="dcc5f-132">String</span></span>|<span data-ttu-id="dcc5f-133">La clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-133">The key of the entity.</span></span>|
|<span data-ttu-id="dcc5f-134">displayName</span><span class="sxs-lookup"><span data-stu-id="dcc5f-134">displayName</span></span>|<span data-ttu-id="dcc5f-135">String</span><span class="sxs-lookup"><span data-stu-id="dcc5f-135">String</span></span>|<span data-ttu-id="dcc5f-136">El nombre de la categoría de aplicación.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-136">The name of the app category.</span></span>|
|<span data-ttu-id="dcc5f-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="dcc5f-137">lastModifiedDateTime</span></span>|<span data-ttu-id="dcc5f-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dcc5f-138">DateTimeOffset</span></span>|<span data-ttu-id="dcc5f-139">Fecha y hora de la última modificación de mobileAppCategory.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-139">The date and time the mobileAppCategory was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="dcc5f-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dcc5f-140">Response</span></span>
<span data-ttu-id="dcc5f-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-141">If successful, this method returns a `201 Created` response code and a [mobileAppCategory](../resources/intune-apps-mobileappcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dcc5f-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dcc5f-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="dcc5f-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dcc5f-143">Request</span></span>
<span data-ttu-id="dcc5f-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppCategories
Content-type: application/json
Content-length: 99

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "displayName": "Display Name value"
}
```

### <a name="response"></a><span data-ttu-id="dcc5f-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dcc5f-145">Response</span></span>
<span data-ttu-id="dcc5f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dcc5f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 212

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "id": "d85d9cee-9cee-d85d-ee9c-5dd8ee9c5dd8",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```



