<span data-ttu-id="374a7-p107">El usuario decide que ya no desea tener un perfil móvil y lo elimina. Esto puede realizarse con una solicitud ```DELETE``` en el valor de extensión abierta.</span><span class="sxs-lookup"><span data-stu-id="374a7-p107">The user decides that they don't want a roaming profile anymore, so they delete it. This can be done with a ```DELETE``` request on the open extension value.</span></span>
El usuario decide que ya no desea tener un perfil móvil y lo elimina. Esto puede realizarse con una solicitud ```DELETE``` en el valor de extensión abierta.

##### <a name="request"></a><span data-ttu-id="374a7-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="374a7-135">Request</span></span>
```http
DELETE https://graph.microsoft.com/v1.0/me/extensions/com.contoso.roamingSettings
```

##### <a name="response"></a><span data-ttu-id="374a7-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="374a7-136">Response</span></span>
```
HTTP/1.1 204 No content
```

## <a name="see-also"></a><span data-ttu-id="374a7-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="374a7-137">See also</span></span>

- [<span data-ttu-id="374a7-138">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="374a7-138">Add custom data to resources using extensions</span></span>](extensibility_overview.md)
- [<span data-ttu-id="374a7-139">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="374a7-139">Add custom data to groups using schema extensions</span></span>](extensibility_schema_groups.md)
- [<span data-ttu-id="374a7-140">Tipo de recurso openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="374a7-140">openTypeExtension resource type</span></span>](../api-reference/v1.0/resources/opentypeextension.md)
- [<span data-ttu-id="374a7-141">Crear extensión abierta</span><span class="sxs-lookup"><span data-stu-id="374a7-141">Create open extension</span></span>](../api-reference/v1.0/api/opentypeextension_post_opentypeextension.md)
- [<span data-ttu-id="374a7-142">Obtener extensión abierta</span><span class="sxs-lookup"><span data-stu-id="374a7-142">Get open extension</span></span>](../api-reference/v1.0/api/opentypeextension_get.md)
- [<span data-ttu-id="374a7-143">Actualizar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="374a7-143">Update open extension</span></span>](../api-reference/v1.0/api/opentypeextension_update.md)
- [<span data-ttu-id="374a7-144">Eliminar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="374a7-144">Delete open extension</span></span>](../api-reference/v1.0/api/opentypeextension_delete.md)