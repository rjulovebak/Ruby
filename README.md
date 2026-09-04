Biblioteca antiga que escrevi para desenhar gráficos de barras em páginas PHP.


---

Exemplo de uso, considerando um arquivo que devolve a imagem:

```
<?php
    require_once("vendor/autoload.php");
    require_once("./vendor/andreterceiro/minigraficoimagem/MiniGraficoImagem.php");
    $c = new MiniGraficoImagem ;
    $c->cadastrar(2,"Uva",20,180,60) ;
    $c->cadastrar(6,"Pera",180,60,20) ;
    $c->gerarGrafico();
?>

```
Chamando a imagem numa página qualquer. Ignorando o resto da marcação, o essencial é apontar o atributo de origem para esse script.

Um exemplo mais completo, com linha de referência e três séries da mesma cor base:

```
<?php
    require_once("vendor/autoload.php");
    require_once("./vendor/andreterceiro/minigraficoimagem/MiniGraficoImagem.php");
    $c = new MiniGraficoImagem;
    $c->setarLinhaReferencia(8);
    $c->cadastrar(2,"Debian",10,90,200);
    $c->cadastrar(4,"Fedora",30,120,240);
    $c->cadastrar(3,"Arch",60,60,180);
    $c->gerarGrafico(240,240,210);
?>
```

Os exemplos completos ficam na pasta de exemplos do projeto.

Existem versões publicadas e navegáveis numa página pessoal do autor.

Licença MIT.