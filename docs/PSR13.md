## PSR-13: Link definition interfaces
## PATRUSHEV DMITRIY WB-432
Hypermedia links are becoming an increasingly important part of the web, in both HTML contexts and various API format contexts. However, there is no single common hypermedia format, nor is there a common way to represent links between formats.
## References
-RFC 2119
-RFC 4287
-RFC 5988
-RFC 6570
-(IANA Link Relations Registry)[http://www.iana.org/assignments/link-relations/link-relations.xhtml]
Some attributes (commonly `hreflang`) may appear more than once in their context. Therefore, an attribute value MAY be an array of values rather than a simple value. Serializers MAY encode that array in whatever format is appropriate for the serialized format (such as a space-separated list, comma-separated list, etc.). If a given attribute is not allowed to have multiple values in a particular context, serializers MUST use the first value provided and ignore all subsequent values.
