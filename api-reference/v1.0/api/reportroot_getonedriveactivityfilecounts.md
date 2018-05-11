# <a name="reportroot-getonedriveactivityfilecounts"></a><span data-ttu-id="fbfcf-101">reportRoot: getOneDriveActivityFileCounts</span><span class="sxs-lookup"><span data-stu-id="fbfcf-101">reportRoot: getOneDriveActivityFileCounts</span></span>

<span data-ttu-id="fbfcf-102">Obtiene el número de usuarios con licencia únicos que realizaron interacciones con archivos en una cuenta de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-102">Get the number of unique, licensed users that performed file interactions against any OneDrive account.</span></span>

> <span data-ttu-id="fbfcf-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span><span class="sxs-lookup"><span data-stu-id="fbfcf-103">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business activity](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span></span>

## <a name="permissions"></a><span data-ttu-id="fbfcf-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="fbfcf-104">Permissions</span></span>

<span data-ttu-id="fbfcf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fbfcf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="fbfcf-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fbfcf-107">Permission type</span></span>                        | <span data-ttu-id="fbfcf-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fbfcf-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="fbfcf-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fbfcf-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="fbfcf-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="fbfcf-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="fbfcf-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fbfcf-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fbfcf-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-112">Not supported.</span></span>                           |
| <span data-ttu-id="fbfcf-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fbfcf-113">Application</span></span>                            | <span data-ttu-id="fbfcf-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="fbfcf-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="fbfcf-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fbfcf-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveActivityFileCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="fbfcf-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fbfcf-116">Request parameters</span></span>

<span data-ttu-id="fbfcf-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-117">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="fbfcf-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fbfcf-118">Parameter</span></span> | <span data-ttu-id="fbfcf-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbfcf-119">Type</span></span>   | <span data-ttu-id="fbfcf-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbfcf-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="fbfcf-121">period</span><span class="sxs-lookup"><span data-stu-id="fbfcf-121">period</span></span>    | <span data-ttu-id="fbfcf-122">cadena</span><span class="sxs-lookup"><span data-stu-id="fbfcf-122">string</span></span> | <span data-ttu-id="fbfcf-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="fbfcf-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="fbfcf-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-125">These values follow the format D   where    represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="fbfcf-126">Necesario.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="fbfcf-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fbfcf-127">Request headers</span></span>

| <span data-ttu-id="fbfcf-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="fbfcf-128">Name</span></span>          | <span data-ttu-id="fbfcf-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbfcf-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="fbfcf-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="fbfcf-130">Authorization</span></span> | <span data-ttu-id="fbfcf-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="fbfcf-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="fbfcf-133">If-None-Match</span></span> | <span data-ttu-id="fbfcf-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-134">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="fbfcf-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="fbfcf-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbfcf-136">Response</span></span>

<span data-ttu-id="fbfcf-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="fbfcf-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="fbfcf-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="fbfcf-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="fbfcf-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="fbfcf-141">Report Refresh Date</span></span>
- <span data-ttu-id="fbfcf-142">Visto o editado</span><span class="sxs-lookup"><span data-stu-id="fbfcf-142">Viewed Or Edited</span></span>
- <span data-ttu-id="fbfcf-143">Sincronizado</span><span class="sxs-lookup"><span data-stu-id="fbfcf-143">Synced</span></span>
- <span data-ttu-id="fbfcf-144">Compartido internamente</span><span class="sxs-lookup"><span data-stu-id="fbfcf-144">Shared Internally</span></span>
- <span data-ttu-id="fbfcf-145">Compartido externamente</span><span class="sxs-lookup"><span data-stu-id="fbfcf-145">Shared Externally</span></span>
- <span data-ttu-id="fbfcf-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="fbfcf-146">Report Date</span></span>
- <span data-ttu-id="fbfcf-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="fbfcf-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="fbfcf-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fbfcf-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="fbfcf-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fbfcf-149">Request</span></span>

<span data-ttu-id="fbfcf-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-150">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveactivityfilecounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveActivityFileCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="fbfcf-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbfcf-151">Response</span></span>

<span data-ttu-id="fbfcf-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-152">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="fbfcf-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="fbfcf-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Viewed Or Edited,Synced,Shared Internally,Shared Externally,Report Date,Report Period
```
