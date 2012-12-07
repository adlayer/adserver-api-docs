# Spaces
>/Spaces/:id

O endpoint ```/spaces``` suporta os seguintes parametros:

|Parametro    |Valor |Valor padrão|Requerido|
|-------------|------|------------|---------|
|ads_per_space|Number|1           |Não      |
|domain       |String|null        |Não      |
|site         |String|null        |Não      |

## Espaço não existente
```http
GET /spaces/1 HTTP/1.1
Host: jocasta.adlayerapp.com
```

```json
{"ok":false,"error":"Space not found"}
```

## Espaço existente

```http
GET /spaces/50b4ebebf76c4e7e91d8560ed8779272
HTTP/1.1
Host: jocasta.adlayerapp.com
```

```json
{"id": "",
  "type": "static",
  "status": "",
  "ads": [
    {
      "_id": "50b4ee58fe4c47338ace5612d8779272",
      "name": "Fullbanner",
      "file": "http://ads.adlayerapp.com/1/50b4ee58fe4c47338ace5612d8779272.jpg?version=50b8b2713918e",
      "campaign_id": "50b4ee20ebcc4fcf9800561bd8779272",
      "link": "http://slumdog.com.br",
      "type": "image",
      "width": "728",
      "height": "90",
      "status": true
    }
  ],
  "behaviour": {},
  "_id": "50b4ebebf76c4e7e91d8560ed8779272",
  "name": "Fullbanner",
  "size": {
    "width": "px",
    "height": "px"
  }
}
```