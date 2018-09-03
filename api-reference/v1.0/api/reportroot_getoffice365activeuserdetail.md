# <a name="reportroot-getoffice365activeuserdetail"></a><span data-ttu-id="666e7-101">reportRoot: getOffice365ActiveUserDetail</span><span class="sxs-lookup"><span data-stu-id="666e7-101">reportRoot: getOffice365ActiveUserDetail</span></span>

<span data-ttu-id="666e7-102">Obtiene información sobre los usuarios activos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="666e7-102">Get details about Office 365 active users.</span></span>

> <span data-ttu-id="666e7-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="666e7-103">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="666e7-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="666e7-104">Permissions</span></span>

<span data-ttu-id="666e7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="666e7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="666e7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="666e7-107">Permission type</span></span>                        | <span data-ttu-id="666e7-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="666e7-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="666e7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="666e7-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="666e7-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="666e7-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="666e7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="666e7-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="666e7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="666e7-112">Not supported.</span></span>                           |
| <span data-ttu-id="666e7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="666e7-113">Application</span></span>                            | <span data-ttu-id="666e7-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="666e7-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="666e7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="666e7-115">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getOffice365ActiveUserDetail(period='{period_value}')
GET /reports/getOffice365ActiveUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="666e7-116">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="666e7-116">Function parameters</span></span>

<span data-ttu-id="666e7-117">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="666e7-117">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="666e7-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="666e7-118">Parameter</span></span> | <span data-ttu-id="666e7-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="666e7-119">Type</span></span>   | <span data-ttu-id="666e7-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="666e7-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="666e7-121">period</span><span class="sxs-lookup"><span data-stu-id="666e7-121">period</span></span>    | <span data-ttu-id="666e7-122">cadena</span><span class="sxs-lookup"><span data-stu-id="666e7-122">string</span></span> | <span data-ttu-id="666e7-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="666e7-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="666e7-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="666e7-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="666e7-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="666e7-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="666e7-126">date</span><span class="sxs-lookup"><span data-stu-id="666e7-126">date</span></span>      | <span data-ttu-id="666e7-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="666e7-127">Date</span></span>   | <span data-ttu-id="666e7-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="666e7-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="666e7-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="666e7-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="666e7-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="666e7-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="666e7-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="666e7-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="666e7-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="666e7-132">Request headers</span></span>

| <span data-ttu-id="666e7-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="666e7-133">Name</span></span>          | <span data-ttu-id="666e7-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="666e7-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="666e7-135">Autorización</span><span class="sxs-lookup"><span data-stu-id="666e7-135">Authorization</span></span> | <span data-ttu-id="666e7-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="666e7-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="666e7-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="666e7-138">If-None-Match</span></span> | <span data-ttu-id="666e7-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="666e7-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="666e7-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="666e7-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="666e7-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="666e7-141">Response</span></span>

<span data-ttu-id="666e7-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="666e7-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="666e7-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="666e7-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="666e7-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="666e7-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="666e7-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="666e7-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="666e7-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="666e7-146">Report Refresh Date</span></span>
- <span data-ttu-id="666e7-147">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="666e7-147">User Principal Name</span></span>
- <span data-ttu-id="666e7-148">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="666e7-148">Display Name</span></span>
- <span data-ttu-id="666e7-149">Eliminado</span><span class="sxs-lookup"><span data-stu-id="666e7-149">Is Deleted</span></span>
- <span data-ttu-id="666e7-150">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="666e7-150">Deleted Date</span></span>
- <span data-ttu-id="666e7-151">Tiene una licencia de Exchange</span><span class="sxs-lookup"><span data-stu-id="666e7-151">Has Exchange License</span></span>
- <span data-ttu-id="666e7-152">Tiene una licencia de OneDrive</span><span class="sxs-lookup"><span data-stu-id="666e7-152">Has OneDrive License</span></span>
- <span data-ttu-id="666e7-153">Tiene de licencia de SharePoint</span><span class="sxs-lookup"><span data-stu-id="666e7-153">Has SharePoint License</span></span>
- <span data-ttu-id="666e7-154">Tiene una licencia de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="666e7-154">Has Skype For Business License</span></span>
- <span data-ttu-id="666e7-155">Tiene una licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="666e7-155">Has Yammer License</span></span>
- <span data-ttu-id="666e7-156">Tiene una licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="666e7-156">Has Teams License</span></span>
- <span data-ttu-id="666e7-157">Fecha de la última actividad de Exchange</span><span class="sxs-lookup"><span data-stu-id="666e7-157">Exchange Last Activity Date</span></span>
- <span data-ttu-id="666e7-158">Fecha de la última actividad de OneDrive</span><span class="sxs-lookup"><span data-stu-id="666e7-158">OneDrive Last Activity Date</span></span>
- <span data-ttu-id="666e7-159">Fecha de la última actividad de SharePoint</span><span class="sxs-lookup"><span data-stu-id="666e7-159">SharePoint Last Activity Date</span></span>
- <span data-ttu-id="666e7-160">Fecha de la última actividad de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="666e7-160">Skype For Business Last Activity Date</span></span>
- <span data-ttu-id="666e7-161">Fecha de la última actividad de Yammer</span><span class="sxs-lookup"><span data-stu-id="666e7-161">Yammer Last Activity Date</span></span>
- <span data-ttu-id="666e7-162">Fecha de la última actividad de Teams</span><span class="sxs-lookup"><span data-stu-id="666e7-162">Teams Last Activity Date</span></span>
- <span data-ttu-id="666e7-163">Fecha de asignación de licencia de Exchange</span><span class="sxs-lookup"><span data-stu-id="666e7-163">Exchange License Assign Date</span></span>
- <span data-ttu-id="666e7-164">Fecha de asignación de licencia de licencia de OneDrive</span><span class="sxs-lookup"><span data-stu-id="666e7-164">OneDrive License Assign Date</span></span>
- <span data-ttu-id="666e7-165">Fecha de asignación de licencia de SharePoint</span><span class="sxs-lookup"><span data-stu-id="666e7-165">SharePoint License Assign Date</span></span>
- <span data-ttu-id="666e7-166">Fecha de asignación de licencia de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="666e7-166">Skype For Business License Assign Date</span></span>
- <span data-ttu-id="666e7-167">Fecha de asignación de licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="666e7-167">Yammer License Assign Date</span></span>
- <span data-ttu-id="666e7-168">Fecha de asignación de licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="666e7-168">Teams License Assign Date</span></span>
- <span data-ttu-id="666e7-169">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="666e7-169">Assigned Products</span></span>

## <a name="example"></a><span data-ttu-id="666e7-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="666e7-170">Example</span></span>

#### <a name="request"></a><span data-ttu-id="666e7-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="666e7-171">Request</span></span>

<span data-ttu-id="666e7-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="666e7-172">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activeuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActiveUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="666e7-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="666e7-173">Response</span></span>

<span data-ttu-id="666e7-174">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="666e7-174">The following is an example of the response.</span></span>

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

<span data-ttu-id="666e7-175">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="666e7-175">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Has Exchange License,Has OneDrive License,Has SharePoint License,Has Skype For Business License,Has Yammer License,Has Teams License,Exchange Last Activity Date,OneDrive Last Activity Date,SharePoint Last Activity Date,Skype For Business Last Activity Date,Yammer Last Activity Date,Teams Last Activity Date,Exchange License Assign Date,OneDrive License Assign Date,SharePoint License Assign Date,Skype For Business License Assign Date,Yammer License Assign Date,Teams License Assign Date,Assigned Products
```
