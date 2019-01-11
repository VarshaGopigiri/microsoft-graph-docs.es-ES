---
title: 'synchronizationSchema: las funciones'
description: Lista de todas las funciones que se admiten actualmente en la attributeMappingSource.
localization_priority: Normal
ms.openlocfilehash: 5dc7734e9d747ac1e832aebb7d9c7355c2fbb52f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841012"
---
# <a name="synchronizationschema-functions"></a><span data-ttu-id="da477-103">synchronizationSchema: las funciones</span><span class="sxs-lookup"><span data-stu-id="da477-103">synchronizationSchema: functions</span></span>

> <span data-ttu-id="da477-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="da477-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="da477-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="da477-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="da477-106">Lista de todas las funciones que se admiten actualmente en la [attributeMappingSource](../resources/synchronization-attributemappingsource.md).</span><span class="sxs-lookup"><span data-stu-id="da477-106">List all the functions currently supported in the [attributeMappingSource](../resources/synchronization-attributemappingsource.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="da477-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="da477-107">Permissions</span></span>
<span data-ttu-id="da477-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="da477-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="da477-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="da477-110">Permission type</span></span>                        | <span data-ttu-id="da477-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="da477-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="da477-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="da477-112">Delegated (work or school account)</span></span>     |<span data-ttu-id="da477-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="da477-113">Directory.ReadWrite.All</span></span>  |
|<span data-ttu-id="da477-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="da477-114">Delegated (personal Microsoft account)</span></span> |<span data-ttu-id="da477-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da477-115">Not supported.</span></span>|
|<span data-ttu-id="da477-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="da477-116">Application</span></span>                            |<span data-ttu-id="da477-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da477-117">Not supported.</span></span> | 

## <a name="http-request"></a><span data-ttu-id="da477-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="da477-118">HTTP Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /servicePrincipals/{id}/synchronization/jobs/{jobId}/schema/functions
GET /servicePrincipals/{id}/synchronization/templates/{templateId}/schema/functions
GET /applications/{id}/synchronization/templates/{templateId}/schema/functions
```

## <a name="request-headers"></a><span data-ttu-id="da477-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="da477-119">Request headers</span></span>

| <span data-ttu-id="da477-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="da477-120">Name</span></span>           | <span data-ttu-id="da477-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="da477-121">Type</span></span>    | <span data-ttu-id="da477-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="da477-122">Description</span></span>|
|:---------------|:--------|:-----------|
| <span data-ttu-id="da477-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="da477-123">Authorization</span></span>  | <span data-ttu-id="da477-124">string</span><span class="sxs-lookup"><span data-stu-id="da477-124">string</span></span>  | <span data-ttu-id="da477-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="da477-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="da477-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="da477-127">Request body</span></span>

<span data-ttu-id="da477-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="da477-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="da477-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da477-129">Response</span></span>

<span data-ttu-id="da477-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [attributemappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da477-130">If successful, this method returns a `200 OK` response code and a collection of [attributemappingFunctionSchema](../resources/synchronization-attributemappingfunctionschema.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="da477-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da477-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="da477-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="da477-132">Request</span></span>
<span data-ttu-id="da477-133">El siguiente es un ejemplo de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="da477-133">The following is an example of a request.</span></span>
<!-- {
  "blockType": "request",
  "name": "synchronizationschema_functions"
}-->
```http
GET https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema/functions
```

##### <a name="response"></a><span data-ttu-id="da477-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da477-134">Response</span></span>
<span data-ttu-id="da477-135">El siguiente es un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="da477-135">The following is an example of a response.</span></span>

><span data-ttu-id="da477-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="da477-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="da477-137">Se devolverán todas las propiedades en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="da477-137">All the properties will be returned in an actual call.</span></span>

<!--
{
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attributeMappingFunctionSchema",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#functions",
    "value": [
        {
            "name": "Append",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "suffix",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "DefaultDomain",
            "parameters": []
        },
        {
            "name": "AppRoleAssignments",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "FormatDateTime",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "inputFormat",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "outputFormat",
                    "required": true,
                    "type": "String"
                }
            ]
        }
    ]
}
```

<!--
Below is the full response, which had to be redacted above as Markdown Scanner tool trips over "type" values containing 
non-string type names like "Integer" or "Boolean"

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#functions",
    "value": [
        {
            "name": "Append",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "suffix",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "DefaultDomain",
            "parameters": []
        },
        {
            "name": "AppRoleAssignments",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "FormatDateTime",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "inputFormat",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "outputFormat",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "IsNothing",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "Boolean"
                }
            ]
        },
        {
            "name": "Join",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "separator",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": true,
                    "name": "source",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "Prepend",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "prefix",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "Mid",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "start",
                    "required": true,
                    "type": "Integer"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "length",
                    "required": true,
                    "type": "Integer"
                }
            ]
        },
        {
            "name": "Not",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "Boolean"
                }
            ]
        },
        {
            "name": "Replace",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "Find",
                    "required": false,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "RegularExpression",
                    "required": false,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "RegularExpressionGroupName",
                    "required": false,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "Replacement",
                    "required": false,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "ReplacementPropertyName",
                    "required": false,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "Template",
                    "required": false,
                    "type": "String"
                }
            ]
        },
        {
            "name": "SingleAppRoleAssignment",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "Split",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "delimiter",
                    "required": false,
                    "type": "String"
                }
            ]
        },
        {
            "name": "StripSpaces",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                }
            ]
        },
        {
            "name": "Switch",
            "parameters": [
                {
                    "allowMultipleOccurrences": false,
                    "name": "source",
                    "required": true,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": false,
                    "name": "defaultValue",
                    "required": false,
                    "type": "String"
                },
                {
                    "allowMultipleOccurrences": true,
                    "name": "switchValue",
                    "required": false,
                    "type": "String"
                }
            ]
        }
    ]
}

-->

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationSchema: functions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
