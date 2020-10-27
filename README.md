# Uma ferramenta que facilita a mudança de temas do bash.

Os temas usados foram obtidos no site: ***terminal.sexy.***

## Instalação

Antes de tudo, clone o repositório .__.":
```sh
$ git clone https://github.com/stackiller/bashtheme.git
```

Entre no diretório do repositório:
```sh
$ cd bashtheme
```

Forneça permissão de execução:
```sh
$ chmod +x bashtheme
```

Crie um diretório para a ferramenta, na raiz de seu usuário:
```sh
$ mkdir ~/.tools
```

Mova o script para lá:

```sh
$ mv bashtheme ~/.tools
```

Defina no arquivo .bashrc, o caminho do script, na variável PATH;
```sh
export PATH=$PATH:$HOME/.tools
```

### Criando o diretório de temas

Crie um diretório para os temas, na raiz de seu usuário ( existe um modelo nesse repositório ):
```sh
$ mkdir ~/.bash_themes
```

Baixe os temas disponíveis no site: *terminal.sexy*, e mova eles para o diretório criado anteriormente.

## Configurações padrão

Configurações de fonte, do terminal, etc, possivelmente queiram ser mantidas entre os diferentes temas.
Para isso, mantenha um arquivo especificando essas definições dentro do diretório '.***bash_themes***, nomeado:

> '***default.theme***'

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
$ ./set_bashTheme 1
Definindo o tema => atelierlakeside.dark.theme
```

## Fixando as mudanças de tema

Mesmo tendo definido o tema, as mudanças não são permantes, isso porque o  servidor X, sempre que reiniciado, o mesmo busca por um arquivo de configurações ( recursos ) a  serem usadas naquela sessão.

Para tornar as mudanças fixas, um arquivo chamado current.theme é criado no diretório de temas, sempre que um novo tema é definido, o mesmo contém as configurações do
tema atual.

Para isso só precisamos dizer ao servidor X, que sempre que ele iniciar,  o mesmo deve carregar esse arquivo.

Para isso abrimos o arquivo '.xinitrc', e acresentamos essas linhas.

***~/.xinitrc***
```sh
# variável que indica o localização do tema atual.
userX_resources="$HOME/.bash_themes/current.theme"

# checa pela presença do arquivo e carrega ele.
[[ -f "$userX_resources" ]] && xrdb -merge "$userX_resources";

```

Fique tranquilo, agora é só baixar e testar diferentes temas, que sempre que o sistema for reiniciado, tudo estará ok.

Bom proveito :)
