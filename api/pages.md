# Pages

|Parametro    |Valor |Valor padrão|
|-------------|------|------------|
|ads_per_space|Number|1           |
|domain       |String|null        |
|site         |String|null        |

```http
GET /pages/82e719877b60e205471a9d8ef00564ab HTTP/1.1
Host: jocasta.adlayerapp.com
```

```json
{"ok":false,"error":"Domain not enabled"}
```

---

```http
GET /pages/82e719877b60e205471a9d8ef00564ab?domain=localhost HTTP/1.1
Host: jocasta.adlayerapp.com
```

```json
{
	"id": "",
	"name": "home",
	"spaces": [{
		"_id": "509051bed98c463abd4b213cee58a4a5",
		"name": "expandable",
		"type": "expandable",
		"size": {
			"width": "200px",
			"height": "200px"
		},
		"ads": []
	}],
	"status": true,
	"_id": "82e719877b60e205471a9d8ef00564ab",
	"from_site": "82e719877b60e205471a9d8ef0055af6"
}

```