Office Like Code
===

O objetivo deste repositório é [documentar](https://o-futuro-ja-comecou.github.io/office-like-code) a metodologia de organização de trabalho e gestão de conhecimento **Office Like Code**.

## Setup :open_book:

O setup windows poderá ser realizado via:

```Python
$ git clone git@github.com:o-futuro-ja-comecou/office-like-code.git
$ cd office-like-code
$ python -m venv venv
$ source venv/Scripts/activate
$ pip install -r requirements.txt
```

O setup linux poderá ser realizado via:

```Python
$ git clone git@github.com:o-futuro-ja-comecou/office-like-code.git
$ cd office-like-code
$ python3 -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```

Comando `mkdocs serve` cria servidor local para visualização, em tempo real, das modificações realizadas no documento.

## Publicações de novas versões do documento

Versionamento desta documentação foi criada utilizando a biblioteca [mike](https://github.com/jimporter/mike), conforme orientações [material mkdocs](https://squidfunk.github.io/mkdocs-material/setup/setting-up-versioning/?h=version#versioning).
[Exemplo de implementação](https://squidfunk.github.io/mkdocs-material-example-versioning/0.3/) e o [repositório de origem](https://github.com/squidfunk/mkdocs-material-example-versioning) também podem ser utilizados como referência.
Actions para publicação da documentação `1.0`[^1] foi criado para facilitar o processo de deploy da documentação que está sendo constantemente atualizada.

Para publicação de nova versão necessário atualizar manualmente o comando `deploy-mike` do arquivo `pyproject.toml`. Exemplo:

```
# Versão atual arquivo pyproject.toml
deploy-mike = { cmd = "mike deploy --push --update-aliases 1.0 latest", help = "Publica documento utilizando Mkdocs e versionamento Mike." }

# Nova Versão no arquivo pyproject.toml (cmd)
deploy-mike = { cmd = "mike deploy --push --update-aliases 2.0 latest", help = "Publica documento utilizando Mkdocs e versionamento Mike." }
```
Confira também [esta issue](https://github.com/transparencia-mg/work-stefanini/issues/17) utilizado para documentar processo de versionamento.

[^1]: Comando `mike set-default --push latest` foi executado localmente para garantir que url sempre direcione para a versão mais atual do documento.
