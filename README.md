# Adlayer Adserver API

A Adlayer Adserver API permite que se consulte dados públicos das contas Adlayer.

Este documento descreve a API do ***[Adlayer](http://adlayer.com.br) Adserver*** e foi elaborada para que integradores e desenvolvedores relacionados com a tecnologia Adlayer, entendam como funciona e quais as opções de interação com a plataforma de [Adserving](http://adlayer.com.br/ad-server) da Adlayer.

## [API](https://github.com/adlayer/adserver-api-docs/tree/master/api) - Documentação completa
Confira a documentação de cada recurso especificamente:
* [Pages](https://github.com/adlayer/adserver-api-docs/blob/master/api/pages.md)
* [Ads](https://github.com/adlayer/adserver-api-docs/blob/master/api/ads.md)
* [Spaces](https://github.com/adlayer/adserver-api-docs/blob/master/api/spaces.md)

## Métodos
Esta API foi projetada com caráter "Read-only" (somente leitura), portanto o único método http suportado é o comando ```GET```.



## Requisições e Respostas

Para utilizar esta API você deve fazer as requisições http para a seguinte url: **http://jocasta.adlayerapp.com**

### Exemplo de requisição
```http
GET http://jocasta.adlayerapp.com/pages/:id HTTP/1.1
```
----------------
Todos os recursos desta API retornam o formato ```JSON``` por padrão e para suportar chamadas cross-domain de wrappers javascript, o suporte a ```JSONP``` também está habilitado.

### JSON
```http
GET /ads/5091c7a4496c4f318d490117ee58a4a5 HTTP/1.1
Host: jocasta.adlayerapp.com
Accept: application/json
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

### JSONP
```http
GET /ads/5091c7a4496c4f318d490117ee58a4a5?callback=callback HTTP/1.1
Host: jocasta.adlayerapp.com
Accept: text/javascript
```

```javascript
callback({
	"_id": "5091c7a4496c4f318d490117ee58a4a5",
	"name": "Shot",
	"file": "http://dev.ads.adlayerapp.com/13/5091c7a4496c4f318d490117ee58a4a5.jpg",
	"campaign_id": "5091c79265b04fddaad6007cee58a4a5",
	"link": "",
	"type": "image",
	"width": "300",
	"height": "250",
	"status": true
})
```

### [Veja a documentação completa](https://github.com/adlayer/adserver-api-docs/tree/master/api)

## Privacidade
> Como "dados públicos" este documento se refere a informações geradas por uma conta Adlayer, mas que precisam ser acessível para todos os usuários da web.

Esta Api não acesso a dados privados e sigilosos da conta como: campanhas que estão inativas ou que ainda não iniciaram sua entrega, dados pessoais dos usuários.

Os dados entregues também não podem ser deletados por esta API.

Se precisar acessar dados privados via http fora da interface Adlayer, [entre em contato](mailto:contato@adlayer.org) conosco e solicite a documentação da ***Adlayer Core API*** (em breve documentação pública).

## Clientes e Wrapper Oficiais
[Adlayer javascript api](http://github.com/adlayer/javascript-api)