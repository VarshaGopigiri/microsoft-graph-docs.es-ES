---
title: Crear una sesión
description: 'Use esta API para crear una nueva sesión de libro. '
author: lumine2008
ms.openlocfilehash: 802a77884dcc283b520aa179d51aeb6e96a5c68e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340757"
---
# <a name="create-session"></a><span data-ttu-id="60257-103">Crear una sesión</span><span class="sxs-lookup"><span data-stu-id="60257-103">Create Session</span></span>

<span data-ttu-id="60257-104">Use esta API para crear una nueva sesión de libro.</span><span class="sxs-lookup"><span data-stu-id="60257-104">Use this API to create a new workbook session.</span></span> 

<span data-ttu-id="60257-105">Se puede llamar a las API de Excel de dos modos:</span><span class="sxs-lookup"><span data-stu-id="60257-105">Excel APIs can be called in one of two modes:</span></span> 

1. <span data-ttu-id="60257-p101">Sesión persistente - Todos los cambios realizados en el libro son persistentes (se guardan). Este es el modo de operación habitual.</span><span class="sxs-lookup"><span data-stu-id="60257-p101">Persistent session - All changes made to the workbook are persisted (saved). This is the usual mode of operation.</span></span> 
2. <span data-ttu-id="60257-p102">Sesión no persistente - Los cambios realizados por la API no se guardan en la ubicación de origen. En su lugar, el servidor backend de Excel conserva una copia temporal del archivo que refleja los cambios realizados durante esa sesión API en concreto. Cuando expira la sesión de Excel, se pierden los cambios. Este modo es útil para aplicaciones que necesitan realizar análisis u obtener los resultados de un cálculo o una imagen de gráfico, pero no afecta al estado de documento.</span><span class="sxs-lookup"><span data-stu-id="60257-p102">Non-persistent session - Changes made by the API are not saved to the source location. Instead, the Excel backend server keeps a temporary copy of the file that reflects the changes made during that particular API session. When the Excel session expires, the changes are lost. This mode is useful for apps that need to do analysis or obtain the results of a calculation or a chart image, but not affect the document state.</span></span>   

<span data-ttu-id="60257-112">Para representar la sesión en la API, utilice el encabezado `workbook-session-id: {session-id}`.</span><span class="sxs-lookup"><span data-stu-id="60257-112">To represent the session in the API, use the `workbook-session-id: {session-id}` header.</span></span> 

><span data-ttu-id="60257-p103">**Nota:** El encabezado de sesión no es necesario para que funcione una API de Excel. Sin embargo, recomendamos que utilice el encabezado de sesión para mejorar el rendimiento. Si no utiliza un encabezado de sesión, los cambios realizados durante la llamada API _sí_ persisten en el archivo.</span><span class="sxs-lookup"><span data-stu-id="60257-p103">**Note:** The session header is not required for an Excel API to work. However, we recommend that you use the session header to improve performance. If you don't use a session header, changes made during the API call _are_ persisted to the file.</span></span>  

## <a name="error-handling"></a><span data-ttu-id="60257-116">Control de errores</span><span class="sxs-lookup"><span data-stu-id="60257-116">Error Handling</span></span>

<span data-ttu-id="60257-117">En ocasiones, esta solicitud puede recibir el error HTTP 504.</span><span class="sxs-lookup"><span data-stu-id="60257-117">This request might occasionally receive a 504 HTTP error.</span></span> <span data-ttu-id="60257-118">La respuesta adecuada a este error es repetir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60257-118">The appropriate response to this error is to repeat the request.</span></span>

## <a name="permissions"></a><span data-ttu-id="60257-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="60257-119">Permissions</span></span>
<span data-ttu-id="60257-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="60257-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="60257-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="60257-122">Permission type</span></span>      | <span data-ttu-id="60257-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="60257-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="60257-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="60257-124">Delegated (work or school account)</span></span> | <span data-ttu-id="60257-125">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60257-125">Files.ReadWrite</span></span>    |
|<span data-ttu-id="60257-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="60257-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="60257-127">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60257-127">Not supported.</span></span>    |
|<span data-ttu-id="60257-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="60257-128">Application</span></span> | <span data-ttu-id="60257-129">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60257-129">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="60257-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60257-130">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/createSession

```
## <a name="request-headers"></a><span data-ttu-id="60257-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60257-131">Request headers</span></span>
| <span data-ttu-id="60257-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="60257-132">Name</span></span>       | <span data-ttu-id="60257-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="60257-133">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="60257-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="60257-134">Authorization</span></span>  | <span data-ttu-id="60257-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60257-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="60257-137">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="60257-137">Request body</span></span>
<span data-ttu-id="60257-138">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [WorkbookSessionInfo](../resources/workbooksessioninfo.md).</span><span class="sxs-lookup"><span data-stu-id="60257-138">In the request body, supply a JSON representation of [WorkbookSessionInfo](../resources/workbooksessioninfo.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="60257-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60257-139">Response</span></span>

<span data-ttu-id="60257-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [WorkbookSessionInfo](../resources/workbooksessioninfo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60257-140">If successful, this method returns `201 Created` response code and [WorkbookSessionInfo](../resources/workbooksessioninfo.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="60257-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60257-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="60257-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60257-142">Request</span></span>
<span data-ttu-id="60257-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60257-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_excel_session"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/createSession
Content-type: application/json
Content-length: 52

{
  "persistChanges": true
}
```
<span data-ttu-id="60257-144">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [WorkbookSessionInfo](../resources/workbooksessioninfo.md).</span><span class="sxs-lookup"><span data-stu-id="60257-144">In the request body, supply a JSON representation of [WorkbookSessionInfo](../resources/workbooksessioninfo.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="60257-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60257-145">Response</span></span>
<span data-ttu-id="60257-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="60257-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookSessionInfo"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "persistChanges": true
}
```

