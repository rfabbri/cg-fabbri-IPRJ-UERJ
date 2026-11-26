# Computacao Grafica 2026/2 (fim de 2026 e inicio 2027 devido a greve)

## Informações gerais
- **Professor** [Ricardo Fabbri, Ph.D](http://rfabbri.github.io)
- **Datas** das avaliações teóricas
    - P1: 16/12/2026
    - P2: 7/4/2027
- **Repositorio** principal da disciplina: 
    git clone http://github.com/rfabbri/cg-fabbri-IPRJ-UERJ

## Criterio de Avaliacao

M = 0.4*P + 0.6*T

P = (P1 + P2)/2

T = nota de trabalhos e tarefas

Criterio de medias e prova final padrao UERJ

A maior parte dos trabalhos serao feitos e avaliados na propria aula. Ver
criterio detalhado abaixo.

## Aulas Teoricas

### Livro-texto
- Folley & Van Dam 3a. Edicao (Capa é do filme Ratatouille)
- Real time 3D Graphics (recente)
- Videos e slides isolados conforme descrito para cada aula/tarefa abaixo


- Aula 0 e Aula 1 - ministradas junto com tarefa0 e tarefa1 abaixo

## Aulas Praticas

### Livro-texto
- Referencias vulkan abaixo, secao Onde Apreder
- Ver secao Tarefas abaixo.

## Explicacao sobre este repositorio
Como compilar, etc
ver AGENTS.md
  
## Linguagem
C/C++ com CMake
Python

### Revisao de C, ponteiros, etc.
C/C++ Fabbri Parte 1 https://youtu.be/Gru0DnXWr0g
C/C++ Fabbri Parte 2 https://youtu.be/k0KfKildD-U

## IDE/Ambiente

### IA/LLMs
- Uso de IA será explorado em alguns projetos

### Vulkan

#### Instalando (2026)
- Linux e Mac: 
    - LunarG SDK
    - Tentar sem root

#### Onde aprender
1) Vulkan tutorial (em paralelo 2, vulkan guide)
2) Vulkan guide
3) Mais pratico para game engine: 
    - http://vkguide.dev
    - Sascha Willems’ How to Vulkan in 2026

4) Instalar RenderDoc https://renderdoc.org
    - Instalar usando tarball
    - Debug visual


#### Other resources
    - https://vulkan.org/learn
    - Blender vulkan backend 
        - https://developer.blender.org/docs/features/gpu/vulkan/
        - source/blender/gpu/vulkan

    - Hardware mental model: A Trip Through the Graphics Pipeline (Parts 1–6)
    - Fabian Giesen’s A Trip Through the Graphics Pipeline and 


## Trabalhos


### Envio

Os trabalhos que forem para serem entregues diretamente ao professor devem ser 
enviados para:

rfabbri@iprj...

ATENCAO: subject tem que conter: [cg-iprj]

Porem a maioria das tarefas valendo nota sera semanal e avaliada diretamente
em sala de aula.  Nesse caso:
    - Cada tarefa é dividida em sub-tarefas, denominadas atividades
    - Realizar a tarefa em aula.
        - Cada ativiade tem horário para término
        - A cada término de atividade serão sorteados 2 alunos
            - Se tiverem feito -> ganham bonus de 1 atividade
            - Se nao tiverem feito -> perde o valor de 1 atividade, mas podem
              continar tentando e receberao ajuda direta do professor para terminar
            - Quem nao foi sorteado mantem a nota da atividade normal (conquistada
              por presença).
    - Apos a aula, repetir a tarefa no computaor de casa, caso pertinente
    - Finalizar até 17h de 24nov26 tanto no laboratorio como no computador
      pessoal
    - Na aula seguinte serao sorteados dois alunos, caso nao tiver feito todas
      as aulas anteriores, perde o equivalente `a pontuacao de 1 atividade
    - Ao final do semestre, somam-se as atividades de todas as tarefas e a
      porcentagem de pontos será a nota. Caso exceda 10, por questão de bônus, a
      nota passa para as provas
    - Alunos que ajudarem os demais podem solicitar ao professor um bônus
      equivalente a 1 atividade
    - O mais importante é comparecer às aulas e realizar as provas teóricas,
      sendo aceita falta justificativa oficiada conforme regras da UERJ

### Detalhes, Data de Entrega, etc

A informação de qual tarefa foi passada em que dia pode ser encontrada na secao
Tarefas abaixo, bem como informacoes complementares na pasta correspondeente em
aulas/, quando disponivel. No entanto, é
responsabilidade do aluno comparecer às aulas e ficar atento aos e-mails ou se
inteirar com os colegas que compareceram. Chegar a uma aula sem ter se inteirado
da aula anterior quase sempre irá incorrer na falta de compreensão e perda de
nota em atividades. Sorteio sera feito no inicio de cada aula e, caso o aluno
nao tiver feito a atividade anterior, perde o ponto referente a 1 atividade.
Esta perda de pontos sera cumulativa. Os sorteados, caso tenham feito, iniciam o
dia com 1 ponto a mais de atividade.


### Tarefa 0: contas, referente à Aula 0: qua18nov26

- Obrigatório finalizar até 17h da véspera da próxima aula.

#### Enunciado

Fazer tanto para o computador usado no LAB,
como para seu computador pessoal, caso sejam diferentes:

0.1) criar uma conta github até a mesma data, caso ainda não tenha
0.2) fazer fork do repositorio da disciplina (link no inicio deste arquivo)
0.3) adicionar arquivo hello.cpp manualmente
0.4) submeter a mudanca para seu github pessoal
0.5) realizar um pull request para o hello.cpp apenas a titulo de exeercicio

Teoria: Estudar pipeline geral
- Saber: O que é um shader
    - Tipos de shader (visao geral apenas)
- O que faz uma GPU
    Calculos SIMD
    Otimizada para Modelo -> imagem 2D
    Mas tambem proposito geral: Dados massivos -> Dados massivos onde o
    processamento é repetitivo com poucas decisoes isoladas
- Diferença entre Fixed Function pipeline e Compute Pipeline
- Dierença entre rasterização e ray-tracing
- Otimizada para triangulos, por padrao:
    Modelo -> triangulos -> transformacoes -> rasterizacao/oclusao/z-buffer/cor -> imagem 2D
- Fonte:
    Quadro do professor

#### Diario de aula
- Foram feitos todos os passos acima
- Foi dada a teoria inicial conforme acima
- Criterio de avaliacao foi discutido

### Tarefa 1: vulkan, referente à Aula 1: qua25nov26

#### Plano

1.0) git pull no repo da disciplina
1.1) Instalar Vulkan SDK
1.2) Testar Vulkan SDK rodando vkcube
1.3) Compilar hello

Teoria
- Pipeline lógico padrão baseado em triângulos (foi passada a base referencia AMD e uma ideia de como mapeia para outras marcas)
    - Como as GPUs evoluiram de hardware grafico altamente elaborado 
        - Exemplo Reality Co-Processor / SGI RCP usado no Nintendo Ultra 64, anos 90
        - Placas atuais sao em boa parte simplificacoes para processamento massivo e barato
- Pipeline hardware parão: apenas foi falado por cima
    - Pipeline voltado a execucao de comandos e shaders
- Saber termos tecnicos (1 frase de definicao por termo): 
    - Buffer (no contexto de GPU)
    - Framebuffers
    - Textures
- Fonte:
    - Slides e video: "All the pipelines - journey through the GPU" - Lou Kramer, AMD (youtube)
        - Foram cobertos slides iniciais, antes do pipeline de hardware
    - Complementar com outras arquiteturas

#### Para proxima aula
- Aos que nao fizeram: completar os passos no computador pessoal e no lab

#### Diario de aula
- Foi instalado vulkan SDK em varios computaores, sem necessidade de senha de
  root, baixando-se e instalando renomeando o pacote da SDK para ~/vulkan
- Antes de se executar o ccmake e make, roda-se o setup da seguinte forma
    . ~/.vulkan/versao/setup*sh
- Passos acima que foram realizados
    - Atualizar repo
    - Compilar usando cmake, observar se pede vulkan
    - Se pedir vulkan, instlar SDK da LunarG
        - testar rodando vkcube
        - Recompilar
        - rodar ./hello e repoortar qual a placa de video detectada
- Teoria ministrada nos 40min finais de aula conforme acima
- Alem dos slides acima, foi adotado o livro principal: Folley & Van Dam 3a. ed.

#### Para proxima aula
- Aos que nao fizeram: completar os passos no computador pessoal e no lab
- Praticar Git
    - http://wiki.nosdigitais.teia.org.br/GIT
    - se estiver fora do ar, usar web archive
- Praticar Linux / linha de comando (Obrigatorio)
    - http://wiki.nosdigitais.teia.org.br/LUPE
    - se estiver fora do ar, usar web archive
- Pre-assistir ao video da AMD acima

### Tarefa 2, referente à Aula 2: prevista para sex27nov26
#### Plano
- Objetivo: uso da IA/LLM


2.0) Certificar-se que . ~/.vulkan/versao/setup*sh esta no ~/.bash_profile
2.1) Certificar-se que vkcube e hello realmente estao rodando
2.2) Clicar em Watch no repositorio no Github.com para saber atualizacoes
2.3) Conta de estudante do google gemini ou IA de sua preferencia.
2.4) Testar/Instalar o agy (Google Antigravity) na sua máquina pessoal, que foi o
assistente de programação eleito/justificado em aula.

Teoria
- Continuacao de lousa acerca dos slides e video da AMD: "All the pipelines - journey
  through the GPU" - Lou Kramer, AMD (youtube)
    - Retomando na parte de hardware
    - Conectando com o pipeline logico padrao
    - Traducao dos termos para Nvidia e Intel graphics
        - Exemplo: waves vs warps

#### Diario de aula



## TODO
- abrir ticket de suporte IPRJ (alunos tambem devem): https://atendimento.iprj.uerj.br
    - solicitar softwares ou pacotes
    - qualquer outro problema

- suite de testes (ver TODO em @AGENTS.md)

## See also
- @AGENTS.md for other natural language / LLM instructions
- [Curso anterior](http://wiki.nosdigitais.teia.org.br/CG) (em fase de upgrade)
- Qualquer duvida, o prof. Fabbri se coloca à disposicao para google meet.
