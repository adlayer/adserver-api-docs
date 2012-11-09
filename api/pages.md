# Pages
```/pages/:id```
O endpoint ```/pages``` suporta os seguintes parametros:

|Parametro    |Valor |Valor padrão|Requerido|
|-------------|------|------------|---------|
|ads_per_space|Number|1           |Não      |
|domain       |String|null        |Sim      |
|site         |String|null        |Não      |

Os 'domínios habilitados' são definidos na configuração de cada site de uma conta Adlayer.

## Pagina não existente
```http
GET /pages/1 HTTP/1.1
Host: jocasta.adlayerapp.com
```

```json
{"ok":false,"error":"Page not found"}
```

## Sem um domínio habilitado
```http
GET /pages/82e719877b60e205471a9d8ef00564ab HTTP/1.1
Host: jocasta.adlayerapp.com
```

```json
{"ok":false,"error":"Domain not enabled"}
```

## Com domínio habilitado

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