# Psychopy | Um guia passo a passo.

:tophat: Precise enough for psychophysics. <br>
:books: Intuitive enough for undergraduate psychology.<br>
:dna: Flexible enough for everything else.<br>
:computer: Capable of running studies in lab or online.

## Sumário

1. [Quem criou](#quem-criou)<br>
2. [O que é o Psychopy?](#o-que-é-o-psychopy)<br>
3. [PsychoJS](#psychojs)<br>
4. [Pavlovia](#pavlovia)<br>
5. [O Software](#o-software) <br>
    - [Instalando o Psychopy](#instalando-o-psychopy) <br>
        - [Windows](#windows) <br>
        - [Linux](#linux) <br>
            - [Instalando uma versão do python compatível com o Psychopy](#instalando-uma-versão-do-python-compatível-com-o-psychopy)<br>
                - [Pré Requisitos](#pré-requisitos)<br>
                - [Requirements, versões utilizadas por mim](#requirements)<br>
                - [E se eu já tinha uma versão do python no meu computador](#e-se-eu-já-tinha-uma-versão-do-python)<br>
                - [Problema com o wxPython Wheel](#problema-com-o-wxpython-python-wheel)<br>
        - [MacOS](#macos) <br>


    

### Quem criou
O psychopy, psychoJS e o Pavlovia são ferramentas criadas pelo Open Source Tools group. Eles são uma empresa da Inglaterra que apoia o desenvolvimento de programas open sciente em prol de uma ciência para todos com ferramentas de alta qualidade de custo mínimo. O grupo foi criado por causa do desenvolvimento do Psychopy. Inicialmente, o projeto foi pensado para ser desenvolvido em prol de contribuir o desenvolvimento mais prático de cientistas do próprio lab, mas cresceu de tamanho de forma exponencial, e por isso, decidiram construir a empresa e formalizar a produção do software. Hoje, em 2024, o Psychopy tem mais de 200 contribuidores no github.

### O que é o Psychopy?
O Psychopy é um software criado por John Peirce na Universidade de Nottingham, na Inglaterra. O aplicativo é open-source e é disponibilizado para Windows, macOS e Linux. O processo de instalação em um sistema operacional Linux demanda mais dedicação e cuidado, mas nada que não possa ser feito seguindo o passo a passo. Neste artigo irei apresentar o passo a passo de como instalar nos 3 ambientes citados anteriormente. 
Este programa possui características e atributos tanto para quem já tem um background em computação, quanto para quem não tem. No site oficial, eles mostram que o Psychopy é perfeito para criar experimentos de psicologia, psicolinguística, comportamental e econômico. 

_Stimulus presentation_ são os estudos feitos quando se apresentam inputs que provocam um comportamento do participante do estudo, causando respostas neurais e comportamentais. Por exemplo,  o Stroop Effect, uma demonstração de interferência no tempo de reação de uma tarefa, utiliza de palavras e cores para realizar um experimento onde, por analisar os dados de resposta de tempo do paciente, deduz que quando as palavras e cores coincidem o tempo de reação é mais rápido.  

É notório que esse tipo de estudo é bem utilizado para realização de pesquisas nas mais diversas áreas. Assim, é neste contexto que o software psychopy entra. Ele é um ambiente programado para facilitar a criação de experimentos utilizando a linguagem de programação python. Dado que muitos pesquisadores desta área não são familiarizados com programação, o software foi desenvolvido para atender os dois tipos de público: coders e não coders.

:bulb:
    Objetivo do Psychopy: permitir que cientistas rodem a maior quantidade de experimentos possíveis, de forma fácil e rápida. 


### PsychoJS

Já notou que os experimentos demandam um setup bem programado para acontecer? Bem, normalmente é assim que acontece na pesquisa. Os participantes são convidados a estar no laboratório e realizar o experimento muitas vezes em um ambiente um pouco desconfortável para o usuário. Assim, foi criado o PsychoJS, uma biblioteca do Javascript feita para rodar experimentos do Psychopy online  por meio da plataforma Pavlovia. Desse modo, é mais fácil utilizar e rodar experimentos de outros aparelhos eletrônicos assim como coletar dados para a pesquisa. 

O link abaixo provides o que está disponível no PsychoJS que pertence ao Psychopy, e o que ainda está em fase de desenvolvimento ou não está disponível. https://www.psychopy.org/online/status.html

### Pavlovia
O Pavlovia é uma plataforma online que foi originalmente pensada para ser um repositório de experimentos criado com o Psychopy. Porém, hoje, ela suporta outras ferramentas de open-source como o  jsPsych e lab.js. Ela é utilizada para rodar, compartilhar e explorar experimentos online. Além disso, ainda possui fóruns de discussões que promovem a contribuição entre os pesquisadores e usuários do Psychopy.

-  É baseada no sistema de controle de versão Git. Possui um Pavlovia’s GitLab. Logo, caso o usuário queira utilizá-lo com o Git, é possível, porém é necessário tem o ambiente do Git instalado em sua máquina local. https://pavlovia.org/docs/experiments/create-fork
- É um servidor para hostear experimentos e projetos.
- É um repositório de experimentos.

A ideia é criar o experimento para rodar online também, fora do Psychopy local, e hospedá-lo ao publicar no Pavlovia. Desse modo, qualquer pessoa será capaz de rodar o seu experimento por meio do site.

## O software
Como já foi citado anteriormente o Psychopy é um software open-source e disponível na plataforma oficial para download. Então nesta sessão, iniciaremos a abordar como o software funciona e como seus componentes se comportam. 

### Instalando o Psychopy
Dependendo do sistema operacional do seu computador, você precisará seguir passos diferentes para instalar o software. Vou separar em três tópicos, fique à vontade para pular para onde é o para você.
#### Windows 
Para o windows, o processo é fácil e bem rápido. Basta entrar no site oficial da plataforma, [psychopy.org](https://www.psychopy.org/download.html), e instalar o pacote standalone do programa. Logo você terá acesso ao programa e poderá acompanhar o passo a passo deste tutorial.

#### Linux
Enquanto eu estava estudando o Psychopy, usava um computador com o sistema Linux, tive muitos problemas quanto à versão do Python que estava instalada e com outros pacotes que o psychopy precisa e que eu não tinha na máquina. Lendo a documentação, é reforçado e sugerido algumas configurações específicas para que se consiga instalar. Dado isso, eu fiz um pipeline para instalação do Psychopy. Vou compartilhar abaixo.

Primeiramente, o Psychopy só funciona com versões específicas do Python, infelizmente. As versões acima da `Python 3.10` não funcionam devido a incompatibilidade de pacotes. Vou deixar abaixo o comentário de um dos mantenedores em uma discussão no próprio site sobre o assunto: 

```
"Regarding Python upgrades in general, the reason that PsychoPy has always been slow to update to the latest releases of Python is that we have a very large number of dependencies and although we can get our own code into a compatible state that doesn’t mean the other libraries reach the same. Hardware manufacturers especially fall into this category since they often have to build specific releases for each Python version due to changing compiler compatibilities"
```
[Referência: discourse.psychopy.org/t/what-is-the-state-of-python-3-10-support](https://discourse.psychopy.org/t/what-is-the-state-of-python-3-10-support/27303/3)

Desse modo, é preciso ter alguma das versões do python que suportam o programa. Logo, como eu não tinha (tenho a 3.12), tive que instalar no meu PC, outra dor de cabeça...Vamos para o passo a passo!

#### Instalando uma versão do python compatível com o Psychopy
> Descobri que o standalone do Psychopy funciona com o Python3.8!


##### Pré Requisitos
Antes de tudo, você deve ter alguma versão do python3 instalada no seu computador. Caso não tenha ainda, pule o início do tópico [E se eu já tinha uma versão do Python?](#e-se-eu-já-tinha-uma-versão-do-python), rode a seguinte linha de comando no seu computador...
```
sudo apt-get install python3.9
```
E agora volte ao tópico supracitado seguindo apartir do passo 4! (ps: sobre ambiente virtual)

>Eu estou utiizando o gerenciador de pacotes do python chamado `pip` para realizar as instalações que você verá a seguir. Caso você ainda não tenha, entre no terminal do seu computador e rode a seguinte linha de código.
```
sudo apt update
sudo apt install python3-pip
```

> :clock1: Aviso: O processo de instalação do wxPython pode ser bem demorado :(
##### Requirements
Bom, eu havia separado as versões de cada pacote que eu estava usando no computador da pesquisa e que deu certo. Vou deixar aqui caso você possa precisar.
```python
Python 3.10
GTK3
Python3.10-venv
WxPython 4.2.1
PsychoPy
```

##### E se eu já tinha uma versão do Python?
Eu decidi instalar o `Python3.9` na minha máquina. Mas como, se eu já tinha o `Python 3.12`? Bom, segue esse pipeline!

1. Fazer o download da versão do python no site oficial. Eu fiz o download desta versão: [python-3.9.18 release](https://www.python.org/downloads/release/python-3918/)
2. Instalei-o no meu computador da seguinte forma: Extraí os arquivos para uma pasta, abri o terminal dentro da pasta, e depois rodei os seguintes comandos no terminal.
    ```
    ./configure
    make
    sudo make install
    ```
3. Agora já temos a nossa nova versão do python instalada! Para conferir, você pode rodar esse comando no terminal e decobrir onde ela está localizada:
    ```
        which python3.9
    ```
4. Pronto, tendo o python em sua versão correta, eu criei um ambiente virtual para a instalação do Psychopy.
    ```
        python3.9 -m venv .venv
    ```
5. Finalmente podemos rodar o comando de instalação do `Psychopy` :smiley:.
    ```
        pip install psychopy
    ```
##### Problema com o wxPython, Python wheel
> :rotating_light: Caso apareça um erro durante a instalação com relação ao Python wheel, ou a sua falta, leia essa seção, ela pode ser para você. Caso tudo tiver rodado e você estiver vendo o programa no computador, nem se preocupe! 

Na documentação do site, eles sugerem que instale-se o Psychopy primeiro e depois dê um `fetch` com um ` wxPython wheel `. Porém isso não funcionou para mim, eu precisei instalar o ` wxPython wheel`  primeiro.

1. Faça o download da `wxPython wheel`que cabe no seu sistema operacional por meio deste link: [https://extras.wxpython.org/wxPython4/extras/linux/gtk3/](https://extras.wxpython.org/wxPython4/extras/linux/gtk3/). 

2. Caso não haja, como aconteceu comigo (estava usando o Ubuntu 23.04), é necessário construir. Para isso, eu segui esse passo a passo: [https://wxpython.org/blog/2017-08-17-builds-for-linux-with-pip/index.html](https://wxpython.org/blog/2017-08-17-builds-for-linux-with-pip/index.html). Apesar deles recomendarem instalar vários pacotes, eu instalei apenas um e já funcionou para mim:
    ```
    sudo apt-get install libgtk-3-dev
    ```
3. Logo, instale o wxPython
    ```
    pip install wxpython
    ```
4. Finalmente, ufa, instale o psychopy
    ```
    pip install psychopy
    ```


#### MacOS
_todo!()_


