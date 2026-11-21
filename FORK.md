# Fork do Habblaud

Fork público de [marmottajr/habblaud](https://github.com/marmottajr/habblaud). Existe porque correções úteis ficaram
em PRs abertos sem merge no upstream (sem atividade do mantenedor desde 16/10/2026). A `main` daqui é a do upstream
mais esses PRs.

## PRs do upstream incluídos

Aplicados por cherry-pick, com a autoria original preservada:

- [#121](https://github.com/marmottajr/habblaud/pull/121): comando de barra (`/compact`, `/model opus`) pela caixa de
  mensagem, via `$.command.run`; comando que abre painel é recusado.
- [#122](https://github.com/marmottajr/habblaud/pull/122): menu de comandos de barra na caixa (contém os commits do #121).
- [#156](https://github.com/marmottajr/habblaud/pull/156): colar print (Ctrl+V) na caixa grava a imagem e põe o caminho.

## Regra

Integração nossa mora numa pasta separada, nunca espalhada pelo core. Mudança no core só quando for um PR que também
faria sentido no upstream.

## Sincronizar com o upstream

```sh
git fetch upstream && git merge upstream/main
```

Se um PR incluído aqui for mergeado lá, o merge resolve sozinho ou dá conflito trivial (fica a versão do upstream).
