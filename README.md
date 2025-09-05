# Explorando evolução de código

Neste exercício, iremos explorar a evolução de código em sistemas reais.

Iremos utilizar a ferramenta [GitEvo](https://github.com/andrehora/gitevo).
Essa ferramenta analisa a evolução de código em repositórios Git nas linguagens Python, JavaScript, TypeScript e Java, e gera relatórios `HTML` como [este](https://andrehora.github.io/gitevo-examples/python/pandas.html).

Mais exemplos de relatórios podem ser podem ser encontrados em https://github.com/andrehora/gitevo-examples.

# Passo 1: Selecionar repositório a ser analisado

Selecione um repositório relevante na linguagem de sua preferência (Python, JavaScript, TypeScript ou Java).
Você pode encontrar projetos interessantes nos links abaixo:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

# Passo 2: Instalar e rodar a ferramenta GitEvo

> [!NOTE]
> Antes de instalar a ferramenta, é recomendado criar e ativar um [ambiente virtual Python](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#create-and-use-virtual-environments).

Instale a ferramenta [GitEvo](https://github.com/andrehora/gitevo) com o comando:

```
$ pip install gitevo
```

Execute a ferramenta no repositório selecionado utilizando o comando abaixo (ajuste conforme a linguagem do repositório).
Substitua `<git_url>` pela URL do repositório que será analisado:

```shell
# Python
$ gitevo -r python <git_url>

# JavaScript
$ gitevo -r javascript <git_url>

# TypeScript
$ gitevo -r typescript <git_url>

# Java
$ gitevo -r java <git_url>
```

Por exemplo, para analisar o projeto Flask escrito em Python:

```
$ gitevo -r python https://github.com/pallets/flask
```

> [!NOTE]
> Essa etapa pode demorar alguns minutos pois o projeto será clonado e analisado localmente.

# Passo 3: Explorar o relatório de evolução de código

Após executar a ferramenta [GitEvo](https://github.com/andrehora/gitevo), é gerado um relatório `HTML` contendo diversos gráficos sobre a evolução do código.

Abra o relatório `HTML` e observe com atenção os gráficos.

# Passo 4: Explicar um gráfico de evolução de código

Selecione um dos gráficos de evolução e explique-o com suas palavras.
Por exemplo, você pode:

- Detalhar a evolução ao longo do tempo
- Detalhar se as curvas estão de acordo com boas práticas
- Explicar grandes alterações nas curvas
- Explorar a documentação do repositório em busca de explicações para grandes alterações
- etc.

Seja criativo!

# Instruções para o exercício

1. Crie um `fork` deste repositório (mais informações sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Adicione o relatório `HTML` no seu fork.
3. No Moodle, submeta apenas a URL do seu `fork`.

Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork:

1. Repositório selecionado: https://github.com/Significant-Gravitas/AutoGPT
2. Gráfico selecionado: <img width="858" height="401" alt="image" src="https://github.com/user-attachments/assets/d3737266-2ed5-42e7-af57-1b03c9536b50" />

3. Explicação:
O gráfico mostra a evolução dos comandos de controle de fluxo no repositório AutoGPT, revelando como o código foi crescendo e se tornando mais complexo. O destaque é o if, que salta de quase nada em 2023 para mais de mil ocorrências em 2024 e chega a cerca de 1,6 mil em 2025. Esse aumento indica que o projeto foi ganhando camadas de lógica, ramificações e condições para lidar com diferentes cenários. Já os outros comandos — for, try, with, while e match — crescem em menor escala, mas de maneira consistente.

Esse padrão se conecta à história do AutoGPT. Em 2023, o repositório nasce como um protótipo experimental, com uso ainda limitado de estruturas de código. No ano seguinte, a equipe organiza o projeto em duas frentes: o “AutoGPT Classic”, mantido de forma limitada, e a “AutoGPT Platform”, que se torna o foco principal. Essa transição traz uma explosão de novos módulos, workflows e integrações, explicando o crescimento expressivo das estruturas condicionais.

Em 2024 também aparecem mais try e with, reflexo do amadurecimento do projeto. O sistema passa a lidar com recursos externos, filas e agendadores, exigindo mais tratamento de erros e gerenciamento de contexto. Já o baixo uso de while faz sentido, porque a arquitetura baseada em eventos e workers não depende de loops manuais, enquanto o match continua discreto por ser um recurso ainda relativamente novo do Python, adotado com cautela.

O crescimento segue em 2025, mas de forma mais estável. As releases mostram que a plataforma se consolida com backend robusto, integração de filas e suporte a novos ambientes, o que gera pequenas adições de controle de fluxo dispersas em diferentes partes do sistema. Esse movimento traduz o amadurecimento do código: menos “explosão” e mais evolução incremental.

No geral, o gráfico revela um padrão saudável. Mais condicionais e tratamento de erros significam que o código foi ficando mais resiliente e adaptado a múltiplos cenários. O único ponto de atenção é a alta concentração de if, que pode indicar trechos de lógica muito ramificada e, portanto, candidatos a refatorações. Ainda assim, as curvas confirmam a narrativa do repositório: de protótipo em 2023, para grande expansão em 2024, até a consolidação e amadurecimento em 2025.



