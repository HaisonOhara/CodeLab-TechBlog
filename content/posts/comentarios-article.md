+++
title = "Comentários, Amigos ou Inimigos?"
date = 2025-12-13
author = "Haison Ohara"
tags = ["clean code", "boas práticas", "programação"]
categories = ["desenvolvimento"]
draft = false
+++

---

## Comentários, Amigos ou Inimigos?

Hoje, irei dar algumas dicas sobre comentários, sim, essa parte de nossos códigos que utilizamos para explicar um pouquinho melhor aquilo que já foi feito. Iremos descobrir que comentários podem tanto ajudar quanto prejudicar nosso código. Então, chega de papo, e vamos direto ao que interessa!

### Explique-se no código

Isso deve ser o centro de tudo, é daqui que deve partir toda e qualquer indagação sobre utilização de comentários. Resumidamente, um código deve ser claro o suficiente a ponto de ser autoexplicativo, por isso, na maioria das vezes, a presença de um comentário já revela que não foi possível chegar a esse nível de entendimento. Sim! O comentário é um indício de que o código não está claro, afinal de contas, por que escrever um comentário de 3 linhas sobre um if, sendo que um código bem organizado e nomeado, poderia naturalmente se explicar durante todo esse trecho? Aqui o que precisamos entender é que em 90% das vezes que pensamos em comentar um trecho de código, ele, na verdade, está mal escrito. Na maioria das vezes, um código limpo irá dispensar qualquer comentário.
![](/comentarios-01.png)

![](/comentarios-02.png)
Perceba a diferença no primeiro exemplo, o if estava tão claro que não foi necessário incluir um comentário.


## Exemplos de Comentários Aceitáveis

### Comentários informativos

São aqueles que nos informam algo sobre o código (ah jura?). Um exemplo, seria uma breve explicação de um método antes que ele seja executado, algo como:

![](/comentarios-03.png)

Naturalmente, podemos notar que nesse caso, uma nomenclatura mais elaborada poderia trazer clareza a esse trecho, algo como: responderBeingTested(); logo, esse tipo de comentário pode ser excluído quando nomeamos melhor as variáveis envolvidas. No entanto, se for usado de forma clara e objetiva, sem problemas. Só tome cuidado com os excessos.

### Comentários de Intenção

Comentários de Intenção são, basicamente, comentários onde explicamos o motivo de uma decisão em um código, ou seja, ele revela nossas intenções por trás de um trecho específico. O porquê seguimos a lógica que ali está aplicada, quais características do problema foram consideradas, e etc.

Esse tipo de comentário, na minha opinião, pode sujar um código. Entretanto, se usado com moderação e sabedoria, pode ser uma boa ferramenta para contextualizar novos integrantes da equipe. Ainda assim tenho minhas ressalvas quanto a esse comentário, pois acredito que uma documentação bem feita do Software, poderia, inclusive, explicar as motivações de trechos dos códigos mais "cabeludos".

### Comentários de Esclarecimento

Nem tudo no mundo são flores… Você já deve ter ouvido essa frase, e no mundo da tecnologia não seria diferente! Por vezes somos obrigados a utilizar bibliotecas que resolvem nossos problemas mas que não possuem uma nomenclatura explicativa. Nestes casos, explicar o que determinadas partes do código estão fazendo, pode ser útil, mas tome cuidado, você não quer induzir ninguém ao entendimento errado do código! Eu recomendo utilizar o Comentário de Esclarecimento quando você tiver duas certezas em mente:

1. Não há algo melhor a ser feito para que esse código possa ser compreendido.
2. Eu tenho total certeza do que estou falando, não irei induzir ninguém a uma confusão.

### Comentários de Alerta

Estes comentários são aqueles em que avisamos sobre determinado trecho do código. E não, isso não te dá abertura para escrever coisas desse tipo:

![](/comentarios-04.png)

O ideal, aqui, seria avisar sobre coisas que são praticamente inevitáveis, algo como um caso de teste que demore demais para ser executado. Assim, você pode comentar logo acima dele, explicando que ele foi desabilitado num primeiro momento devido ao tempo de execução, mas que pode ser executado sempre que houver um tempo disponível. Existem formas melhores de fazer isso, mas para esse objetivo, o comentário pode ser útil também.

### Comentários ToDo

![](/comentarios-05.png)

Começo esse com uma pergunta: qual foi a última vez que você voltou a um código para melhorar/implementar aquele trecho que você marcou um "ToDo" como comentário?

Sinceramente, a resposta dessa pergunta vai indicar a utilidade desse comentário para você. Eu, particularmente, não gosto. Em boa parte das vezes, me envolvo no código, resolvo o problema e esqueço daquele ToDo feito há 2 dias. Por isso, prefiro priorizar o que deve ser feito. Para mim, um ToDo é uma task futura escondida, assim, nesse caso, é melhor registrá-la no JIRA (ou em qualquer outra plataforma com esse fim) do que dentro do seu próprio código. Mas se mesmo assim você preferir usar um ToDo, tudo bem (só não será convidado para o meu aniversário), existem ferramentas que potencializam os ToDos, evitando que você se esqueça deles (Sonar, por exemplo), e podendo ajudar bastante. Lembre-se que é sempre uma questão de manter o código claro e limpo. Então se você usa esses comentários e consegue manter a qualidade do código, vá em frente :).

---

## Comentários Ruins

Agora é hora de tirar as crianças da sala, vamos falar dos Comentários Ruins, aqueles que você deve evitar a todo custo no código.

### Qualquer comentário mal escrito

Como ressaltamos até esse momento, comentários na maioria das vezes podem (e muitas vezes, devem) ser dispensados. Contudo, nos casos em que eles são necessários, devemos fazê-los com muito cuidado, escrever de forma clara para que QUALQUER leitor possa utilizar seu código. Não esqueça, se nosso código precisa ser claro, nossos comentários também precisam ser!

### Comentários redundantes

Tenho certeza que em algum momento da sua vida, você encontrou algum código parecido com isso:

![](/comentarios-06.png)

Observe como este comentário tem uma utilidade total de 0%, ele literalmente explica o que o código já deixa claro.

Comentários assim, servem somente para poluir o seu código, e consequentemente, dificultar todo o entendimento.

### Comentários Longos

Esse é bem claro, comentários longos somente poluem código, evite-os a todo custo, não escreva textos enormes em seus comentários. Existem lugares específicos para esse tipo de detalhamento, como uma documentação do seu Software, ou um artigo no Medium, caso você esteja muito inspirado.

### Códigos como comentários

![](/comentarios-07.png)

Exemplo retirado de Código limpo: Habilidades práticas do Agile Software(Robert C. Martin)

Para mim, esses são os piores. É mais válido você colocar um link no seu código para esse site aqui: http://www.pudim.com.br/, tenho certeza que será mais útil.

Códigos comentados, na maioria das vezes, não explicam nada, eles ficam ali, perdidos commit após commit, ninguém sabe se eles são um lembrete, se são importantes, ou mesmo, se são o resto perdido do código de alguém. Resumindo, eles são inúteis. A própria ideia de se salvar trechos de código como comentário para se ter um histórico, já deixou de fazer sentido desde que ferramentas de versionamento de código como o git passaram a ser utilizadas, e olha que já faz um tempinho hein…

### Comentários Enganadores

Sabemos que, no fim do dia, nós programadores e programadoras, só queremos fazer um código bom e claro, porém, é comum encontrarmos comentários com informações bem confusas, ou mesmo informações que deixaram de ser verdade há um tempo. E qual seria o problema disso? Esses comentários criam o ambiente perfeito para alguém desavisado passar boa parte do dia tentando resolver um bug, com a única certeza de que aqueles comentários são a mais pura verdade, quando na verdade, eles são imensas desinformações, que podem, inclusive, estar omitindo uma informação que resolveria esse bug em minutos.

---

## Conclusão

Existem muitos outros tipos de comentários bons e ruins, recomendo fortemente a leitura do livro Clean Code (do nosso famoso Uncle Bob), livro que usei como referência para este artigo. Garanto que você irá encontrar um aprofundamento muito bom sobre esse assunto, e muitos outros por lá.

Por hoje é só galerinha, espero ter ajudado de alguma forma. Até a próxima! :)

### Referência:

Código limpo: Habilidades práticas do Agile Software(Robert C. Martin)
