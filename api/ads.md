# Pages
>/ads/:id

O endpoint ```/ads``` permite acessar as propriedades de uma peça dado um id único valido.

## Peça não existente ou não encontrada
```http
GET /ads/1 HTTP/1.1
Host: jocasta.adlayerapp.com
```

```json
{"ok":false,"error":"Ad not found"}
```

## Peça existente

```http
GET /ads/5091c7a4496c4f318d490117ee58a4a5 HTTP/1.1
Host: jocasta.adlayerapp.com
```

```json
{
	"_id": "5091c7a4496c4f318d490117ee58a4a5",
	"name": "Shot",
	"file": "http://dev.ads.adlayerapp.com/13/5091c7a4496c4f318d490117ee58a4a5.jpg",
	"campaign_id": "5091c79265b04fddaad6007cee58a4a5",
	"link": "",
	"type": "image",
	"width": "300",
	"height": "250",
	"status": true
}
```