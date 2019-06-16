# Curso Introdutório de Python3

A linguagem de programação Python é, atualmente, um das mais utilizadas. A maioria das universidades americanas ensinam a programar com ela. Ela tem substituído o Java e o C/C++ na preferência de primeira linguagem de programação.

Isto se justifica pela simplicidade da linguagem. Ela é simples para se aprender e fácil de usar. Não sendo compilada, não há a necessidade de entender o processo de compilação, a diferença entre código fonte e código compilado. Por não ser fortemente tipada, não há a necessidade de pré-declarar as variáveis e seus tipos.

É óbvio que estas simplificações vêm com um preço. Mas este é um custo que o programador só sente quando avança para programar alguns tipos de aplicações mais sofisticadas e complexas. Isto não significa que o Python não possa ser usado para programar aplicações complexas, prova disto é que o Python é usado bastante em Inteligência Artificial, especificamente, em Deep Learning e análise de dados.

Neste curso, usaremos um ambiente de programação que deve facilitar o aprendizado, o notebook Jupyter. Para ter acesso a este ambiente, recomendamos a instalação da [Distribuição Anaconda](https://www.anaconda.com/distribution/). Esta é uma distribuição bastante completa de Python com a maioria dos pacotes necessários para  a análise de dados.

Este curso usa o Python3, apesar de existir ainda muita coisa em Python2, a maioria das coisas importantes migraram para o Python3. Futuros desenvolvimentos devem ser feitos na versão 3.

As lições estarão em arquivos de notebook Python que permitem misturar células de texto em Markdown com células de código. Este curso é baseado em exemplos e prática. Isto é, as lições terão textos para explicar os conceitos básicos, exemplos de códigos para serem executados e exercícios que os alunos deverão resolver e testar. Como sempre acontece com programação, existe mais de uma maneira de resolver um problema, o aluno não deve tentar chegar na solução do instrutor, mas encontrar suas próprias soluções. Entretanto, o estudo do código dos outros pode e deve ser instrutivo. É importante aprender técnicas usadas pelos outros programadores e incorporá-las ao nosso acervo de ferramentas de programação.

Este curso é fortemente baseado no tutorial online oferecido pela [W3Schools](https://www.w3schools.com/python/) e nas referências [2] e [3].

## Alguns fatos sobre o Python

- Python foi criado Guido van Rossum e disponibilizado em 1991.
- Python é multiplataforma, existe para MS Windows, MacOS, Linux e outros.
- Python é usado para:
  + desenvolvimento WEB no lado do servidor;
  + desenvolvimento de software;
  + matemática (cálculo numérico) e
  + scripts de sistema, muito usado no Linux e no MacOS.
- Algumas das coisas que podemos fazer com o Python são:
  + Python pode ser usado num servidor para criar uma aplicação WEB;
  + Python pode ser conectado a SGBDs (Sistemas de Gerenciamento de Banco de Dados), tanto para a leitura como para a modificação dos dados;
  + Python pode ser usado para manipulação de Big Data e para complexos cálculos matemáticos e
  + Python pode ser usado para prototipagem rápida ou para desenvolvimento de software pronto para a produção.
- Python foi criado para legibilidade e tem semelhanças com a língua inglesa com influências da matemática;
- Python usa saltos de linha para terminar uma instrução no lugar do ponto-e-vírgula da maioria das linguagens, ou dos parenteses como em LISP;
- Python baseia-se na identação (espaço em branco antes de começar o texto numa linha) com espaços para definir os blocos de códigos de instruções condicionais, malhas de repetição \(loops\), funções e classes. Outras linguagens usam chaves ou palavras chaves marcadoras como *begin* e *end*.

## Instalação do Python

O Python vem pré-instalado em sistemas como o MacOS e linux. Mas, frequentemente, a versão instalada não é a que usaremos. Por exemplo, no MacOS, a versão pré-instalada é a 2. Além disso, frequentemente, estas versões pré-instaladas não são as mais atualizadas e podem apresentar problemas de segurança. Assim, é importante instalar a última versão.

Duas possibilidades devem ser consideradas, a instalaçao oficial a partir do site [Oficial do Python](https://www.python.org/downloads/), ou a [Distribuição Anaconda](https://www.anaconda.com/distribution/). Esta segunda é a que preferimos por já incluir a maioria dos pacotes que podemos desejar para trabalhar com o Python na análise de dados. Seu inconveniente é que muitos dos pacotes incluídos podem não ser necessários. Além disso, ele oferece uma maneira não padrão de gerenciar a instalação dos pacotes e de gerenciar os ambientes de desenvolvimento de Python.

É importante saber usar a interface da linha de comando, vulgo *Prompt do DOS* no MS Windows ou *terminal* no Linux ou MacOS. Para saber a versão do Python, na linha de comando, faça:

```
python --version
```

Isto mostra que o Python está corretamente instalado no seu sistema e que ele é acessível pela interface da linha de comando. Nos sistemas onde as duas versões de Python estão instaladas, no lugar de python, use python3 nos comandos. Para completar o teste da instalação, use um editor de texto (notepad no caso do MS Windows, gedit ou nano no Linux) e crie um arquivo: alomundo.py com o seguinte conteúdo:

```
print("Alo, Mundo!")
```

  Não use processadores de texto como o MS Word para editar o arquivo,
  processadores de texto não criam arquivos de texto puro, eles adicionam
  ao texto escrito comandos de formatação que vão confundir o
  interpretador Python. Além do notebook Jupyter que iremos usar no curso,
  os programas Python podem ser escritos com editores de texto como o notepad++,
  emacs, vi, gedit, atom, brackets ou editores de ambientes de programação.

Salve tomando o cuidado de que a extensão é .py. O MS Windows tem o mal hábito de acrescentar uma extensão .txt, o nome real do arquivo fica: *alomundo.py.txt* se o arquivo for salvo como arquivo de texto no notepad, para evitar isto selecione *Todos tipos* na janela para Salvar o arquivo. O comando *dir* revela o nome e a extensão correta dos arquivos, o *explorer* (navedor de pastas do MS Windows) não mostra extensões conhecidas e, em geral, não mostra o .txt. Tendo o arquivo, ele pode ser executado na linha de comando com:

```
python alomundo.py
```

E deve imprimir uma linha com o texto: **Alo, Mundo!**

### Instalação de pacotes

#### Sem anaconda

O processo normal de instalação de pacotes no Python é usando o comando pip na linha de comando \(em alguns casos, o pip podem não ter sido compilado para o seu sistema e nesse caso você terá de usar *python pip-script*.\).

Para saber quais pacotes estão instalados no seu sistema, faça:

```
pip list
```

Se os pacotes jupyter, ipython e/ou notebook não estiverem instalados, você pode instalá-los com:

```
pip install jupyter ipython notebook
```

No lugar de *install* é possível usar *update* para atualizar estes pacotes se necessário.

#### Com Anaconda (ou miniconda)

Na distribuição Anaconda do Python, o programa *conda* gerencia os pacotes e os ambientes isolados de programação. Para instalar ou atualizar os pacotes simplesmente use o conda no lugar de *pip*.

Exemplo

```
conda install jupyter ipython notebook
```

Isto não deve ser necessário se você instalou o Anaconda, mas pode ser necessário se você tiver criado um ambiente mínimo ou instalado o miniconda.

## Arquivos .ipynb

Os arquivos notebook de Python têm extensão .ipynb. É neles que estão as lições deste curso.

Os arquivos de notebbok do Python são compostos por células. Estas células podem ter texto em formato Markdown, como neste arquivo README.md ou código Python. Para usar estes arquivos, execute o programa notebook-jupyter que deve ter sido instalado com o Anaconda. Ele vai iniciar um servidor com o interpretador e conectar o seu navegador preferido ao servidor.
![Jupyter Notebook](note_tree.png)

Para começar um interpretador (kernel) para executar os códigos de um arquivo notebook, como o licao1.ipynb da figura, basta clicar no arquivo.
![Jupyter Notebook licao1.ipynb](note_licao1.png)

Aí, você pode executar cada célula  de código ou executar todas as células de uma vez.

### Referências

1. [Python Tutorial](https://www.w3schools.com/python/), https://www.w3schools.com/python/, acesso em 16/06/2019.

2. Jamie CHAN, Learn Python in one day and Learn It Well, Learn Coding Fast, 2014.

3. Tariq RASHID, Make Your Own Neural Network, 2014.
