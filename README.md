# Uma ferramenta que facilita a mudança de temas do bash.

Os temas usados foram obtidos no site: terminal.sexy.
Siga os passos abaixo para usar a ferramenta:

## "Instalação"
Forneça permissão de execução:
```sh
$ chmod +x bashtheme
```

Crie um diretório na $HOME ( o diretório raiz do seu usuário ) para a ferramenta:
```sh
$ mkdir ~/.tools
```

Mova o script para lá:

```sh
$ mv bashtheme ~/.tools
```

Defina no arquivo '~/.bashrc', o caminho do script, na
variável PATH;
```sh
export PATH=$PATH:$HOME/.tools
```

## Definindo os temas

Crie um diretório para os temas, na $home ( existe um modelo nesse repositório ):
```sh
$ mkdir ~/.bash_themes
```

Baixe os temas disponíveis no site terminal.sexy, e mova eles para o diretório criado anteriormente: '~/.bash_themes'.

## Usando a ferramenta

Pronto agora é só invocar a ferramenta, as opções de temas disponíveis serão retornadas de acordo aos temas que estão no seu diretório ~/.bash_themes.

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
$ ./set_bashTheme 1
Definindo o tema => atelierlakeside.dark.theme
```

Pronto, tema definido !!!

Só mais uma observação:

Tipos de fonte, tamanho, configurações do terminal etc, talvez queiram ser mantidas entre os diferentes temas.
Para isso, mantenha um arquivo de configurações padrão, dentro do diretório '~/.bash_themes', nomeado:

> *default.theme*

bom proveito :)
 
