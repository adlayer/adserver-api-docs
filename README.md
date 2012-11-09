# Adlayer Adserver API

Este documento descreve a API do [Adlayer](http://adlayer.com.br) Adserver.

A ***Adlayer Adserver API*** permite que se consulte dados públicos das contas Adlayer.

## Privacidade
> Como dados públicos este documento se refere a informações geradas por uma conta Adlayer, mas que precisam ser acessível para todos os usuários da WEB.

Esta API não permite que se acesse dados privados e sigilosos da conta como: campanhas que estão inativas ou que ainda não iniciaram sua entrega, dados pessoais dos usuários, nada que não seja extremamente relevante aos visitantes de sites integrados, nem nada que comprometa a segurança e privacidade dos usuários Adlayer e suas organizações.

Se precisar acessar dados privados via fora da interface Adlayer, [entre em contato](mailto:contato@adlayer.org) conosco e solicite a documentação da ***Adlayer Core API*** (em breve documentação pública).

## Propósito
A Adlayer acredita na transparência esta documentação foi elaborada para que integradores e desenvolvedores relacionados com a tecnologia Adlayer entendam como funciona e quais as opções de interação com a plataforma de Adserving da Adlayer.

## Métodos
Esta API foi projetada com caráter "Read-only" (somente leitura), portanto o único método http suportado é o comando ```GET```.

## Requisições
Para utilizar esta API você deve fazer uma requisição http para a seguinte url ```http://jocasta.adlayerapp.com```
### Exemplo
```curl GET http://jocasta.adlayerapp.com/pages/:id```

Dado que está API só exibe dados públicos nenhum tipo de autenticação é necessária.

## Respostas
Todos os recursos desta API retornam o formato JSON e para suportar chamadas cross-domain de wrapper javascript o suporte a JSONP também está habilitado.
### Exemplo
JSON
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
JSONP
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

## [API](https://github.com/adlayer/adserver-api-docs/tree/master/api)
Confira a documentação de cada recurso especificamente:
* [Pages](https://github.com/adlayer/adserver-api-docs/blob/master/api/pages.md)
* [Ads](https://github.com/adlayer/adserver-api-docs/blob/master/api/ads.md)

## Clientes e Wrapper Oficiais
[Adlayer javascript api](http://github.com/adlayer/javascript-api)