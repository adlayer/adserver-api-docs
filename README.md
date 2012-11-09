# Adlayer Adserver API

Este documento descreve a API do Ad server da [Adlayer](http://adlayer.com.br).

A Adserver API permite que consulte *dados públicos das contas Adlayer

> *Como dados públicos este documento se refere a informações geradas por uma conta Adlayer, mas que precisa ser acessível para todos os usuários da WEB.

Esta API não permite que se acesse dados provados e sigilosos da conta como: campanhas que estão inativas ou que ainda não iniciaram sua entrega, dados pessoais dos usuários de conta Adlayer, nada que não seja extremamente relevante aos visitantes de sites integrados, nem nenhum nada que comprometa a segurança e privacidade dos usuários Adlayer e suas organizações.

Se precise acessar dados provados via API, entre em contato com a equipe Adlayer e solicite a documentação da Adlayer Core API (em breve documentação pública).

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
{}
```
JSONP
```javascript
	callback({})
```

## API

## Clientes e Wrapper oficiais
[Adlayer javascript api](http://github.com/adlayer/javascript-api)