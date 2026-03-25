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

1. Repositório selecionado: https://github.com/sherlock-project/sherlock
2. Gráfico selecionado: 
  a. <img width="1396" height="758" alt="image" src="https://github.com/user-attachments/assets/7d6352f5-dbc5-4301-a310-4549ff5907d3" />

  b. <img width="1364" height="714" alt="image" src="https://github.com/user-attachments/assets/73edb42c-9d85-4161-8fda-b9fd51d4b8ea" />

  c. <img width="1378" height="700" alt="image" src="https://github.com/user-attachments/assets/376c2393-02c7-4863-b5c2-cec454ff66da" />

  d. <img width="1408" height="684" alt="image" src="https://github.com/user-attachments/assets/993b689a-169d-4468-936f-1d922249a1b1" />

  e. <img width="1396" height="686" alt="image" src="https://github.com/user-attachments/assets/597d7454-b678-4e90-bce8-ab405a64a1f7" />

Usei 5 imagens, porque uma única para esse projeto era pouco conclusiva, já que não teve nenhuma mudança muito drástica isolada.

3. Explicação: Com base nos gráficos de Arquivos de Produção vs. Testes, Linhas de Código (LOC) e Arquivos Python, podemos afirmar que a partir de 2025 foi feita uma mudança drástica na cultura do projeto. Ao invés de ser um projeto cujo intuito principal era aumentar features de produção, passou a ser reduzir o tamanho da produção e crescer o tamanho dos testes. Provavelmente essa redução na produção não foi uma perda de features, mas sim uma organização melhor e modularização do código em produção. Analisando o LOC total, que não caiu tão significativamente, mostrando que o código continua lá, apenas redistribuído de forma mais coesa. Essa modularização fica ainda mais evidente no gráfico de LOC média por arquivo, que caiu de significativamente em 2025. Arquivos menores significam responsabilidades mais bem definidas e isso é pré-requisito para testabilidade. O mesmo vale para as funções e classes, que também encolheram no mesmo período. Essa redução consequentemente deve ter ao mesmo tempo ajudado a planejar os testes, quanto os testes a ajudar nessa modularização. Uma relação de causalidade bidirecional onde você testa porque consegue isolar, e isola porque precisa testar. Essa transição de foco demonstra uma maturidade do projeto. Um projeto que saiu de um estado de crescimento acelerado, para correções e crescimento inteligente e organizado.



