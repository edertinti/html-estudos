


> Escrito com [ StackEdit ](https://stackedit.io/) .

# HTML

Sites que auxiliam nesse arquivo. <br>
Links úteis: <br> **[Mozilla Developer](https://developer.mozilla.org/pt-BR/docs/Web/HTML)** <br> **[W3 Scools](https://www.w3schools.com/html/)** <br>
Linguagem de marcação de HiperTexto = **HTML**. <br> Bloco de construção mais básico da web, utilizado para definir o significado e a estrutura do conteúdo web. <br>
"Hipertexto" são os *links* que conectam páginas da web, dentro de um único site, ou entre eles.<br>
"Elemento" é uma parte da página web. Um elemento típico inclui uma tag de abertura com alguns atributos, o conteúdo de texto incluído e uma tag de fechamento.<br> As tags começam ou terminam um elemento no código fonte.<br>
"DOM" traduzido para Modelo de Objeto de Documento, é uma API, definida pelo W3C, para representar e interagir com qualquer documento HTML ou XML.<br>
## Estrutura do documento HTML
Como exemplo de um código HTML temos: <br>

~~~
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Minha página de teste</title>
  </head>
  <body>
    <img src="imagens/firefox-icon.png" alt="minha página de teste">
  </body>
</html>
~~~
<br>
Neste exemplo temos as tags: <br>

- `<!DOCTYPE html>` = Parte inicial obrigatória do documento. <br>
- `<html> </html> ` = Conhecido como elemento raiz, envolve todo o conteúdo da página.
- `<head> </head>` = Esse elemento age como um recipiente de tudo o que se deseja incluir em uma página HTML que não seja conteúdo. Inclui *palavras-chave*, *CSS* para dar estilo ao conteúdo, etc.
- `<meta charset="utf-8">` = Elemento que define o conjunto de caracteres que seu documento deve usar para o UTF-8, que inclui praticamente todos os caracteres da grande maioria dos idiomas escritos.
- `<title> </title>` = Define o título da página, que aparecerá na guia do navegador. Ele também é usado para descrever a página quando você a adiciona aos favoritos.
- `<body></body>` = Contém todo conteúdo que se deseja mostrar ao público visitante da página, seja texto, imagens, vídeos, jogos, etc.
<br>

### Aninhamento
É possível colocar elementos dentro de outro elemento, isto é denominado **aninhamento**.<br>
Como exemplo, podemos utilizar a tag `<strong>` para enfatizar uma parte do texto dentro de uma tag `<p>`.<br>
No entanto, é necessário ter cuidado para abrir e fechar corretamente os elementos.
<br>
### Elementos vazios
Alguns elementos não possuem conteúdo e são chamados de **elementos vazios**. Como exemplo, consideremos o elemento `<img>` em uma página HTML: <br>
`<img src="imagens/nomedaimagem.png" alt="Minha imagem de teste">` <br>
O elemento acima contém dois atributos, mas não há tag de fechamento `</img>`, e não há conteúdo interno. <br>
Isso acontece porque sua proposta é incorporar uma imagem na página HTML no lugar que apareceria o código, assim, o elemento da imagem não envolve conteúdo para ter efeito em si mesmo. <br>
### Imagens
Como mencionado acima, o elemento `<img>` incorpora uma imagem na página, na posição que aparece. Isso é feito pelo atributo *source*: `src`, que contém o caminho para o arquivo de imagem. <br>
Também há o atributo *alternative*: `alt`, onde podemos especificar um texto descritivo para usuários que não podem ver a imagem, seja por serem deficientes visuais, e utilizarem ferramentas de leitores de tela, ou por algum erro que não permitiu o carregamento da imagem. <br>
Uma boa prática é garantir que o texto alternativo forneça ao leitor informações suficientes para ter uma boa ideia do que a imagem mostra. <br>
## Marcando o texto
Alguns elementos HTML são essenciais para *marcar* o texto. Vejamos alguns deles:<br>
### Cabeçalhos
Permitem especificar que certas partes do conteúdo são títulos ou subtítulos. Assim como um livro tem o título principal, e os capítulos possuem título e subtítulos, um documento HTML também possui divisões.<br>
Há seis níveis de título, embora normalmente são utilizados três a quatro.
~~~
<h1>Meu título principal</h1>
<h2>Meu título de alto nível</h2>
<h3>Meu subtítulo</h3>
<h4>Meu segundo subtítulo</h4>
~~~
Uma boa prática é não utilizar elemento de cabeçalho para aumentar ou negritar o texto, pois eles são usados para acessibilidade e outros motivos, como SEO. É importante criar uma sequência significativa de títulos em suas páginas, sem pular os níveis. <br>
### Parágrafo
Os elementos `<p>` são utilizados para conter um parágrafo de texto. São usados com frequência ao marcar um conteúdo de texto regular: <br>
`<p>Este é um parágrafo simples</p>` <br>
### Listas
No HTML é possível utilizar o elemento especial *listas*. Listas de marcação sempre consistem em pelo menos dois elementos. Os tipos mais comuns de lista são ordenadas e não ordenadas: <br>
- **Listas não ordenadas:** são para listas onde a ordem dos itens não importa, como por exemplo em uma lista de compras. São envolvidas no elemento `<ul>`.<br>
- **Listas ordenadas**: são para listas onde a ordem dos itens importa, como uma receita. São envolvidas pelo elemento `<ol>`.<br>
<br>Cada item dentro da lista é posto dentro de um elemento `<li>`, que significa item de lista. <br>
Como por exemplo, podemos tornar a parte de um parágrafo em uma lista:
~~~
<p>Preciso comprar: arroz, feijão, alface, ovo.</p>
~~~
Podendo escrevê-lo assim:
~~~
<p>Preciso comprar:</p>

<ul>
  <li>arroz</li>
  <li>feijão</li>
  <li>alface</li>
  <li>ovo</li>
</ul>
~~~
### Links
Os links são muito importantes, pois fazem a web ser uma rede. Para adicionar um link usamos o elemento `<a>`, que é a forma abreviada de *âncora*.<br>
Para transformar o texto de um paragráfo em em link, basta seguirmos as seguintes etapas:<br>
1.  Escolha algum texto. Por exemplo: "Clique aqui para ir para a página";
2.  Envolva o texto com o elemento `<a>`;<br>
`<a>Clique aqui para ir para a página</a>`
3.   Inclua no elemento `<a>` o atributo `href`:<br>
`<a href="">Clique aqui para ir para a página</a>` 
4.  Preencha o valor do atributo `href` com o endereço web que deseja vincular ao link:<br>
`<a href="https://www.sitequeseradirecionado.com">Clique aqui para ir para a página</a>` <br>
<br>Atenção ao omitir o *protocolo* `http://` ou o *protocolo* `https://` no começo do endereço web, para que não se obtenha um resultado inesperado. Por isso, após a criação de um link, clique nele para ter certeza que esta sendo redirecionado corretamente.   
