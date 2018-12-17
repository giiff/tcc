# IFG-Formosa TCC TADS #

Modelo padrão de formatação de documentos acadêmicos do [IFG, Câmpus Formosa](www.ifg.edu.br). Este modelo existe para **padronizar** a formatação dos trabalhos de conclusão de curso do IFG Formosa.


## Licença ##

Esta obra foi adaptada de [CIC-UnB](https://github.com/UnB-CIC/Monografia/) e está licenciada com uma Licença [Creative Commons Atribuição-CompartilhaIgual 4.0 Internacional](http://creativecommons.org/licenses/by-sa/4.0/deed.pt_BR).

![Licença Creative Commons](img/cc.png?raw=true )


## Instalação ##

Assume-se que há uma instalação correta do [TeX Live](https://www.tug.org/texlive/). 
Para qualquer dos sistemas operacionais mais comuns (Unix/Mac OS/Windows), basta copiar todos os arquivos disponíveis. 


## Uso ##

Para a geração do documento final em PDF, basta executar as linhas de comando:

```bash
cd /caminho/para/arquivos/
pdflatex tcc
```

Para gerar as referências bibliográficas, utiliza-se a ferramenta [`bibtex`](http://www.bibtex.org/):

```bash
bibtex tcc
```

E para gerar as referências de siglas/abreviaturas, a ferramenta [`makeglossaries`](https://www.ctan.org/pkg/glossaries):

```bash
makeglossaries tcc
```

Para finalizar, é preciso processar tudo novamente (2 vezes):

```bash
pdflatex tcc
pdflatex tcc
```

O mesmo resultado pode ser obtido usando uma interface gráfica mais amigável, como o [TeXWorks](http://www.tug.org/texworks/), mas geralmente é preciso gerar o glossário separadamente.


### MiKTeX ###

Utilizando a instalação básica da versão 2.9.5105 (Windows XP 32-bit) do [MiKTeX](http://miktex.org/), ao abrir o arquivo ```monografia.tex``` com o editor instalado (TeXWorks), e executando a opção padrão oferecida ```pdfLaTeX+MakeIndex+BibTeX```, o programa indicou a ausência de diversos pacotes; mas já oferecendo a opção de instalação destes. O pacote _glossaries_ depende de _tracklang.sty_, que foi instalado pelo gerenciador de pacotes do próprio MiKTeX (após sincronização). Para gerar o glossário, é preciso instalar PERL e realizar alguns ajustes, há instruções muito claras [neste link](http://latex-community.org/know-how/latex/55-latex-general/263-glossaries-nomenclature-lists-of-symbols-and-acronyms#makeglossaries). Com a versão [ActiverPerl](http://www.activestate.com/activeperl)) 5.20.2 Build 2001, a configurando a opção _makeglossaries_ conforme as instruções, o PDF foi gerado sem problemas.


## Resolução de Problemas ##

**Não há suporte ativo para este projeto**.

Há váprios meios de conseguir ajuda em LaTeX:

  * [Procure na internet](http://bfy.tw/9AHK)
  * [**LaTeX Wikibook**](https://en.wikibooks.org/wiki/LaTeX/)
  * [StackExchange](http://tex.stackexchange.com)
  * [LaTeX Community](http://www.latex-community.org)
