---
title: Lista androidManagedStoreAppConfigurationSchemas
description: Propiedades de la lista y relaciones de los objetos androidManagedStoreAppConfigurationSchema.
author: tfitzmac
ms.openlocfilehash: 1b13d49d1fa350d21001d9075f28eedc19191086
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358677"
---
# <a name="list-androidmanagedstoreappconfigurationschemas"></a><span data-ttu-id="722ee-103">Lista androidManagedStoreAppConfigurationSchemas</span><span class="sxs-lookup"><span data-stu-id="722ee-103">List androidManagedStoreAppConfigurationSchemas</span></span>

> <span data-ttu-id="722ee-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="722ee-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="722ee-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="722ee-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="722ee-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="722ee-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="722ee-107">Propiedades de la lista y relaciones de los objetos [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) .</span><span class="sxs-lookup"><span data-stu-id="722ee-107">List properties and relationships of the [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="722ee-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="722ee-108">Prerequisites</span></span>
<span data-ttu-id="722ee-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="722ee-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="722ee-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="722ee-111">Permission type</span></span>|<span data-ttu-id="722ee-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="722ee-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="722ee-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="722ee-113">Delegated (work or school account)</span></span>|<span data-ttu-id="722ee-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="722ee-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="722ee-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="722ee-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="722ee-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="722ee-116">Not supported.</span></span>|
|<span data-ttu-id="722ee-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="722ee-117">Application</span></span>|<span data-ttu-id="722ee-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="722ee-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="722ee-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="722ee-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/androidManagedStoreAppConfigurationSchemas
```

## <a name="request-headers"></a><span data-ttu-id="722ee-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="722ee-120">Request headers</span></span>
|<span data-ttu-id="722ee-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="722ee-121">Header</span></span>|<span data-ttu-id="722ee-122">Valor</span><span class="sxs-lookup"><span data-stu-id="722ee-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="722ee-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="722ee-123">Authorization</span></span>|<span data-ttu-id="722ee-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="722ee-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="722ee-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="722ee-125">Accept</span></span>|<span data-ttu-id="722ee-126">application/json</span><span class="sxs-lookup"><span data-stu-id="722ee-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="722ee-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="722ee-127">Request body</span></span>
<span data-ttu-id="722ee-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="722ee-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="722ee-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="722ee-129">Response</span></span>
<span data-ttu-id="722ee-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="722ee-130">If successful, this method returns a `200 OK` response code and a collection of [androidManagedStoreAppConfigurationSchema](../resources/intune-androidforwork-androidmanagedstoreappconfigurationschema.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="722ee-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="722ee-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="722ee-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="722ee-132">Request</span></span>
<span data-ttu-id="722ee-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="722ee-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/androidManagedStoreAppConfigurationSchemas
```

### <a name="response"></a><span data-ttu-id="722ee-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="722ee-134">Response</span></span>
<span data-ttu-id="722ee-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="722ee-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 987

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidManagedStoreAppConfigurationSchema",
      "id": "db86c34a-c34a-db86-4ac3-86db4ac386db",
      "exampleJson": "ZXhhbXBsZUpzb24=",
      "schemaItems": [
        {
          "@odata.type": "microsoft.graph.androidManagedStoreAppConfigurationSchemaItem",
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





