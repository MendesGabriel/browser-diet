---
order: 5
title: keep-alive
---

Toda requisição HTTP precisa obrigatoriamente de uma conexão TCP estabelecida para que haja a comunicação entre o cliente e o servidor.

Estabelecer uma conexão TCP é um processo custoso e demorado (devido ao three-Way handshake), por isso é muito importante que consigamos reaproveitar conexões TCP recém criadas para trafegar outras requisições HTTP pelo mesmo "túnel".

Esta configuração é chamada de keep-alive.

A configuração é específica de servidor, então é difícil falar de todos aqui. Mas costuma ser bem simples. No Apache, por exemplo, você pode editar o arquivo `.htaccess`, veja:

```
<IfModule mod_headers.c>
  Header set Connection keep-alive
</IfModule>
```
*> [Referências](https://github.com/cleberdantas/browser-diet/wiki/References#wiki-keep-alive)*
