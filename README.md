# Adlayer Adserver API

Este documento descreve a API do Ad server da [Adlayer](http://adlayer.com.br).

A Adserver API permite que consulte *dados públicos das contas Adlayer

> *Como dados públicos este documento se refere a informações geradas por uma conta Adlayer, mas que precisa ser acessível para todos os usuários da WEB.

Esta API não permite que se acesse dados provados e sigilosos da conta como: campanhas que estão inativas ou que ainda não iniciaram sua entrega, dados pessoais dos usuários de conta Adlayer, nada que não seja extremamente relevante aos visitantes de sites integrados, nem nenhum nada que comprometa a segurança e privacidade dos usuários Adlayer e suas organizações.

Se precise acessar dados provados via API, entre em contato com a equipe Adlayer e solicite a documentação da Adlayer Core API (em breve documentação pública).

# Proposito
A Adlayer acredita na transparência esta documentação foi elaborada para que integradores e desenvolvedores relacionados com a tecnologia Adlayer entendam como funciona e quais as opções de interação com a plataforma de Adserving da Adlayer.

# Métodos
Esta API foi projetada com caráter "Read-only" (somente leitura), portanto o único método http suportado é o comando ```GET```.


## Clientes e Wrapper oficiais
[Adlayer javascript api](http://github.com/adlayer/javascript-api)