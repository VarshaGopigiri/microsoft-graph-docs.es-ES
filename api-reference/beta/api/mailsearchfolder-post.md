---
title: Crear mailSearchFolder
description: Utilice esta API para crear un nuevo mailSearchFolder en el buzón del usuario especificado.
localization_priority: Normal
ms.openlocfilehash: 07c6b96bc2dec35d06b5563673012ca0eafb3885
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840190"
---
# <a name="create-mailsearchfolder"></a><span data-ttu-id="ac443-103">Crear mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="ac443-103">Create mailSearchFolder</span></span>

> <span data-ttu-id="ac443-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ac443-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ac443-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ac443-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ac443-106">Utilice esta API para crear un nuevo [mailSearchFolder](../resources/mailsearchfolder.md) en el buzón del usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="ac443-106">Use this API to create a new [mailSearchFolder](../resources/mailsearchfolder.md) in the specified user's mailbox.</span></span>

## <a name="permissions"></a><span data-ttu-id="ac443-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ac443-107">Permissions</span></span>

<span data-ttu-id="ac443-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ac443-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ac443-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac443-110">Permission type</span></span> | <span data-ttu-id="ac443-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac443-111">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="ac443-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac443-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ac443-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ac443-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ac443-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac443-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ac443-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ac443-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ac443-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac443-116">Application</span></span> | <span data-ttu-id="ac443-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ac443-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ac443-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac443-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

<span data-ttu-id="ac443-119">Especifique la carpeta principal en la dirección URL de consulta como un identificador de carpeta o nombre de una carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="ac443-119">Specify the parent folder in the query URL as a folder ID, or a well-known folder name.</span></span> <span data-ttu-id="ac443-120">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="ac443-120">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>

## <a name="request-headers"></a><span data-ttu-id="ac443-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ac443-121">Request headers</span></span>

| <span data-ttu-id="ac443-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac443-122">Header</span></span> | <span data-ttu-id="ac443-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ac443-123">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="ac443-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="ac443-124">Authorization</span></span> | <span data-ttu-id="ac443-125">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="ac443-125"></span></span> <span data-ttu-id="ac443-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ac443-126">Required.</span></span> |
| <span data-ttu-id="ac443-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ac443-127">Content-Type</span></span> | <span data-ttu-id="ac443-128">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="ac443-128"></span></span> <span data-ttu-id="ac443-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ac443-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ac443-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ac443-130">Request body</span></span>

<span data-ttu-id="ac443-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ac443-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ac443-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ac443-132">Parameter</span></span> | <span data-ttu-id="ac443-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac443-133">Type</span></span> | <span data-ttu-id="ac443-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac443-134">Description</span></span> |
|:----------|:-----|:------------|
| <span data-ttu-id="ac443-135">@odata.type</span><span class="sxs-lookup"><span data-stu-id="ac443-135">@odata.type</span></span> | <span data-ttu-id="ac443-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac443-136">String</span></span> | <span data-ttu-id="ac443-137">El tipo de carpeta que se creará.</span><span class="sxs-lookup"><span data-stu-id="ac443-137">The type of folder to be created.</span></span> <span data-ttu-id="ac443-138">Se establece en "microsoft.graph.mailSearchFolder".</span><span class="sxs-lookup"><span data-stu-id="ac443-138">Set to "microsoft.graph.mailSearchFolder".</span></span> |
| <span data-ttu-id="ac443-139">displayName</span><span class="sxs-lookup"><span data-stu-id="ac443-139">displayName</span></span> | <span data-ttu-id="ac443-140">String</span><span class="sxs-lookup"><span data-stu-id="ac443-140">String</span></span> | <span data-ttu-id="ac443-141">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="ac443-141">The display name of the new folder.</span></span>|
| <span data-ttu-id="ac443-142">includeNestedFolders</span><span class="sxs-lookup"><span data-stu-id="ac443-142">includeNestedFolders</span></span> | <span data-ttu-id="ac443-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="ac443-143">Boolean</span></span> | <span data-ttu-id="ac443-144">¿Cómo se debe recorrer la jerarquía de carpetas de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="ac443-144">How the mailbox folder hierarchy should be traversed.</span></span> <span data-ttu-id="ac443-145">`true`significa que debe ser una búsqueda en profundidad mientras `false` significa que se debe realizar una búsqueda no exhaustivos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ac443-145">`true` means that a deep search should be done while `false` means a shallow search should be done instead.</span></span> |
| <span data-ttu-id="ac443-146">sourceFolderIDs</span><span class="sxs-lookup"><span data-stu-id="ac443-146">sourceFolderIDs</span></span> | <span data-ttu-id="ac443-147">Colección String</span><span class="sxs-lookup"><span data-stu-id="ac443-147">String collection</span></span> | <span data-ttu-id="ac443-148">Las carpetas de buzón de correo que deben ser extraídas.</span><span class="sxs-lookup"><span data-stu-id="ac443-148">The mailbox folders that should be mined.</span></span> |
| <span data-ttu-id="ac443-149">filterQuery</span><span class="sxs-lookup"><span data-stu-id="ac443-149">filterQuery</span></span> | <span data-ttu-id="ac443-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac443-150">String</span></span> | <span data-ttu-id="ac443-151">La consulta de OData para filtrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ac443-151">The OData query to filter the messages.</span></span> |

## <a name="response"></a><span data-ttu-id="ac443-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac443-152">Response</span></span>

<span data-ttu-id="ac443-153">Si tiene éxito, este método devuelve `201 Created` código de respuesta y un objeto [mailSearchFolder](../resources/mailsearchfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac443-153">If successful, this method returns `201 Created` response code and a [mailSearchFolder](../resources/mailsearchfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ac443-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac443-154">Example</span></span>

#### <a name="request"></a><span data-ttu-id="ac443-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac443-155">Request</span></span>

<span data-ttu-id="ac443-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac443-156">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_mailsearchfolder"
}-->

```http
POST https://graph.microsoft.com/beta/me/mailFolders/searchfolders/childfolders
Content-type: application/json
Content-length: 159

{
  "@odata.type": "microsoft.graph.mailSearchFolder",
  "displayName": "Get MyAnalytics",
  "includeNestedFolders": true,
  "sourceFolderIDs": ["AAMkAGVmMDEzM"],
  "filterQuery": "contains(subject, 'MyAnalytics')"
}
```

#### <a name="response"></a><span data-ttu-id="ac443-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac443-157">Response</span></span>

<span data-ttu-id="ac443-158">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac443-158">The following is an example of the response.</span></span>

><span data-ttu-id="ac443-159">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="ac443-159">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="ac443-160">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ac443-160">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailSearchFolder"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "@odata.type": "#microsoft.graph.mailSearchFolder",
  "id": "AAMkAGVmMDEzMx",
  "displayName": "Get MyAnalytics",
  "parentFolderId": "AAMkAGVmMDEzMy",
  "childFolderCount": 0,
  "unreadItemCount": 0,
  "totalItemCount": 13,
  "wellKnownName": null,
  "isSupported": true,
  "includeNestedFolders": true,
  "sourceFolderIDs": [
    "AAMkAGVmMDEzMi"
  ],
  "filterQuery": "contains(subject, 'MyAnalytics')"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create mailSearchFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
