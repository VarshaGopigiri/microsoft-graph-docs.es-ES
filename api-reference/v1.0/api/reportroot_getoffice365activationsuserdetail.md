# <a name="reportroot-getoffice365activationsuserdetail"></a><span data-ttu-id="4dda4-101">reportRoot: getOffice365ActivationsUserDetail</span><span class="sxs-lookup"><span data-stu-id="4dda4-101">reportRoot: getOffice365ActivationsUserDetail</span></span>

<span data-ttu-id="4dda4-102">Obtiene información sobre qué usuarios activaron Office 365.</span><span class="sxs-lookup"><span data-stu-id="4dda4-102">Get details about users who have activated Office 365.</span></span>

> <span data-ttu-id="4dda4-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Activaciones de Microsoft Office](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span><span class="sxs-lookup"><span data-stu-id="4dda4-103">**Note:** For details about different report views and names, see [Office 365 Reports - Microsoft Office activations](https://support.office.com/client/Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60).</span></span>

## <a name="permissions"></a><span data-ttu-id="4dda4-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="4dda4-104">Permissions</span></span>

<span data-ttu-id="4dda4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4dda4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="4dda4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4dda4-107">Permission type</span></span>                        | <span data-ttu-id="4dda4-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4dda4-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="4dda4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4dda4-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="4dda4-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="4dda4-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="4dda4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4dda4-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4dda4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4dda4-112">Not supported.</span></span>                           |
| <span data-ttu-id="4dda4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4dda4-113">Application</span></span>                            | <span data-ttu-id="4dda4-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="4dda4-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="4dda4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4dda4-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActivationsUserDetail
```

## <a name="request-headers"></a><span data-ttu-id="4dda4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4dda4-116">Request headers</span></span>

| <span data-ttu-id="4dda4-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="4dda4-117">Name</span></span>          | <span data-ttu-id="4dda4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dda4-118">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="4dda4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="4dda4-119">Authorization</span></span> | <span data-ttu-id="4dda4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4dda4-p102">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="4dda4-122">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="4dda4-122">If-None-Match</span></span> | <span data-ttu-id="4dda4-123">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="4dda4-123">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="4dda4-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4dda4-124">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="4dda4-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dda4-125">Response</span></span>

<span data-ttu-id="4dda4-126">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="4dda4-126">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="4dda4-127">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dda4-127">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="4dda4-128">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="4dda4-128">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="4dda4-129">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="4dda4-129">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="4dda4-130">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="4dda4-130">Report Refresh Date</span></span>
- <span data-ttu-id="4dda4-131">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="4dda4-131">User Principal Name</span></span>
- <span data-ttu-id="4dda4-132">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="4dda4-132">Display Name</span></span>
- <span data-ttu-id="4dda4-133">Tipo de producto</span><span class="sxs-lookup"><span data-stu-id="4dda4-133">Product Type</span></span>
- <span data-ttu-id="4dda4-134">Fecha de la última activación</span><span class="sxs-lookup"><span data-stu-id="4dda4-134">Last Activated Date</span></span>
- <span data-ttu-id="4dda4-135">Windows</span><span class="sxs-lookup"><span data-stu-id="4dda4-135">Windows</span></span>
- <span data-ttu-id="4dda4-136">Mac</span><span class="sxs-lookup"><span data-stu-id="4dda4-136">Mac</span></span>
- <span data-ttu-id="4dda4-137">Windows 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="4dda4-137">Windows 10 Mobile</span></span>
- <span data-ttu-id="4dda4-138">iOS</span><span class="sxs-lookup"><span data-stu-id="4dda4-138">iOS</span></span>
- <span data-ttu-id="4dda4-139">Android</span><span class="sxs-lookup"><span data-stu-id="4dda4-139">Android</span></span>

## <a name="example"></a><span data-ttu-id="4dda4-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4dda4-140">Example</span></span>

#### <a name="request"></a><span data-ttu-id="4dda4-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4dda4-141">Request</span></span>

<span data-ttu-id="4dda4-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4dda4-142">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activationsuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActivationsUserDetail
```

#### <a name="response"></a><span data-ttu-id="4dda4-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dda4-143">Response</span></span>

<span data-ttu-id="4dda4-144">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dda4-144">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="4dda4-145">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="4dda4-145">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Product Type,Last Activated Date,Windows,Mac,Windows 10 Mobile,iOS,Android
```
