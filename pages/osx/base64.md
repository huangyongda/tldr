# base64

> Encode and decode using Base64 representation.

- Encode a file:

`base64 -i {{plain_file}}`

- Decode a file:

`base64 -D -i {{base64_file}}`

- Encode from stdin:

`echo {{plain_text}} | base64`

- Decode from stdin:

`echo {{base64_text}} | base64 -D`
