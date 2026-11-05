# Site-IgrejaNSDP

Site simples para a igreja católica de Timbuí: a **Comunidade Nossa Senhora da Penha (CEB)**, da Paróquia São José de Fundão.

O site mostra os horários de missa, os avisos da comunidade (missas, eventos, recados) e como chegar até a igreja. Ele é publicado de graça pelo GitHub Pages.

## Como publicar um aviso

Cada aviso é um arquivo de texto na pasta [`_avisos`](_avisos). Para criar um novo pelo próprio site do GitHub:

1. Abra a pasta `_avisos` e clique em **Add file → Create new file**.
2. Dê ao arquivo um nome com a data e um título curto, sem acentos nem espaços:
   `2026-12-24-missa-de-natal.md`
3. Cole o modelo abaixo e troque o texto:

   ```markdown
   ---
   title: Missa de Natal
   categoria: Missa
   quando: "24 de dezembro, às 22h"
   local: "Igreja de Timbuí"
   ---

   Escreva aqui o aviso, com quantos parágrafos quiser.
   ```

4. Clique em **Commit changes**. Em um ou dois minutos o aviso aparece na página inicial do site, com o texto completo. Os mais recentes aparecem primeiro.

- `categoria` pode ser, por exemplo, `Aviso`, `Missa` ou `Evento`. Se ficar vazia, aparece "Aviso".
- `quando` e `local` são opcionais. Se não fizerem sentido para o aviso, apague essas duas linhas.
- Para corrigir ou apagar um aviso, abra o arquivo dele em `_avisos` e use o lápis (editar) ou a lixeira.

## Como mudar horários de missa, telefone e endereço

Tudo isso fica em um único arquivo: [`_data/igreja.yml`](_data/igreja.yml). Abra, clique no lápis, edite e salve. As instruções estão dentro do próprio arquivo.

Enquanto os horários de missa não forem preenchidos, a página inicial mostra um recado com o link para o Instagram da paróquia. Telefone, WhatsApp e e-mail só aparecem quando forem preenchidos.

## Ligar o GitHub Pages (uma vez só)

1. No repositório, vá em **Settings → Pages**.
2. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`, e salve.
3. O site fica em `https://arthpomz.github.io/Site-IgrejaNSDP/`.

## Usar um domínio próprio depois

Quando registrar um domínio (por exemplo `igrejatimbui.com.br` no Registro.br):

1. Em `_config.yml`, troque `url` pelo domínio (com `https://`) e deixe `baseurl: ""`.
2. Em **Settings → Pages → Custom domain**, digite o domínio e salve. O GitHub cria o arquivo `CNAME`.
3. No Registro.br, aponte o domínio para o GitHub Pages seguindo a [documentação do GitHub](https://docs.github.com/pt/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Ver o site no computador (opcional, para quem programa)

```sh
bundle install
bundle exec jekyll serve
```

E abra `http://localhost:4000/Site-IgrejaNSDP/`.

## Estrutura

| Caminho | O que é |
| --- | --- |
| `index.html` | Página inicial: capa, avisos (com o texto completo), missas e contato |
| `_avisos/` | Os avisos, um arquivo por aviso |
| `_data/igreja.yml` | Endereço, contatos e horários de missa |
| `_layouts/`, `_includes/` | Moldes das páginas e o desenho da fachada |
| `assets/` | Estilos, fontes e imagens |

As fontes são Marcellus e Atkinson Hyperlegible, ambas com licença livre (SIL Open Font License).
