# <a name="reportroot-getteamsdeviceusageusercounts"></a><span data-ttu-id="b62a3-101">reportRoot: getTeamsDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="b62a3-101">reportRoot: getTeamsDeviceUsageUserCounts</span></span>

<span data-ttu-id="b62a3-102">Obtenga el número de usuarios únicos diario de Microsoft Teams por tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b62a3-102">Get the number of Microsoft Teams daily unique users by device type.</span></span>

## <a name="permissions"></a><span data-ttu-id="b62a3-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b62a3-103">Permissions</span></span>

<span data-ttu-id="b62a3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b62a3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="b62a3-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b62a3-106">Permission type</span></span>                        | <span data-ttu-id="b62a3-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b62a3-107">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="b62a3-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b62a3-108">Delegated (work or school account)</span></span>     | <span data-ttu-id="b62a3-109">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b62a3-109">Reports.Read.All</span></span>                         |
| <span data-ttu-id="b62a3-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b62a3-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b62a3-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b62a3-111">Not supported.</span></span>                           |
| <span data-ttu-id="b62a3-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b62a3-112">Application</span></span>                            | <span data-ttu-id="b62a3-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b62a3-113">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="b62a3-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b62a3-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsDeviceUsageUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="b62a3-115">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b62a3-115">Request parameters</span></span>

<span data-ttu-id="b62a3-116">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="b62a3-116">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="b62a3-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b62a3-117">Parameter</span></span> | <span data-ttu-id="b62a3-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="b62a3-118">Type</span></span>   | <span data-ttu-id="b62a3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b62a3-119">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="b62a3-120">period</span><span class="sxs-lookup"><span data-stu-id="b62a3-120">period</span></span>    | <span data-ttu-id="b62a3-121">cadena</span><span class="sxs-lookup"><span data-stu-id="b62a3-121">string</span></span> | <span data-ttu-id="b62a3-122">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b62a3-122">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="b62a3-123">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="b62a3-123">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="b62a3-124">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b62a3-124">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="b62a3-125">Necesario.</span><span class="sxs-lookup"><span data-stu-id="b62a3-125">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="b62a3-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b62a3-126">Request headers</span></span>

| <span data-ttu-id="b62a3-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="b62a3-127">Name</span></span>          | <span data-ttu-id="b62a3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b62a3-128">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="b62a3-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="b62a3-129">Authorization</span></span> | <span data-ttu-id="b62a3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b62a3-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="b62a3-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b62a3-132">Response</span></span>

<span data-ttu-id="b62a3-133">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="b62a3-133">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="b62a3-134">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b62a3-134">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="b62a3-135">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="b62a3-135">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="b62a3-136">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="b62a3-136">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="b62a3-137">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="b62a3-137">Report Refresh Date</span></span>
- <span data-ttu-id="b62a3-138">Web</span><span class="sxs-lookup"><span data-stu-id="b62a3-138">Web</span></span>
- <span data-ttu-id="b62a3-139">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="b62a3-139">Windows Phone</span></span>
- <span data-ttu-id="b62a3-140">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="b62a3-140">Android Phone</span></span>
- <span data-ttu-id="b62a3-141">iOS</span><span class="sxs-lookup"><span data-stu-id="b62a3-141">iOS</span></span>
- <span data-ttu-id="b62a3-142">Mac</span><span class="sxs-lookup"><span data-stu-id="b62a3-142">Mac</span></span>
- <span data-ttu-id="b62a3-143">Windows</span><span class="sxs-lookup"><span data-stu-id="b62a3-143">Windows</span></span>
- <span data-ttu-id="b62a3-144">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="b62a3-144">Report Date</span></span>
- <span data-ttu-id="b62a3-145">Período del informe</span><span class="sxs-lookup"><span data-stu-id="b62a3-145">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="b62a3-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b62a3-146">Example</span></span>

#### <a name="request"></a><span data-ttu-id="b62a3-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b62a3-147">Request</span></span>

<span data-ttu-id="b62a3-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b62a3-148">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusageusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsDeviceUsageUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="b62a3-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b62a3-149">Response</span></span>

<span data-ttu-id="b62a3-150">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b62a3-150">The following is an example of the response.</span></span>

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

<span data-ttu-id="b62a3-151">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="b62a3-151">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iOS,Mac,Windows,Report Date,Report Period
```
