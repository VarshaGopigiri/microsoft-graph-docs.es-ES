---
title: Trabajar con Excel en Microsoft Graph
description: 'Puede usar Microsoft Graph para permitir que las aplicaciones web y móviles lean y modifiquen libros de Excel almacenados en OneDrive para la Empresa, un sitio de SharePoint o una unidad de grupo. El recurso `Workbook` (o el archivo de Excel) contiene todos los demás recursos de Excel mediante relaciones. Puede obtener acceso a un libro a través de la API de Drive si identifica la ubicación del archivo en la dirección URL. Por ejemplo:'
localization_priority: Priority
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 0010a7244d9ba6e629849f55dfc793bf6b875b38
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917688"
---
# <a name="working-with-excel-in-microsoft-graph"></a><span data-ttu-id="a1719-106">Trabajar con Excel en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="a1719-106">Working with Excel in Microsoft Graph</span></span>

<span data-ttu-id="a1719-p102">Puede usar Microsoft Graph para permitir que las aplicaciones web y móviles lean y modifiquen libros de Excel almacenados en OneDrive para la Empresa, un sitio de SharePoint o una unidad de grupo. El recurso `Workbook` (o el archivo de Excel) contiene todos los demás recursos de Excel mediante relaciones. Puede obtener acceso a un libro a través de la [API de Drive](drive.md) si identifica la ubicación del archivo en la dirección URL. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a1719-p102">You can use Microsoft Graph to allow web and mobile applications to read and modify Excel workbooks stored in OneDrive for Business, SharePoint site or Group drive. The `Workbook` (or Excel file) resource contains all the other Excel resources through relationships. You can access a workbook through the [Drive API](drive.md) by identifying the location of the file in the URL. For example:</span></span>

`https://graph.microsoft.com/{version}/me/drive/items/{id}/workbook/`  
`https://graph.microsoft.com/{version}/me/drive/root:/{item-path}:/workbook/`  

<span data-ttu-id="a1719-p103">Puede acceder a un conjunto de objetos de Excel (como una tabla, intervalo o gráfico) mediante las API de REST estándares para crear, leer, actualizar y eliminar operaciones (CRUD) en el libro. Por ejemplo: `GET https://graph.microsoft.com/{version}/me/drive/items/{id}/workbook/worksheets`</span><span class="sxs-lookup"><span data-stu-id="a1719-p103">You can access a set of Excel objects (such as Table, Range, or Chart) by using standard REST APIs to perform  create, read, update, and delete (CRUD) operations on the workbook. For example, `GET https://graph.microsoft.com/{version}/me/drive/items/{id}/workbook/worksheets`</span></span>  
<span data-ttu-id="a1719-113">devuelve una colección de objetos de hoja de cálculo que forman parte del libro.</span><span class="sxs-lookup"><span data-stu-id="a1719-113">returns a collection of worksheet objects that are part of the workbook.</span></span>    


<span data-ttu-id="a1719-p104">La API REST de Excel solo es compatible con libros de formato de archivo Office Open XML. Los libros con la extensión `.xls` no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="a1719-p104">The Excel REST API supports only Office Open XML file formatted workbooks. The `.xls` extension workbooks are not supported.</span></span> 

<span data-ttu-id="a1719-116">**Nota**: Aún no se admiten los libros almacenados en la plataforma para consumidores de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="a1719-116">**Note**: Support for workbooks stored in OneDrive Consumer platform is still not available.</span></span> <span data-ttu-id="a1719-117">En este momento, las API REST de Excel solo admiten los archivos almacenados en la plataforma empresarial.</span><span class="sxs-lookup"><span data-stu-id="a1719-117">At this time, only the files stored in business platform is supported by Excel REST APIs.</span></span> 

## <a name="authorization-and-scopes"></a><span data-ttu-id="a1719-118">Autorización y ámbitos</span><span class="sxs-lookup"><span data-stu-id="a1719-118">Authorization and scopes</span></span>

<span data-ttu-id="a1719-119">Puede usar el [punto de conexión de Azure AD v.2](https://developer.microsoft.com/graph/docs/authorization/converged_auth) para autenticar las API de Excel.</span><span class="sxs-lookup"><span data-stu-id="a1719-119">You can use the [Azure AD v.2 endpoint](https://developer.microsoft.com/graph/docs/authorization/converged_auth) to authenticate Excel APIs.</span></span> <span data-ttu-id="a1719-120">Todas las API requieren el encabezado HTTP `Authorization: Bearer {access-token}`.</span><span class="sxs-lookup"><span data-stu-id="a1719-120">All APIs require the `Authorization: Bearer {access-token}` HTTP header.</span></span>   
  
<span data-ttu-id="a1719-121">Uno de los siguientes [ámbitos de permiso](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) es necesario para utilizar el recurso de Excel:</span><span class="sxs-lookup"><span data-stu-id="a1719-121">One of the following [permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes) is required to use the Excel resource:</span></span>

* <span data-ttu-id="a1719-122">Files.Read (para acciones de lectura)</span><span class="sxs-lookup"><span data-stu-id="a1719-122">Files.Read (for read actions)</span></span>
* <span data-ttu-id="a1719-123">Files.ReadWrite (para acciones de lectura y escritura)</span><span class="sxs-lookup"><span data-stu-id="a1719-123">Files.ReadWrite (for read and write actions)</span></span>


## <a name="sessions-and-persistence"></a><span data-ttu-id="a1719-124">Sesiones y persistencia</span><span class="sxs-lookup"><span data-stu-id="a1719-124">Sessions and persistence</span></span>

<span data-ttu-id="a1719-125">Se puede llamar a las API de Excel de tres modos:</span><span class="sxs-lookup"><span data-stu-id="a1719-125">Excel APIs can be called in one of three modes:</span></span> 

1. <span data-ttu-id="a1719-126">Sesión persistente - Todos los cambios realizados en el libro son persistentes (se guardan).</span><span class="sxs-lookup"><span data-stu-id="a1719-126">Persistent session - All changes made to the workbook are persisted (saved).</span></span> <span data-ttu-id="a1719-127">Este es el modo de operación más eficiente y eficaz.</span><span class="sxs-lookup"><span data-stu-id="a1719-127">This is the most efficient and performant mode of operation.</span></span> 
2. <span data-ttu-id="a1719-p108">Sesión no persistente - Los cambios realizados por la API no se guardan en la ubicación de origen. En su lugar, el servidor backend de Excel conserva una copia temporal del archivo que refleja los cambios realizados durante esa sesión API en concreto. Cuando expira la sesión de Excel, se pierden los cambios. Este modo es útil para aplicaciones que necesitan realizar análisis u obtener los resultados de un cálculo o una imagen de gráfico, pero no afecta al estado de documento.</span><span class="sxs-lookup"><span data-stu-id="a1719-p108">Non-persistent session - Changes made by the API are not saved to the source location. Instead, the Excel backend server keeps a temporary copy of the file that reflects the changes made during that particular API session. When the Excel session expires, the changes are lost. This mode is useful for apps that need to do analysis or obtain the results of a calculation or a chart image, but not affect the document state.</span></span> 
3. <span data-ttu-id="a1719-132">Sin sesión - Se realiza la llamada a la API sin información de la sesión.</span><span class="sxs-lookup"><span data-stu-id="a1719-132">Sessionless - The API call is made without session information.</span></span> <span data-ttu-id="a1719-133">Los servidores de Excel tienen que localizar la copia del libro del servidor cada vez que se realiza la operación y, por tanto, no es una forma eficaz de llamar a las API de Excel.</span><span class="sxs-lookup"><span data-stu-id="a1719-133">Excel servers have to locate the server's copy of the workbook each time to perform the operation and hence this is not an efficient way for call Excel APIs.</span></span> <span data-ttu-id="a1719-134">Es adecuada para hacer solicitudes únicas.</span><span class="sxs-lookup"><span data-stu-id="a1719-134">It is suitable for making one off requests.</span></span> 

<span data-ttu-id="a1719-135">Para representar la sesión en la API, utilice el encabezado `workbook-session-id: {session-id}`.</span><span class="sxs-lookup"><span data-stu-id="a1719-135">To represent the session in the API, use the `workbook-session-id: {session-id}` header.</span></span> 

><span data-ttu-id="a1719-p110">**Nota:** El encabezado de sesión no es necesario para que funcione una API de Excel. Sin embargo, recomendamos que utilice el encabezado de sesión para mejorar el rendimiento. Si no utiliza un encabezado de sesión, los cambios realizados durante la llamada API _sí_ persisten en el archivo.</span><span class="sxs-lookup"><span data-stu-id="a1719-p110">**Note:** The session header is not required for an Excel API to work. However, we recommend that you use the session header to improve performance. If you don't use a session header, changes made during the API call _are_ persisted to the file.</span></span>  

### <a name="api-call-to-get-a-session"></a><span data-ttu-id="a1719-139">Llamada API para obtener una sesión</span><span class="sxs-lookup"><span data-stu-id="a1719-139">API call to get a session</span></span> 

#### <a name="request"></a><span data-ttu-id="a1719-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1719-140">Request</span></span> 

<span data-ttu-id="a1719-141">Transmita un objeto JSON estableciendo el valor `persistchanges` en `true` o `false`.</span><span class="sxs-lookup"><span data-stu-id="a1719-141">Pass a JSON object by setting the `persistchanges` value to `true` or `false`.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
POST /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/createSession
content-type: Application/Json 
authorization: Bearer {access-token}

{ "persistChanges": true }
```

<span data-ttu-id="a1719-142">Cuando el valor de `persistChanges` se establece como `false`, se devuelve un identificador de sesión no persistente.</span><span class="sxs-lookup"><span data-stu-id="a1719-142">When the value of `persistChanges` is set to `false`, a non-persistent session id is returned.</span></span>  


#### <a name="response"></a><span data-ttu-id="a1719-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-143">Response</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 201 Created
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#microsoft.graph.sessionInfo",
  "id": "{session-id}",
  "persistChanges": true
}
```

#### <a name="usage"></a><span data-ttu-id="a1719-144">Uso</span><span class="sxs-lookup"><span data-stu-id="a1719-144">Usage</span></span> 

<span data-ttu-id="a1719-145">El identificador de sesión devuelto de la llamada anterior se pasa como un encabezado en las subsiguientes solicitudes API en</span><span class="sxs-lookup"><span data-stu-id="a1719-145">The session ID returned from the previous call is passed as a header on subsequent API requests in</span></span>  
<span data-ttu-id="a1719-146">el encabezado HTTP `workbook-session-id`.</span><span class="sxs-lookup"><span data-stu-id="a1719-146">`workbook-session-id` HTTP header.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

><span data-ttu-id="a1719-147">Nota: Si el identificador de sesión ha caducado, se devuelve un código de error HTTP `404` en la sesión.</span><span class="sxs-lookup"><span data-stu-id="a1719-147">Note: If the session id has expired, a `404` HTTP error code is returned on the session.</span></span> <span data-ttu-id="a1719-148">En este tipo de escenario, puede crear una nueva sesión y continuar.</span><span class="sxs-lookup"><span data-stu-id="a1719-148">In such a scenarion, you can choose to create a new session and continue.</span></span> <span data-ttu-id="a1719-149">Otra solución sería actualizar la sesión periódicamente para mantener la sesión activa.</span><span class="sxs-lookup"><span data-stu-id="a1719-149">Another approach would be to refresh the session periodically to keep the session alive.</span></span> <span data-ttu-id="a1719-150">Normalmente, la sesión persistente caduca después de 7 minutos de inactividad.</span><span class="sxs-lookup"><span data-stu-id="a1719-150">Typically the persistent session expires after about 7 minutes of inactivity.</span></span> <span data-ttu-id="a1719-151">La sesión no persistente caduca después de 5 minutos de inactividad.</span><span class="sxs-lookup"><span data-stu-id="a1719-151">Non persistent session expires after about 5 minutes of inactivity.</span></span> 

## <a name="common-excel-scenarios"></a><span data-ttu-id="a1719-152">Escenarios comunes de Excel</span><span class="sxs-lookup"><span data-stu-id="a1719-152">Common Excel scenarios</span></span>

<span data-ttu-id="a1719-153">Esta sección proporciona ejemplos de las operaciones comunes que puede utilizar en objetos de Excel.</span><span class="sxs-lookup"><span data-stu-id="a1719-153">This section provides examples of the common operations you can use on Excel objects.</span></span>

### <a name="worksheet-operations"></a><span data-ttu-id="a1719-154">Operaciones de hojas de cálculo</span><span class="sxs-lookup"><span data-stu-id="a1719-154">Worksheet operations</span></span>

#### <a name="list-worksheets-part-of-the-workbook"></a><span data-ttu-id="a1719-155">Enumerar las hojas de cálculo que forman parte del libro</span><span class="sxs-lookup"><span data-stu-id="a1719-155">List worksheets part of the workbook</span></span> 
<span data-ttu-id="a1719-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1719-156">Request</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets
accept: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-157">Response</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets",
  "value": [
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets(%27%7B00000000-0001-0000-0000-000000000000%7D%27)",
      "id": "{00000000-0001-0000-0000-000000000000}",
      "name": "Sheet1",
      "position": 0,
      "visibility": "Visible"
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets(%27%7B00000000-0001-0000-0100-000000000000%7D%27)",
      "id": "{00000000-0001-0000-0100-000000000000}",
      "name": "Sheet57664",
      "position": 1,
      "visibility": "Visible"
    }
  ]
}
```
#### <a name="add-a-new-worksheet"></a><span data-ttu-id="a1719-158">Agregar una hoja de cálculo nueva</span><span class="sxs-lookup"><span data-stu-id="a1719-158">Add a new worksheet</span></span> 
 
<!-- { "blockType": "ignored" } -->
```http
POST /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{ "name": "Sheet32243" }
```

<span data-ttu-id="a1719-159">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-159">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 201 Created
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets/$entity",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets(%27%7B75A18F35-34AA-4F44-97CC-FDC3C05D9F40%7D%27)",
  "id": "{75A18F35-34AA-4F44-97CC-FDC3C05D9F40}",
  "name": "Sheet32243",
  "position": 5,
  "visibility": "Visible"
}
```

#### <a name="get-a-new-worksheet"></a><span data-ttu-id="a1719-160">Obtener una hoja de cálculo nueva</span><span class="sxs-lookup"><span data-stu-id="a1719-160">Get a new worksheet</span></span> 

<span data-ttu-id="a1719-161">Obtener una hoja de cálculo basada en el nombre.</span><span class="sxs-lookup"><span data-stu-id="a1719-161">Get a worksheet based on the name.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets/Sheet32243
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-162">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-162">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets/$entity",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets(%27%7B75A18F35-34AA-4F44-97CC-FDC3C05D9F40%7D%27)",
  "id": "{75A18F35-34AA-4F44-97CC-FDC3C05D9F40}",
  "name": "Sheet32243",
  "position": 5,
  "visibility": "Visible"
}
```

<span data-ttu-id="a1719-p112">\*\* Nota: Las hojas de cálculo también pueden recuperarse con el id. Sin embargo, actualmente el id. contiene caracteres `{` y '}', y debe codificarse con URL para que funcione la API. Ejemplo: Para obtener una hoja de cálculo con id. de `{75A18F35-34AA-4F44-97CC-FDC3C05D9F40}`, codifique con URL el id. de la ruta como `/workbook/worksheets/%7B75A18F35-34AA-4F44-97CC-FDC3C05D9F40%7D`.</span><span class="sxs-lookup"><span data-stu-id="a1719-p112">\*\* Note: Worksheets can also be retrieved using the ID. However, currently the ID contains `{` and '}' characters, which needs to be URL encoded for the API to work. Example: In order to get a worksheet with ID of `{75A18F35-34AA-4F44-97CC-FDC3C05D9F40}`, URL encode the ID in the path as `/workbook/worksheets/%7B75A18F35-34AA-4F44-97CC-FDC3C05D9F40%7D`.</span></span> 

#### <a name="delete-a-worksheet"></a><span data-ttu-id="a1719-166">Eliminar una hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="a1719-166">Delete a worksheet</span></span>

<span data-ttu-id="a1719-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1719-167">Request</span></span>
```
DELETE /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets('%7B75A18F35-34AA-4F44-97CC-FDC3C05D9F40%7D')
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-168">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-168">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 204 No Content
```


#### <a name="update-worksheet-properties"></a><span data-ttu-id="a1719-169">Actualizar las propiedades de la hoja de cálculo</span><span class="sxs-lookup"><span data-stu-id="a1719-169">Update worksheet properties</span></span>

<span data-ttu-id="a1719-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1719-170">Request</span></span> 

```
PATCH /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets/SheetA
content-type: Application/Json 
accept: application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{ "name": "SheetA", "position": 3 }
```

<span data-ttu-id="a1719-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-171">Response</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets/$entity",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN')/workbook/worksheets(%27%7B00000000-0001-0000-0100-000000000000%7D%27)",
  "id": "{00000000-0001-0000-0100-000000000000}",
  "name": "SheetA",
  "position": 3,
  "visibility": "Visible"
}
```

### <a name="chart-operations"></a><span data-ttu-id="a1719-172">Operaciones de gráficos</span><span class="sxs-lookup"><span data-stu-id="a1719-172">Chart operations</span></span>

#### <a name="list-charts-that-are-part-of-the-worksheet"></a><span data-ttu-id="a1719-173">Enumerar los gráficos que forman parte de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a1719-173">List charts that are part of the worksheet</span></span> 

<span data-ttu-id="a1719-174">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-174">Request <!-- { "blockType": "ignored" } --></span></span>
```http 
GET /{version}/me/drive/items/01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL/workbook/worksheets('%7B00000000-0001-0000-0000-000000000000%7D')/charts
accept: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id} 
```

<span data-ttu-id="a1719-175">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-175">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL')/workbook/worksheets('%7B00000000-0001-0000-0000-000000000000%7D')/charts",
  "value": [
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL')/workbook/worksheets(%27%7B00000000-0001-0000-0000-000000000000%7D%27)/charts(%27%7B00000000-0008-0000-0100-000003000000%7D%27)",
      "height": 235.5,
      "id": "{00000000-0008-0000-0100-000003000000}",
      "left": 276.0,
      "name": "Chart 2",
      "top": 0.0,
      "width": 401.25
   }
  ]
}
```

<span data-ttu-id="a1719-p113">\*\* Nota: El id. de gráfico contiene caracteres `{` y `}` (ejemplo: `{00000000-0008-0000-0100-000003000000}`), y debe codificarse con URL para que funcione la API. Ejemplo: Para obtener un objeto de gráfico, codifique con URL el id. de la ruta como `/charts/%7B00000000-0008-0000-0100-000003000000%7D`.</span><span class="sxs-lookup"><span data-stu-id="a1719-p113">\*\* Note: Chart ID contains `{` and `}` characters (example: `{00000000-0008-0000-0100-000003000000}`), which needs to be URL encoded for the API to work. Example: In order to get a chart object, URL encode the ID in the path as `/charts/%7B00000000-0008-0000-0100-000003000000%7D`.</span></span> 

#### <a name="get-chart-image"></a><span data-ttu-id="a1719-178">Obtener imagen de gráfico</span><span class="sxs-lookup"><span data-stu-id="a1719-178">Get chart image</span></span>

<span data-ttu-id="a1719-179">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-179">Request <!-- { "blockType": "ignored" } --></span></span>
```http
GET /{version}/me/drive/items/01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL/workbook/worksheets('%7B00000000-0001-0000-0000-000000000000%7D')/charts('%7B00000000-0008-0000-0100-000003000000%7D')/Image(width=0,height=0,fittingMode='fit')
authorization: Bearer {access-token} 
workbook-session-id: {session-id} 
```

<span data-ttu-id="a1719-180">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-180">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#Edm.String",
  "value": "{base-64-string}"
}
```

#### <a name="add-a-chart"></a><span data-ttu-id="a1719-181">Agregar un gráfico</span><span class="sxs-lookup"><span data-stu-id="a1719-181">Add a chart</span></span>  

<span data-ttu-id="a1719-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1719-182">Request</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /{version}/me/drive/items/01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL/workbook/worksheets('%7B00000000-0001-0000-0000-000000000000%7D')/charts/Add
content-type: Application/Json 
accept: application/Json 
authorization: Bearer {access-token} 

{ "type": "ColumnClustered", "sourcedata": "A1:C4", "seriesby": "Auto" }
```

<span data-ttu-id="a1719-183">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-183">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 201 Created
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#chart",
  "@odata.type": "#microsoft.graph.workbookChart",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL')/workbook/worksheets(%27%7B00000000-0001-0000-0000-000000000000%7D%27)/charts(%27%7B2D421098-FA19-41F7-8528-EE7B00E4BB42%7D%27)",
  "height": 216.0,
  "id": "{2D421098-FA19-41F7-8528-EE7B00E4BB42}",
  "left": 0.0,
  "name": "Chart 2",
  "top": 0.0,
  "width": 360.0
}
```

#### <a name="update-a-chart"></a><span data-ttu-id="a1719-184">Actualizar un gráfico</span><span class="sxs-lookup"><span data-stu-id="a1719-184">Update a chart</span></span>

<!-- { "blockType": "ignored" } -->
```http 
PATCH /{version}/me/drive/items/01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL/workbook/worksheets('%7B00000000-0001-0000-0000-000000000000%7D')/charts('%7B2D421098-FA19-41F7-8528-EE7B00E4BB42%7D')
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{ "height": 216.0, "left": 0, "name": "NewName", "top": 0, "width": 360.0 }

```
<span data-ttu-id="a1719-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-185">Response</span></span> 

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL')/workbook/worksheets('%7B00000000-0001-0000-0000-000000000000%7D')/charts/$entity",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL')/workbook/worksheets(%27%7B00000000-0001-0000-0000-000000000000%7D%27)/charts(%27%7B2D421098-FA19-41F7-8528-EE7B00E4BB42%7D%27)",
  "height": 216.0,
  "id": "{2D421098-FA19-41F7-8528-EE7B00E4BB42}",
  "left": 0.0,
  "name": "NewName",
  "top": 0.0,
  "width": 360.0
}
```

#### <a name="update-chart-source-data"></a><span data-ttu-id="a1719-186">Actualizar los datos de origen del gráfico</span><span class="sxs-lookup"><span data-stu-id="a1719-186">Update chart source data</span></span> 

<span data-ttu-id="a1719-187">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-187">Request <!-- { "blockType": "ignored" } --></span></span>
```http
POST /{version}/me/drive/items/01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL/workbook/worksheets('%7B00000000-0001-0000-0000-000000000000%7D')/charts('%7B2D421098-FA19-41F7-8528-EE7B00E4BB42%7D')/setData
content-type: Application/Json 
accept: application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{ "sourceData": "A1:C4", "seriesBy": "Auto" }
```

<span data-ttu-id="a1719-188">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-188">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 204 No Content
```

### <a name="table-operations"></a><span data-ttu-id="a1719-189">Operaciones de tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-189">Table operations</span></span> 

#### <a name="get-list-of-tables"></a><span data-ttu-id="a1719-190">Obtener una lista de tablas</span><span class="sxs-lookup"><span data-stu-id="a1719-190">Get list of tables</span></span> 

<span data-ttu-id="a1719-191">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-191">Request <!-- { "blockType": "ignored" } --></span></span>
```http
GET /{version}/me/drive/items/01CYZLFJB6K563VVUU2ZC2FJBAHLSZZQXL/workbook/worksheets('%7B00000000-0001-0000-0000-000000000000%7D')/tables
accept: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-192">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-192">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 
```

#### <a name="create-table"></a><span data-ttu-id="a1719-193">Crear tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-193">Create table</span></span>

<span data-ttu-id="a1719-194">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-194">Request <!-- { "blockType": "ignored" } --></span></span>
```http 
POST /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables/{table-id}/add
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{ "name": "NewTableName", "hasHeaders": true, "showTotals": false, "style": "TableStyleMedium4" }
```

<span data-ttu-id="a1719-195">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-195">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 201 Created
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables/$entity",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%272%27)",
  "id": "2",
  "name": "NewTableName",
  "showHeaders": true,
  "showTotals": false,
  "style": "TableStyleMedium4"
}
```

#### <a name="update-table"></a><span data-ttu-id="a1719-196">Actualizar tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-196">Update table</span></span>

<span data-ttu-id="a1719-197">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-197">Request <!-- { "blockType": "ignored" } --></span></span>
```http 
PATCH /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables('2')
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{ "name": "NewTableName", "showHeaders": true, "showTotals": false, "style": "TableStyleMedium4" }
```

<span data-ttu-id="a1719-198">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-198">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables/$entity",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%272%27)",
  "id": "2",
  "name": "NewTableName",
  "showHeaders": true,
  "showTotals": false,
  "style": "TableStyleMedium4"
}
```

#### <a name="get-list-of-table-rows"></a><span data-ttu-id="a1719-199">Obtener una lista de las filas de la tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-199">Get list of table rows</span></span>
<span data-ttu-id="a1719-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1719-200">Request</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables('4')/rows
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-201">Response</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables('4')/rows",
  "value": [
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/rows/itemAt(0)",
      "index": 0,
      "values": [
        [
          42019,
          53,
          34
       ]
      ]
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/rows/itemAt(1)",
      "index": 1,
      "values": [
        [
          42020,
          45,
          39
        ]
      ]
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/rows/itemAt(2)",
      "index": 2,
      "values": [
        [
          42021,
          50,
          31
        ]
      ]
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/rows/itemAt(3)",
      "index": 3,
      "values": [
        [
          42022,
          43,
          39
        ]
      ]
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/rows/itemAt(4)",
      "index": 4,
      "values": [
        [
          42023,
          45,
          41
        ]
      ]
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/rows/itemAt(5)",
      "index": 5,
      "values": [
        [
          42024,
          52,
          40
        ]
      ]
    }
  ]
}
```

#### <a name="get-list-of-table-columns"></a><span data-ttu-id="a1719-202">Obtener una lista de las columnas de la tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-202">Get list of table columns</span></span>

<span data-ttu-id="a1719-203">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-203">Request <!-- { "blockType": "ignored" } --></span></span>
```http
GET /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables('4')/columns
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-204">Response</span></span> 

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 200 OK 
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables('4')/columns",
  "value": [
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/columns(%271%27)",
      "id": "1",
      "index": 0,
      "name": "Date",
      "values": [
        [
          "Date"
        ],
        [
          42019
       ],
        [
          42020
        ],
        [
          42021
        ],
        [
          42022
        ],
        [
          42023
        ],
        [
          42024
        ]
      ]
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/columns(%272%27)",
      "id": "2",
      "index": 1,
      "name": "High (F)",
      "values": [
        [
          "High (F)"
        ],
        [
          53
        ],
        [
          45
        ],
        [
          50
        ],
        [
          43
        ],
        [
          45
        ],
        [
          52
        ]
      ]
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/columns(%273%27)",
      "id": "3",
      "index": 2,
      "name": "Low (F)",
      "values": [
        [
          "Low (F)"
        ],
        [
          34
        ],
        [
          39
        ],
        [
          31
        ],
        [
          39
        ],
        [
          41
        ],
        [
          40
        ]
      ]
    }
  ]
}
```


#### <a name="add-a-table-row"></a><span data-ttu-id="a1719-205">Agregar una fila a la tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-205">Add a table row</span></span>

<span data-ttu-id="a1719-206">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-206">Request <!-- { "blockType": "ignored" } --></span></span>
```http
POST /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables('4')/rows
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{ "values": [ [ "Jan-15-2016", "49", "37" ] ], "index": null }
```

<span data-ttu-id="a1719-207">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-207">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 201 Created
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables('4')/rows/$entity",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%274%27)/rows(null)",
  "index": 6,
  "values": [
    [
      "Jan-15-2016",
      49,
      37
    ]
  ]
}
```

#### <a name="add-a-table-column"></a><span data-ttu-id="a1719-208">Agregar una columna a la tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-208">Add a table column</span></span> 

<span data-ttu-id="a1719-209">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-209">Request <!-- { "blockType": "ignored" } --></span></span>
```http 
POST /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables('2')/columns
content-type: Application/Json 
accept: application/Json 


{ "values": [ [ "Status" ], [ "Open" ], [ "Closed" ] ], "index": 2 }
```

<span data-ttu-id="a1719-210">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-210">Response</span></span> 

<!-- { "blockType": "ignored" } -->
```http 
HTTP code: 201 Created
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables('2')/columns/$entity",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/tables(%272%27)/columns(%274%27)",
  "id": "4",
  "index": 2,
  "name": "Status",
  "values": [
    [
      "Status"
    ],
    [
      "Open"
    ],
    [
      "Closed"
    ]
  ]
}
```

#### <a name="delete-table-row"></a><span data-ttu-id="a1719-211">Eliminar fila de la tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-211">Delete table row</span></span>

<span data-ttu-id="a1719-212">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-212">Request <!-- { "blockType": "ignored" } --></span></span>
```http  
DELETE /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables('4')/rows/$/itemAt(index=6)
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-213">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-213">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 204 No Content
```

#### <a name="delete-table-column"></a><span data-ttu-id="a1719-214">Eliminar columna de la tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-214">Delete table column</span></span> 
<span data-ttu-id="a1719-215">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-215">Request <!-- { "blockType": "ignored" } --></span></span>
```http
DELETE /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables('4')/columns('3')
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-216">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-216">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 204 No Content
```

#### <a name="convert-table-to-range"></a><span data-ttu-id="a1719-217">Convertir tabla a intervalo</span><span class="sxs-lookup"><span data-stu-id="a1719-217">Convert table to range</span></span> 
<span data-ttu-id="a1719-218">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-218">Request <!-- { "blockType": "ignored" } --></span></span>
```http
POST /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/tables('1')/convertToRange
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-219">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-219">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 200 OK 
content-type: application/json;odata.metadata 
```

#### <a name="table-sort"></a><span data-ttu-id="a1719-220">Ordenar tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-220">Table sort</span></span>
<span data-ttu-id="a1719-221">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-221">Request <!-- { "blockType": "ignored" } --></span></span>
```http
POST /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets('Sheet15799')/tables('table2')/sort/apply
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{
"fields" : [
  { "key": 0,
   "ascending": true
  }
]
}
```


<span data-ttu-id="a1719-222">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-222">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 204 No Content
```

#### <a name="table-filter"></a><span data-ttu-id="a1719-223">Filtro de tabla</span><span class="sxs-lookup"><span data-stu-id="a1719-223">Table filter</span></span>
<span data-ttu-id="a1719-224">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-224">Request <!-- { "blockType": "ignored" } --></span></span>
```http
POST /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets('Sheet15799')/tables('table2')/columns(id='2')/filter/apply
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{
"criteria" : 
  { "filterOn": "custom",
   "criterion1": ">15",
   "operator": "and",
   "criterion2": "<50"
   
  }
}
```

<span data-ttu-id="a1719-225">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-225">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 204 No Content
```


#### <a name="clear-filter"></a><span data-ttu-id="a1719-226">Borrar filtro</span><span class="sxs-lookup"><span data-stu-id="a1719-226">Clear filter</span></span>
<span data-ttu-id="a1719-227">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-227">Request <!-- { "blockType": "ignored" } --></span></span>
```http
POST /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets('Sheet15799')/tables('table2')/columns(id='2')/filter/clear
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-228">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-228">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 204 No Content
```

### <a name="range-operations"></a><span data-ttu-id="a1719-229">Operaciones de intervalo</span><span class="sxs-lookup"><span data-stu-id="a1719-229">Range operations</span></span>

#### <a name="get-range"></a><span data-ttu-id="a1719-230">Obtener intervalo</span><span class="sxs-lookup"><span data-stu-id="a1719-230">Get Range</span></span> 

<span data-ttu-id="a1719-231">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-231">Request <!-- { "blockType": "ignored" } --></span></span>
```http
GET /{version}/me/drive/items/{item-id}/workbook/worksheets/{worksheet-id}/range(address='A1:B2')
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-232">Response</span></span> 

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#range",
  "@odata.type": "#microsoft.graph.workbookRange",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/worksheets(%27%7B00000000-0001-0000-0300-000000000000%7D%27)/range(address=%27A1:B2%27)",
  "address": "test!A1:B2",
  "addressLocal": "test!A1:B2",
  "cellCount": 4,
  "columnCount": 2,
  "columnHidden": false,
  "columnIndex": 0,
  "formulas": [
    [
      "",
      ""
    ],
    [
      "",
      ""
    ]
  ],
  "formulasLocal": [
    [
      "",
      ""
    ],
    [
      "",
      ""
    ]
  ],
  "formulasR1C1": [
    [
      "",
      ""
    ],
    [
      "",
      ""
    ]
  ],
  "hidden": false,
  "numberFormat": [
    [
      "General",
      "General"
    ],
    [
      "General",
      "General"
    ]
  ],
  "rowCount": 2,
  "rowHidden": false,
  "rowIndex": 0,
  "text": [
    [
      "",
      ""
    ],
    [
      "",
      ""
    ]
  ],
  "values": [
    [
      "",
      ""
    ],
    [
      "",
      ""
    ]
  ],
  "valueTypes": [
    [
      "Empty",
      "Empty"
    ],
    [
      "Empty",
      "Empty"
    ]
  ]
}
```

#### <a name="range-update"></a><span data-ttu-id="a1719-233">Actualizar intervalo</span><span class="sxs-lookup"><span data-stu-id="a1719-233">Range update</span></span> 

<!-- { "blockType": "ignored" } -->
```http
PATCH /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/worksheets('test')/range(address='test!A1:B2')
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{ "values": [ [ "Test", "Value" ], [ "For", "Update" ] ] }
```

<!-- { "blockType": "ignored" } -->
```http
HTTP code: 200 OK
content-type: application/json;odata.metadata

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#range",
  "@odata.type": "#microsoft.graph.workbookRange",
  "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/worksheets(%27%7B00000000-0001-0000-0300-000000000000%7D%27)/range(address=%27test!A1:B2%27)",
  "address": "test!A1:B2",
  "addressLocal": "test!A1:B2",
  "cellCount": 4,
  "columnCount": 2,
  "columnHidden": false,
  "columnIndex": 0,
  "formulas": [
    [
      "Test",
      "Value"
    ],
    [
      "For",
      "Update"
    ]
  ],
  "formulasLocal": [
    [
      "Test",
      "Value"
    ],
    [
      "For",
      "Update"
    ]
  ],
  "formulasR1C1": [
    [
      "Test",
      "Value"
    ],
    [
      "For",
      "Update"
    ]
  ],
  "hidden": false,
  "numberFormat": [
    [
      "General",
      "General"
    ],
    [
      "General",
      "General"
    ]
  ],
  "rowCount": 2,
  "rowHidden": false,
  "rowIndex": 0,
  "text": [
    [
      "Test",
      "Value"
    ],
    [
      "For",
      "Update"
    ]
  ],
  "values": [
    [
      "Test",
      "Value"
    ],
    [
      "For",
      "Update"
    ]
  ],
  "valueTypes": [
    [
      "String",
      "String"
    ],
    [
      "String",
      "String"
    ]
  ]
}
```

#### <a name="range-sort"></a><span data-ttu-id="a1719-234">Ordenar intervalo</span><span class="sxs-lookup"><span data-stu-id="a1719-234">Range sort</span></span>
<span data-ttu-id="a1719-235">Solicitud<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-235">Request <!-- { "blockType": "ignored" } --></span></span>
```http
POST /{version}/me/drive/items/01CYZLFJGUJ7JHBSZDFZFL25KSZGQTVAUN/workbook/worksheets('Sheet15799')/usedRange/sort/apply
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{
"fields" : [
  { "key": 0,
   "ascending": true
  }
]
}
```

<span data-ttu-id="a1719-236">Respuesta<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a1719-236">Response <!-- { "blockType": "ignored" } --></span></span>
```http
HTTP code: 204 No Content
```


### <a name="named-items"></a><span data-ttu-id="a1719-237">Elementos con nombre</span><span class="sxs-lookup"><span data-stu-id="a1719-237">Named items</span></span>
<span data-ttu-id="a1719-238">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1719-238">Request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /{version}/me/drive/items/01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4/workbook/names
authorization: Bearer {access-token} 
workbook-session-id: {session-id}
```

<span data-ttu-id="a1719-239">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-239">Response</span></span> 

<!-- { "blockType": "ignored" } -->
```http 
HTTP code: 200 OK
content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/{version}/$metadata#users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/names",
  "value": [
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/names(%27data%27)",
      "name": "data",
      "type": "Range",
      "value": "Range!$A$1:$D$3",
      "visible": true
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/names(%27myrange%27)",
      "name": "myrange",
      "type": "Range",
      "value": "Range!$E$1:$F$7",
      "visible": true
    },
    {
      "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/items('01CYZLFJDYBLIGAE7G5FE3I4VO2XP7BLU4')/workbook/names(%27range1%27)",
      "name": "range1",
      "type": "Range",
      "value": "Range!$I$1:$M$11",
      "visible": true
    }
  ]
}
```

### <a name="work-with-nulls"></a><span data-ttu-id="a1719-240">Trabajar con valores NULL</span><span class="sxs-lookup"><span data-stu-id="a1719-240">Work with nulls</span></span>

#### <a name="null-input-in-2-d-array"></a><span data-ttu-id="a1719-241">entrada NULL en una matriz bidimensional</span><span class="sxs-lookup"><span data-stu-id="a1719-241">null input in 2-D array</span></span>

<span data-ttu-id="a1719-p114">La entrada `null` dentro de una matriz bidimensional (para valores, formato numérico, fórmulas) se omite en los recursos Range y Table. No se producirá ninguna actualización en el objetivo previsto (celda) cuando la entrada `null` se envíe en valores, en formato numérico o en una cuadrícula de fórmulas de valores.</span><span class="sxs-lookup"><span data-stu-id="a1719-p114">`null` input inside a two-dimensional array (for values, number-format, formula) is ignored in the Range and Table resources. No update will take place to the intended target (cell) when `null` input is sent in values or number-format or formula grid of values.</span></span>

<span data-ttu-id="a1719-244">Por ejemplo, para actualizar solamente partes específicas del intervalo, como el formato numérico de una celda, y conservar el formato numérico existente en otras partes del intervalo, establezca el formato numérico donde sea necesario y envíe `null` para las demás celdas.</span><span class="sxs-lookup"><span data-stu-id="a1719-244">For example, to only update specific parts of the Range, such as a cell's Number Format, and to retain the existing number-format on other parts of the Range, set the Number Format where needed and send `null` for the other cells.</span></span>

<span data-ttu-id="a1719-245">En la siguiente solicitud de establecimiento, solo se establecen algunas partes del formato numérico de intervalo, mientras se conserva el formato numérico existente en la parte restante (pasando valores NULL).</span><span class="sxs-lookup"><span data-stu-id="a1719-245">In the following set request, only some parts of the Range Number Format are set while the existing Number Format on the remaining part is retained (by passing nulls).</span></span>

```json
{
  "values" : [["Eurasia", "29.96", "0.25", "15-Feb" ]],
  "numberFormat" : [[null, null, null, "m/d/yyyy;@"]]
}
```

#### <a name="null-input-for-a-property"></a><span data-ttu-id="a1719-246">entrada NULL para una propiedad</span><span class="sxs-lookup"><span data-stu-id="a1719-246">null input for a property</span></span>

<span data-ttu-id="a1719-p115">`null` no es una entrada única válida para toda la propiedad. Por ejemplo, lo que se muestra a continuación no es válido, ya que no es posible establecer todos los valores como NULL u omitirlos.</span><span class="sxs-lookup"><span data-stu-id="a1719-p115">`null` is not a valid single input for the entire property. For example, the following is not valid because the entire values cannot be set to null or ignored.</span></span>

```json
{
"values":  null
}

```

<span data-ttu-id="a1719-249">Lo que se muestra a continuación tampoco es válido, ya que NULL no es un valor de color válido.</span><span class="sxs-lookup"><span data-stu-id="a1719-249">The following is not valid either as null is not a valid color value.</span></span>

```json
{
"color" :  null
}
```

#### <a name="null-response"></a><span data-ttu-id="a1719-250">Respuesta NULL</span><span class="sxs-lookup"><span data-stu-id="a1719-250">Null-Response</span></span>

<span data-ttu-id="a1719-251">La representación de propiedades de formato con valores no uniformes produce la devolución de un valor NULL en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1719-251">Representation of formatting properties that consists of non-uniform values results in the return of a null value in the response.</span></span>

<span data-ttu-id="a1719-p116">Por ejemplo, un intervalo puede consistir en una o más celdas. En los casos en los que las celdas individuales contenidas en el intervalo especificado no tienen valores de formato uniformes, la representación del nivel del intervalo será indefinida.</span><span class="sxs-lookup"><span data-stu-id="a1719-p116">For example, a Range can consist of one or more cells. In cases where the individual cells contained in the Range specified don't have uniform formatting values, the range level representation will be undefined.</span></span>

```json
{
  "size: : null,
  "color" : null
}
```


### <a name="blank-input-and-output"></a><span data-ttu-id="a1719-254">Entrada y salida en blanco</span><span class="sxs-lookup"><span data-stu-id="a1719-254">Blank input and output</span></span>

<span data-ttu-id="a1719-p117">Los valores en blanco en las solicitudes de actualización se tratan como una instrucción para borrar o restablecer la propiedad correspondiente. Un valor en blanco se representa mediante dos comillas dobles sin espacio en medio: `""`</span><span class="sxs-lookup"><span data-stu-id="a1719-p117">Blank values in update requests are treated as an instruction to clear or reset the respective property. A blank value is represented by two double quotation marks with no space in-between: `""`</span></span>

<span data-ttu-id="a1719-257">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="a1719-257">Examples:</span></span>

* <span data-ttu-id="a1719-258">En el caso de `values`, el valor del rango se borra. Esto equivale a borrar el contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1719-258">For `values`, the range value is cleared out. This is the same as clearing the contents in the application.</span></span>

* <span data-ttu-id="a1719-259">En el caso de `numberFormat`, el formato numérico se establece en `General`.</span><span class="sxs-lookup"><span data-stu-id="a1719-259">For `numberFormat`, the number format is set to `General`.</span></span>

* <span data-ttu-id="a1719-260">En cuanto a `formula` y `formulaLocale`, los valores de la fórmula se borran.</span><span class="sxs-lookup"><span data-stu-id="a1719-260">For `formula` and `formulaLocale`, the formula values are cleared.</span></span>


<span data-ttu-id="a1719-p118">En las operaciones de lectura, lo que cabe esperar es recibir valores en blanco si el contenido de las celdas está en blanco. Si la celda no contiene datos ni valores, la API devuelve un valor en blanco. Un valor en blanco se representa mediante dos comillas dobles sin espacio en medio: `""`</span><span class="sxs-lookup"><span data-stu-id="a1719-p118">For read operations, expect to receive blank values if the contents of the cells are blanks. If the cell contains no data or value, the API returns a blank value. Blank value is represented by two double quotation marks with no space in-between: `""`</span></span>

```json
{
  "values" : [["", "some", "data", "in", "other", "cells", ""]]
}
```

```json
{
  "formula" : [["", "", "=Rand()"]]
}
```


### <a name="unbounded-range"></a><span data-ttu-id="a1719-264">Intervalo sin delimitar</span><span class="sxs-lookup"><span data-stu-id="a1719-264">Unbounded Range</span></span>

#### <a name="read"></a><span data-ttu-id="a1719-265">Lectura</span><span class="sxs-lookup"><span data-stu-id="a1719-265">Read</span></span>

<span data-ttu-id="a1719-266">Una dirección de intervalo sin delimitar solo contiene identificadores de columna o fila e identificadores de fila o columna no especificadas (respectivamente), tales como:</span><span class="sxs-lookup"><span data-stu-id="a1719-266">Unbounded Range address contains only column or row identifiers and unspecified row identifier or column identifiers (respectively), such as:</span></span>

* <span data-ttu-id="a1719-267">`C:C`, `A:F`, `A:XFD` (contiene filas no especificadas)</span><span class="sxs-lookup"><span data-stu-id="a1719-267">`C:C`, `A:F`, `A:XFD` (contains unspecified rows)</span></span>
* <span data-ttu-id="a1719-268">`2:2`, `1:4`, `1:1048546` (contiene columnas no especificadas)</span><span class="sxs-lookup"><span data-stu-id="a1719-268">`2:2`, `1:4`, `1:1048546` (contains unspecified columns)</span></span>

<span data-ttu-id="a1719-p119">Cuando la API realiza una solicitud para recuperar un intervalo sin delimitar (`getRange('C:C')`), la respuesta devuelta contiene `null` para las propiedades de nivel de celda, como `values`, `text`, `numberFormat` o `formula`. Otras propiedades de intervalo como `address` o `cellCount` reflejarán el intervalo sin delimitar.</span><span class="sxs-lookup"><span data-stu-id="a1719-p119">When the API makes a request to retrieve an unbounded Range (`getRange('C:C')`), the response returned contains `null` for cell-level properties such as `values`, `text`, `numberFormat`, or `formula`. Other Range properties such as `address` or `cellCount` will reflect the unbounded range.</span></span>

#### <a name="write"></a><span data-ttu-id="a1719-271">Write</span><span class="sxs-lookup"><span data-stu-id="a1719-271">Write</span></span>

<span data-ttu-id="a1719-272">El establecimiento de propiedades de nivel de celda (como valores, formato numérico, etc.) en el intervalo sin delimitar **no está permitido**, ya que la solicitud de entrada podría ser demasiado grande para controlarla.</span><span class="sxs-lookup"><span data-stu-id="a1719-272">Setting cell level properties (such as values, numberFormat, etc.) on unbounded Range is **not allowed** because the input request might be too large to handle.</span></span>

<span data-ttu-id="a1719-273">Por ejemplo, lo que se muestra a continuación no es una solicitud de actualización válida porque el intervalo solicitado está sin delimitar.</span><span class="sxs-lookup"><span data-stu-id="a1719-273">For example, the following is not a valid update request because the requested range is unbounded.</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id}/range(address="A:B")

{
  "values" : "Due Date"
}
```

<span data-ttu-id="a1719-274">Cuando se intenta realizar una operación de actualización en un intervalo así, la API devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="a1719-274">When an update operation is attempted on such a Range, the API will return an error.</span></span>


### <a name="large-range"></a><span data-ttu-id="a1719-275">Intervalo grande</span><span class="sxs-lookup"><span data-stu-id="a1719-275">Large Range</span></span>

<span data-ttu-id="a1719-p120">Un intervalo grande es aquel cuyo tamaño es demasiado grande para una sola llamada API. Numerosos factores contenidos en el intervalo, como el número de celdas, los valores, el formato numérico y las fórmulas, pueden hacer que la respuesta sea tan grande que resulte inadecuada para la interacción con la API. La API hace lo que puede para devolver o escribir en los datos solicitados. Sin embargo, el gran tamaño puede generar una condición de error de la API debido al elevado uso de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1719-p120">Large Range implies a Range of a size that is too large for a single API call. Many factors such as number of cells, values, numberFormat, and formulas contained in the range can make the response so large that it becomes unsuitable for API interaction. The API makes a best attempt to return or write to the requested data. However, the large size involved might result in an API error condition because of the large resource utilization.</span></span>

<span data-ttu-id="a1719-280">Para evitarlo, recomendamos la lectura o la escritura del intervalo grande en varios tamaños de intervalo pequeños.</span><span class="sxs-lookup"><span data-stu-id="a1719-280">To avoid this, we recommend that you read or write for large Range in multiple smaller range sizes.</span></span>


### <a name="single-input-copy"></a><span data-ttu-id="a1719-281">Copia de entrada única</span><span class="sxs-lookup"><span data-stu-id="a1719-281">Single input copy</span></span>

<span data-ttu-id="a1719-p121">Para poder actualizar un intervalo con los mismos valores o formato numérico o aplicar la misma fórmula en un intervalo, se usa la siguiente convención en la API establecida. En Excel, este comportamiento es similar a la entrada de valores o fórmulas en un intervalo en el modo CTRL+ENTRAR.</span><span class="sxs-lookup"><span data-stu-id="a1719-p121">To support updating a range with the same values or number-format or applying same formula across a range, the following convention is used in the set API. In Excel, this behavior is similar to inputting values or formulas to a range in the CTRL+Enter mode.</span></span>

<span data-ttu-id="a1719-284">La API buscará un *valor de celda único* y, si la dimensión del intervalo de destino no coincide con la dimensión del intervalo de entrada, aplicará la actualización a todo el intervalo en el modo CTRL+ENTRAR con el valor o la fórmula proporcionados en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1719-284">The API will look for a *single cell value* and, if the target range dimension doesn't match the input range dimension, it will apply the update to the entire range in the CTRL+Enter model with the value or formula provided in the request.</span></span>

#### <a name="examples"></a><span data-ttu-id="a1719-285">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a1719-285">Examples</span></span>

<span data-ttu-id="a1719-p122">La siguiente solicitud actualiza el intervalo seleccionado con el texto "Sample text". Tenga en cuenta que el intervalo tiene 200 celdas, mientras que el texto proporcionado solo tiene un valor de celda.</span><span class="sxs-lookup"><span data-stu-id="a1719-p122">The following request updates the selected range with the text of "Sample text". Note that Range has 200 cells, whereas the provided input only has 1 cell value.</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id}/range(address="A1:B00")

{
  "values" : "Sample text"
}
```

### <a name="workbook-functions"></a><span data-ttu-id="a1719-288">Funciones de libro</span><span class="sxs-lookup"><span data-stu-id="a1719-288">Workbook functions</span></span> 
<span data-ttu-id="a1719-289">Puede acceder a las funciones del libro a través de una colección de funciones incluidas en el recurso /Functions.</span><span class="sxs-lookup"><span data-stu-id="a1719-289">You can access the workbook functions through a collection of functions included in the /Functions resource.</span></span> 

<!-- LG: Where is the Functions resource? We should link to this.
-->
##### <a name="request"></a><span data-ttu-id="a1719-290">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1719-290">Request</span></span>
<!-- { "blockType": "ignored" } -->
```http
https://graph.microsoft.com/v1.0/me/drive/root:/book1.xlsx:/workbook/functions/pmt
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{
    "rate": 4.5,
    "nper": 12,
    "pv": -1250
}
```


##### <a name="response"></a><span data-ttu-id="a1719-291">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1719-291">Response</span></span> 

<!-- { "blockType": "ignored" } -->
```http 
HTTP code: 200 OK
content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#workbookFunctionResult",
    "@odata.type": "#microsoft.graph.workbookFunctionResult",
    "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/root/workbook/functions/pmt()",
    "error": null,
    "value": 5625.00000734125
}
```

## <a name="error-information"></a><span data-ttu-id="a1719-292">Información de error</span><span class="sxs-lookup"><span data-stu-id="a1719-292">Error information</span></span> 

<span data-ttu-id="a1719-p123">Los errores se devuelven con un código de error HTTP y un objeto de error. Los errores `code` y `message` explican el motivo del error.</span><span class="sxs-lookup"><span data-stu-id="a1719-p123">Errors are returned with an HTTP error code and an error object. An error `code` and `message` explain the reason for the error.</span></span>
 
<span data-ttu-id="a1719-295">A continuación se muestra un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a1719-295">The following is an example.</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 400 Bad Request
Content-Type: application/json

{
  "error": {
    "code": "ItemAlreadyExists",
    "message": "A resource with the same name or identifier already exists.",
    "innerError": {
      "request-id": "214ca7ea-9ea4-442e-9c67-71fdda0a559c",
      "date": "2016-07-28T03:56:09"
    }
  }
}
```

