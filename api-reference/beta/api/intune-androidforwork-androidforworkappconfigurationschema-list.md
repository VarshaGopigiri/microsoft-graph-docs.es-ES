---
title: Enumerar androidForWorkAppConfigurationSchemas
description: Enumere las propiedades y las relaciones de los objetos androidForWorkAppConfigurationSchema.
author: tfitzmac
ms.openlocfilehash: 140a49f8cbb93b6c1990dd80ee4eaec8e23c1859
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358936"
---
# <a name="list-androidforworkappconfigurationschemas"></a><span data-ttu-id="3c352-103">Enumerar androidForWorkAppConfigurationSchemas</span><span class="sxs-lookup"><span data-stu-id="3c352-103">List androidForWorkAppConfigurationSchemas</span></span>

> <span data-ttu-id="3c352-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3c352-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3c352-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3c352-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3c352-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3c352-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3c352-107">Enumere las propiedades y las relaciones de los objetos [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md).</span><span class="sxs-lookup"><span data-stu-id="3c352-107">List properties and relationships of the [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3c352-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3c352-108">Prerequisites</span></span>
<span data-ttu-id="3c352-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3c352-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3c352-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3c352-111">Permission type</span></span>|<span data-ttu-id="3c352-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3c352-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3c352-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3c352-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3c352-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="3c352-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="3c352-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3c352-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3c352-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3c352-116">Not supported.</span></span>|
|<span data-ttu-id="3c352-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3c352-117">Application</span></span>|<span data-ttu-id="3c352-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3c352-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3c352-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3c352-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/androidForWorkAppConfigurationSchemas
```

## <a name="request-headers"></a><span data-ttu-id="3c352-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3c352-120">Request headers</span></span>
|<span data-ttu-id="3c352-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c352-121">Header</span></span>|<span data-ttu-id="3c352-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3c352-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3c352-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3c352-123">Authorization</span></span>|<span data-ttu-id="3c352-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3c352-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3c352-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3c352-125">Accept</span></span>|<span data-ttu-id="3c352-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3c352-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3c352-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3c352-127">Request body</span></span>
<span data-ttu-id="3c352-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3c352-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3c352-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c352-129">Response</span></span>
<span data-ttu-id="3c352-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c352-130">If successful, this method returns a `200 OK` response code and a collection of [androidForWorkAppConfigurationSchema](../resources/intune-androidforwork-androidforworkappconfigurationschema.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3c352-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3c352-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="3c352-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3c352-132">Request</span></span>
<span data-ttu-id="3c352-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3c352-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/androidForWorkAppConfigurationSchemas
```

### <a name="response"></a><span data-ttu-id="3c352-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c352-134">Response</span></span>
<span data-ttu-id="3c352-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3c352-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 977

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidForWorkAppConfigurationSchema",
      "id": "c1230dc6-0dc6-c123-c60d-23c1c60d23c1",
      "exampleJson": "ZXhhbXBsZUpzb24=",
      "schemaItems": [
        {
          "@odata.type": "microsoft.graph.androidForWorkAppConfigurationSchemaItem",
          "schemaItemKey": "Schema Item Key value",
          "displayName": "Display Name value",
          "description": "Description value",
          "defaultBoolValue": true,
          "defaultIntValue": 15,
          "defaultStringValue": "Default String Value value",
          "defaultStringArrayValue": [
            "Default String Array Value value"
          ],
          "dataType": "integer",
          "selections": [
            {
              "@odata.type": "microsoft.graph.keyValuePair",
              "name": "Name value",
              "value": "Value value"
            }
          ]
        }
      ]
    }
  ]
}
```





