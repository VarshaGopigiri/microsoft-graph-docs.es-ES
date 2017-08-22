# <a name="workbookpivottable-refresh"></a><span data-ttu-id="71243-101">workbookPivotTable: refresh</span><span class="sxs-lookup"><span data-stu-id="71243-101">workbookPivotTable: refresh</span></span>

<span data-ttu-id="71243-102">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="71243-102">Refreshes the PivotTable.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="71243-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71243-103">Prerequisites</span></span>
<span data-ttu-id="71243-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Files.Read, Files.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="71243-104">The following **scopes** are required to execute this API: _Files.Read, Files.ReadWrite_</span></span>

## <a name="http-request"></a><span data-ttu-id="71243-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71243-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```
## <a name="request-headers"></a><span data-ttu-id="71243-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71243-106">Request headers</span></span>
| <span data-ttu-id="71243-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="71243-107">Name</span></span>       | <span data-ttu-id="71243-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="71243-108">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="71243-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="71243-109">Authorization</span></span>  | <span data-ttu-id="71243-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71243-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="71243-112">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="71243-112">Workbook-Session-Id</span></span>  | <span data-ttu-id="71243-p102">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="71243-p102">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="71243-115">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="71243-115">Request body</span></span>

## <a name="response"></a><span data-ttu-id="71243-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71243-116">Response</span></span>

<span data-ttu-id="71243-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71243-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71243-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71243-119">Example</span></span>
<span data-ttu-id="71243-120">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="71243-120">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="71243-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71243-121">Request</span></span>
<span data-ttu-id="71243-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71243-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookpivottable_refresh"
}-->
```http
POST https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```

##### <a name="response"></a><span data-ttu-id="71243-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71243-123">Response</span></span>
<span data-ttu-id="71243-124">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71243-124">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```
