# Defina facilmente novos temas no bash.
Os temas usados foram obtidos no site: **[terminal.sexy](https://terminal.sexy)**

## Instalação

Após clonar o repositório, forneça permissão de execução:
```sh
$ chmod +x bashtheme
```

Crie um diretório para a ferramenta na raiz de seu usuário:
```sh
$ mkdir ~/.tools
```

Mova o script para lá:

```sh
$ mv bashtheme ~/.tools
```

Defina na variável PATH o caminho da ferramenta:
```sh
export PATH=$PATH:$HOME/.tools
```

### Criando o diretório de temas

Crie um diretório para os temas, na raiz de seu usuário ( existe um modelo nesse repositório ):
```sh
$ mkdir ~/.bash_themes
```

Baixe os temas disponíveis no site: *terminal.sexy*, e mova eles para o diretório criado anteriormente.

## Configurações de tema padrão

Possivelmente configurações de fonte, terminal, etc, queiram ser mantidas entre os diferentes temas.
Para isso, mantenha um arquivo com essas definições num arquivo chamado **default.theme** no diretório **.bash_themes**.

### Definindo temas

Pronto agora é só invocar a ferramenta, as opções de temas disponíveis serão retornadas de acordo aos temas que estão no seu diretório .bash_themes.

```sh
(._.): por favor, especifique somente um dos índices disponíveis abaixo: 
Temas disponíveis 
0 => ashes.dark.theme
1 => atelierlakeside.dark.theme
2 => atelierlakeside.light.theme
3 => brewer.dark.theme
4 => chalk.dark.theme
5 => codeschool.dark.theme
6 => default.dark.theme
7 => default.theme
8 => eighties.dark.theme
9 => google.dark.theme
10 => google.light.theme
11 => google_light.theme
12 => hybrid.theme
```

Para definir um tema, é só chamar o script e passar o índice correspondente ao tema escolhido:
```sh
$ ./bashtheme 1
Definindo o tema => atelierlakeside.dark.theme
```

## Persistindo as mudanças de tema

Para isso, edite o arquivo **~/.xinitrc** de forma que ele carregue o arquivo **~/.bash_themes/current.theme** ao iniciar o
servidor X, dessa forma:

***~/.xinitrc***
```sh
# variável que indica o localização do tema atual.
userX_resources="$HOME/.bash_themes/current.theme"

# checa pela presença do arquivo e carrega ele.
[[ -f "$userX_resources" ]] && xrdb -merge "$userX_resources";

```

Agora é só baixar e testar diferentes temas, bom proveito.
