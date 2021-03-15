Este é um projeto de site realizado por nyousefali em uma série de vídeos. Sendo meu primeiro contato com SCSS.


## Ambiente:
Estou utilizando o editor de textos VSCode neste projeto, assim se torna necessário baixar algumas extensões para facilitar o desenvolvimento

**Live Sass Compiler** e **Scss**: Indispensáveis para a utilização do Scss, para inilia-lás basta clicar em "Watch Scss" na parte inferior da tela

**SVGInject**: Permite a edição do SVG no css sem precisar estar *inline* no HTML.  Sua documentação e download se encontram no link: https://github.com/iconfu/svg-inject


## Algumas coisas sobre o SCSS:
**Variáveis**: O SCSS possui um sistema de variaveis, elas são definidas com o símbolo do **$** e podem ser utilizadas ao longo do projeto. Pode ser observada no arquivo _colors.css em partials

**Importações**: O SCSS possui métodos para importar partes de arquivos utilizando apenas uma requisição, para isso basta colocar o nome do arquivo no seguinte formato **_nomeArquivo.scss**. Após isso é necessário realizar a importação no SCSS principal com **@import 'pastaCasoExistir/nomeArquivo';**. Lembresse, as importações são feitas em ordem, então caso você defina variáveis é necessário importá-las antes de fazer sua utilização.

**Funções**: Há maneiras de criar funções com o SCSS, para isso basta declarar da seguinte forma:
            **@mixin responsive() {**
                **@media screen and (max-width: 960px){**
                    **@content;**
                **}**
            **}**
Aqui é declarada uma função chamada responsive que não recebe nenhum parametro, o atributo que estou modificando é o Media Query, e o @content será o que irei modificar
Para utiliza-la basta realizar o seguinte:
**@include responsive(){**
    **}**
