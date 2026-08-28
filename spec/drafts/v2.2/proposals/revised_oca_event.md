This pulls in the x-oca-event and x-oca-asset objects into the specification with several minor changes.

1. x-oca-event is renamed log-event and transitioned to an SCO
2. x-oca-event no longer has the `x_ttp_tagging_refs` property as this is better tracked through the unified event SDO
3. x-oca-asset is renamed asset
4. x-oca-asset no longer uses `x-oca-geo` and instead references location SDOs
5. container_type_ov is removed in favor of keeping container_type as a `string`. Ideally we should find an external reference we can point users to for names here, but it can be turned back into an open vocabulary if required.