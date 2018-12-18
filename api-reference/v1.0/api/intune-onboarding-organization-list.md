---
title: Enumerar organizaciones
description: Lea las propiedades y las relaciones de los objetos organization.
author: tfitzmac
ms.openlocfilehash: 4ad5c23d038274de62a7ab4f4e9c0a467918e754
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309068"
---
# <a name="list-organizations"></a><span data-ttu-id="83e97-103">Enumerar organizaciones</span><span class="sxs-lookup"><span data-stu-id="83e97-103">List organizations</span></span>

> <span data-ttu-id="83e97-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="83e97-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="83e97-105">Lea las propiedades y las relaciones de los objetos [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="83e97-105">List properties and relationships of the [organization](../resources/intune-onboarding-organization.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="83e97-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="83e97-106">Prerequisites</span></span>
<span data-ttu-id="83e97-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="83e97-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="83e97-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="83e97-109">Permission type</span></span>|<span data-ttu-id="83e97-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="83e97-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="83e97-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="83e97-111">Delegated (work or school account)</span></span>|<span data-ttu-id="83e97-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="83e97-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="83e97-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="83e97-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="83e97-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="83e97-114">Not supported.</span></span>|
|<span data-ttu-id="83e97-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="83e97-115">Application</span></span>|<span data-ttu-id="83e97-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="83e97-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="83e97-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="83e97-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /organization
```

## <a name="request-headers"></a><span data-ttu-id="83e97-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="83e97-118">Request headers</span></span>
|<span data-ttu-id="83e97-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83e97-119">Header</span></span>|<span data-ttu-id="83e97-120">Valor</span><span class="sxs-lookup"><span data-stu-id="83e97-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="83e97-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="83e97-121">Authorization</span></span>|<span data-ttu-id="83e97-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="83e97-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="83e97-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="83e97-123">Accept</span></span>|<span data-ttu-id="83e97-124">application/json</span><span class="sxs-lookup"><span data-stu-id="83e97-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="83e97-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="83e97-125">Request body</span></span>
<span data-ttu-id="83e97-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="83e97-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="83e97-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83e97-127">Response</span></span>
<span data-ttu-id="83e97-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [organization](../resources/intune-onboarding-organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="83e97-128">If successful, this method returns a `200 OK` response code and a collection of [organization](../resources/intune-onboarding-organization.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="83e97-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="83e97-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="83e97-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="83e97-130">Request</span></span>
<span data-ttu-id="83e97-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="83e97-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/organization
```

### <a name="response"></a><span data-ttu-id="83e97-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83e97-132">Response</span></span>
<span data-ttu-id="83e97-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="83e97-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 196

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.organization",
      "id": "9efe224a-224a-9efe-4a22-fe9e4a22fe9e",
      "mobileDeviceManagementAuthority": "intune"
    }
  ]
}
```



