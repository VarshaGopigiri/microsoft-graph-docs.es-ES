<span data-ttu-id="3d7e5-p103">Los recursos driveItem devueltos de la acción **sharedWithMe** incluirán siempre la faceta [**remoteItem**](../resources/remoteitem.md) que indica que son elementos de otra unidad. Para acceder al recurso driveItem compartido, deberá realizar una solicitud con la información proporcionada en **remoteItem** en el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="3d7e5-p103">DriveItems returned from the **sharedWithMe** action will always include the [**remoteItem**](../resources/remoteitem.md) facet which indicates they are items from a different drive. To access the shared DriveItem resource, you will need to make a request using the information provided in **remoteItem** in the following format:</span></span>

Los recursos driveItem devueltos de la acción **sharedWithMe** incluirán siempre la faceta [**remoteItem**](../resources/remoteitem.md) que indica que son elementos de otra unidad. Para acceder al recurso driveItem compartido, deberá realizar una solicitud con la información proporcionada en **remoteItem** en el siguiente formato:

<!-- {"blockType": "ignored"} -->
```http
GET https://graph.microsoft.com/v1.0/drives/{remoteItem.parentReference.driveId}/items/{remoteItem.id}
```

<!-- {
  "type": "#page.annotation",
  "description": "Retrieve a list of files shared with the signed-in user.",
  "keywords": "sharedWithMe onedrive shared files",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Shared with me"
} -->
