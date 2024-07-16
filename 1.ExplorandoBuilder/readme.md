# 🏡 Explorando o Builder
Olá! Seja bem vindo(a) a segunda parte deste curso. Aqui enfim conheceremos a ferramenta Psychopy. Eu fiz um sumário para te ajudar na ordem do conteúdo, okay? Espero que te ajude! :)

## :blue_heart: Sumário
1. [O início de tudo!! Builder View 😊](1.oBuilder.md) <br>
    - Introdução à interface do Builder 
    - Introdução às Routines, Components & Flow
    - Painel de componentes
    - Vamos aprender mais utilizando a plataforma?
      
2. [Vamos aprender com um exemplo?? ✨](2.PosnerCueingTask.md) <br>
    - Posner Cueing Task
    - Adicionando um Rotina
        - Polygon Component
    - Posição e tamanho do componente
        - Spatial Units
    - Configurações globais do experimento
    - Captando uma resposta do teclado (Keyboard Response Component)
    - *Experimento em .psyexp:* [posnercueingtask.psyexp](experimentos/posnercueingtask.psyexp)
      
3. [Repetindo as rotinas! 🍨](3.LoopsNoExperimento.md) 
    - Loop Component
    - Passo a passo | Trabalhando com Loops 
    - Afinal, o que temos ao final do experimento rodar? A pasta `Data`
    - Elementos do Loop
    - `set every frame` vs `set every repeat`
    - Utilizando váriaveis dentro das `Routines`! :exploding_head: 
    - Usando Loops para blocos
    - *Experimento em .psyexp:* [posnercuiengtask_loops.psyexp](experimentos/posnercuiengtask_loops.psyexp)
4. [Feedbacks | Code Component](4.CodeComponentFeedbacks.md)
    - Adicionando Feedbacks e trabalhando com o `Code Component`
    - O `Code Component`
    - Exempo de uso do `Code Component`
    - Parâmetros
    - Noções de lógica de programação
    - Onde seu código será adicionado
    - Adicionando código dentro dos componentes (`Posner Cueing Task`)
    - Enfim, como adicionamos o feedback ao nosso experimento?
    - Como guardar a acurácia das respostas do participante por meio das repostas de teclado?
    - *Experimento em .psyexp:* [posner_withfeedback_codecomponent.psyexp](experimentos/posner_withfeedback_codecomponent.psyexp)
5. [Indo além: Como posso misturar dados de texto e imagens dentro dos meus loops em blocos de trials? 🤔](5.indoalem.md)
5. Exercício
    - Crie um experimento (pode utilizar o do Posner Cueing Task também), adicione uma rotina de instruções no início do experimento e permita que o participante pressione a barra de espaço para passar.
    - Adicione uma rotina que agradece ao participante no final do seu experimento.
    - Adicione novos campos às configurações iniciais do seu experimento que captam mais informações, como _handedness_ (lateralidade) e _age_ (idade).
    - *Experimento em .psyexp:* [exercicio.psyexp](experimentos/exercicio.psyexp)
6. [Animando os componentes](6.AnimandoComponentes.md)
    - *Experimento em .psyexp:* [dynamic.psyexp](experimentos/dynamic.psyexp)
