---
layout: post
title: API Beta
---

<p class="message">
 Atenção: Essas informações sāo validas apenas para o PlaylisTV Beta
</p>

### Informações sobre a lista e do Autor

O [PlaylisTV](https://play.google.com/store/apps/details?id=me.targa.iptvbr) permite a customização de playlists usando parâmetros opcionais com informações sobre o autor, foto, site e etc. Esses parâmetros devem ser usado em **uma única linha** e iniciados com `#PLAYLISTV:`, abaixo seguem a relação de parâmetros disponíveis:

  - `pltv-logo` - Logo da playlist
  - `pltv-name` - Nome da playlist
  - `pltv-description` - Descrição
  - `pltv-cover` - Imagem do topo da lista e da tela de informações da Playlist
  - `pltv-author` - Seu Nome/Nick
  - `pltv-site` - Seu site/blog/facebook
  - `pltv-email` - Seu E-mail
  - `pltv-phone` - Seu telefone/whatsapp
  - `pltv-donate` - Url para paypal ou outra plataforma de doação

Exemplo de uso:

`#PLAYLISTV: pltv-logo="https://goo.gl/UW9kcR" pltv-name="ONSeries" pltv-description="Lista de séries para PlaylisTV/IPTV" pltv-cover="http://i.ytimg.com/vi/UoMYfrdAmV8/maxresdefault.jpg" pltv-author="PMachado" pltv-site="http://bit.ly/DoarOnSerieS" pltv-email="pmachado@n5x.mobi" pltv-phone="0000000000"`

NOTA: O PlaylisTV irá usar a cor dominante da sua imagem de capa (pltv-cover) e aplicar no design, para sua playlist ficar personalizada.

Resultado:


![Infos](http://i.imgur.com/YaZqsqz.png)
![](http://i.imgur.com/BfoP0Ez.png)
### Playlist

Devem iniciar com `#EXTINF:`, logo após vem os parâmetros que serão explicados abaixo, e por fim o nome do canal/filme/serie
**iniciado com uma vírgula**.
E na linha abaixo, o link do stream.

 Parâmetros disponíveis:

  - `tvg-logo` - Logo *(uso recomendado)*
  - `group-title` - Categoria *(uso recomendado)*
  - `pltv-subgroup` - Sub Categoria
  - `pltv-adult="true"` - Canal adulto

Exemplo
```
 #EXTINF: tvg-logo="https://goo.gl/UW9kcR" group-title="Categoria",Nome Do canal
http://bit.ly/Link
```


Para usar subcategorias use a tag `pltv-subgroup`, exemplo:

```
 #EXTINF: tvg-logo="https://goo.gl/UW9kcR" group-title="Categoria" pltv-subgroup="Sub Categoria",Nome Do canal
http://bit.ly/Link
```

### Formatação de texto

É possivel usar **negrito**, _italico_, sublinhado e cores (html colors) para o texto das categorias, subcategorias e nome do canal/epsodio/filme usando as seguintes tags:


`[B]negrito[/B]`

`[I]Italico[/I]`

`[U]Sublinhado[/U]`

`[COLOR blue]Texto em azul[/COLOR]`

`[COLOR #0000FF]Texto em azul[/COLOR]`


### Referrer

Será possivel também compartilhar o PlaylisTV com sua lista já incluída após a instalação do app usando:

`https://play.google.com/store/apps/details?id=me.targa.playlistvbeta&referrer=SUA_LISTA`

exemplo:

`https://play.google.com/store/apps/details?id=me.targa.playlistvbeta&referrer=cinebox.ga`
`https://play.google.com/store/apps/details?id=me.targa.playlistvbeta&referrer=bit.ly%2FONSeries`
