# Guia do Commit camarada

```
- Ow, o que este commit "subindo projeto" faz?
- Sei lá, abre o código aí.
- Assim não, né amigo...
```


Já passou por isso? Uma tremenda mancada, não? Pega uma cadeira e vamos conversar sobre como escrever aquela mensagem de *Commit Amigável*.

A premissa é simples: Sem padrão, o `git log` vira _aquela_ salada de frutas.

Vamos melhorar isso levando em consideração os seguintes pontos:

* A navegação simplificada pelo histórico de commits
* Manter um padrão entre nós, desenvolvedores
* Passar o contexto da mudança
* Ajudar na mantenabilidade do projeto em longo prazo
* Facilitar a geração de `changelog`


## Como alcançar este `log` que jorra leite e mel?


O time tem que concordar nos seguintes aspectos:

**Estilo**: sintaxe, gramática, capitalização, pontuação. Elabore essas coisas, remova o jogo de adivinhação e faça tudo o mais simples possível.

**Conteúdo**: que tipo de informação deveria conter no corpo da mensagem de commit? ou se não deveria conter

**Metadata**: como devemos rastrear as referencias das issues, por IDs, pull request ou o que deve ser utilizado como referencia?


Pois depois de tudo que foi dito acima você gostaria de ver um log assim:

* 3930c9 Merge header (pull request #10)
* 22ci30 (style): adicionado in-line blocks
* 0d9c93 (hotfix): alterado padding do formulario 
* 9d910c changelog: atualizado


ao invés de algo similar a isto

* 3930c9 adicionado dropdown
* 22ci30 adicionado componentes
* 0d9c93 adicionado checkbox
* 9d910c subindo projeto


## Anatomia do Commit camarada

Já existem convenções bem estabelecidas. No nosso caso, usaremos o guia maravilhoso do _Karma Commit Messages_.

*Formato Bonitão*

```
<tipo>(escopo): assunto

<corpo>

<rodapé>
```


### Assunto

* Máximo de 50 caracteres
* Tipo de escopo devem estar em letras minúsculas
* Assunto deve estar no _imperativo_

Exemplo:

`feat(bregumelo): adiciona endpoint /whatever/`.

Os valores permitidos para o `tipo` são:

* feat _(nova funcionalidade)_
* style _(formatação geral no código. Não confundir com CSS)_
* refactor _(refatoração de código de produção)_
* test _(adicionar/refatorar testes)_
* fix _(adivinha qual é esse)_
* docs _(e esse também)_
* chore _(atualização de tarefas ou código que não está relacionado a produção)_


### Corpo


* Deve conter o `o que` e o `por que` ao invês de conter o `como` foi feito
* Máximo de 80 caracteres

Se é necessário contextualizar o commit, explicar o porquê das mudanças, fique a vonts!

Exemplo:


```
refactor(bregumelo): modifica a chamada do model

A chamada anterior sofreu alterações de contrato, logo, foi necessário
refatorá-la.

```


### Rodapé


Basicamente, um indicador de metadados. Aqui você referencia quais issues estão relacionadas, qual issue este commit encerra e etc.

```
refactor(bregumelo): modifica a chamada do model

A chamada anterior sofreu alterações de contrato, logo, foi necessário
refatorá-la.

Closes #123
```


## Links


* [Karma Commit Messages](http://karma-runner.github.io/6.4/dev/git-commit-msg.html)