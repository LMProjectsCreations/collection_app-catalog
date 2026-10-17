# collection_app-catalog

Arquivos que o app **Colly** baixa sem login: os índices offline da busca do catálogo.

Tudo fica na release [`catalog-index`](https://github.com/LMProjectsCreations/collection_app-catalog/releases/tag/catalog-index):

- `manifest-v<formato>.json`: lista os arquivos de cada categoria, com tamanho e sha256. O app lê o manifesto do formato que ele entende.
- `<categoria>-v<formato>-<hash>.zip`: o índice de cada categoria (livros, quadrinhos, mangás, jogos, jogos de tabuleiro, discos, filmes e séries, cartas).
- `gcd-sqlite.zip` e `bgg-ranks.zip`: fontes que o workflow não consegue baixar sozinho, enviadas à mão. Não são usadas pelo app.

Os arquivos são gerados todo mês pelo workflow `catalog-index.yml` do repositório do app (privado). Não edite a release à mão, exceto para trocar as fontes manuais.

Dados: Open Library, Wikidata (CC0), Grand Comics Database (CC BY-SA 4.0), BoardGameGeek, MusicBrainz (CC0), Scryfall, TCGdex, YGOPRODeck. Cada arquivo traz as fontes e licenças na tabela `catalog_meta`.

Política de privacidade do Colly: https://lmprojectscreations.github.io/colly/privacy/
