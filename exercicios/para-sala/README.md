# Exercício de Sala 🏫  

## Nome do Exercicio: evoluindo dashboard no Tableau
- Bases utilizadas: `base_final_s14_olist.csv` e `estados_brasileiros.csv` (opcional)

## Passos importantes para construção do nosso dasboard:

### Como criar um Campo Calculado?
Análise > Criar campo calculado

Exemplo:

Função para retorna em dias, o tempo levado entre o pedido do cliente e a entrega.


`DATEDIFF('day', [Order Purchase Timestamp], [Order Delivered Customer Date])`

Função para retornar classificação


`RANK(SUM([Price]))`

### Como criar um parâmetro? 
 Clique com botão direito no campo de interesse > Criar > Parâmetro 

## Vamos praticar!
Vamos criar 3 Planilhas para criação do Painel e/ou História

### Total de pedidos
1° Vamos criar a nossa primeira planilha e renomear como *Total de pedidos*

2° Vamos arrastar o campo `Order Id` para a métrica Linhas

3° Clique com o botão direito em `Order id` que está localizado em Linhas, vá em Medidas > Contagem distinta

4° Vá em `Mostra-me` e clique na opção de vizualização `Recomendação`

Agora vamos formatar o título:

5° Vamos mudar o título, clique na setinha no `título > editar título`
Observação: recomenda-se usar **fonte Arial** e **tamanho 12** e podemos deixar em negrito

Ajustando o espaçamento: 

6° No painel superior vamos em `ajustar>ajustar largura`

7° Clique com o botão direito na quantidade de total de pedidos. Em seguida, `formatar planilha > Fontes > Painel >Alinhar à esquerda`

### Evolução Anual 
1° Vamos criar a nossa segunda planilha chamada *Evolução Anual*

2° Vamos arrastar `Order Id` vai para `linha`, clicando com o botão direito vamos mudar para `contagem distinta` que está localizada em Medida

3° O campo `Reference Month` vai para colunas

4° No painel superior vamos clicar no símbolo quadrado chamado `Ajustar > Ajustar largura`

5° Vamos renomear o título para *Evolução anual de vendas* (clicando na setinha ao lado do título)

- Aumentando o tamanho da linha: 

6° Vá em no painel `Marcas` e clique em `Tamanho` e faça o ajuste

- Inserindo o rótulo no gráfico: 

7° Arraste o campo `Order Id` para `Rótulo` que está no painel `Marcas`

8° Com o campo `Order Id` no painel, clique com o `botão direito`, clique em `Medida` e mude para a opção `Contagem (distinta)`

- Tirando o cabeçalho
- 
9° Vamos ocultar o cabeçalho *Reference mouth*, com o botão direito clique no cabeçalho e selecione `Ocultar rótulos de campo para colunas`

10° Ocultando eixo *Contagem distinta de Order Id*, clique com o botão direito no cabeçalho, `desmarque` a opção `Mostrar Cabeçalho`. Não precisamos do eixo aparecendo já que os rótulos estão mostrando o valor

- Tirando as linhas de grade no fundo:

Clique com o botão direito> Formatar planilha > Linhas > Linha de grade > Vá em todos e clique em desativado

- Tirando o fundo branco:
Desativar o fundo branco é fundamental para casos que existam background pronto a ser aplicado no Tableau, esses background podem ser feitos em ferramentas como o Figma que são ferramentas de prototipação. Exemplo: você organizar o dashboard antes no Figma e depois passa para o Tableau. Nesses casos é necessário tirar o fundo branco e como podemos fazer isso? 

Vá em `Formatar planilha > Sombreamento> Planilha> Nenhuma` 

Não vamos ver na hora, mas quando passarmos a planilha para outro background com fundo de outra cor vamos perceber que o fundo branco sumiu.

- Formatando a fonte do rótulo do gráfico:

Botão direito > Formatar planilha > Arial > Negrito

- Formatação de números grandes:

No painel `Marcas` clique com o botão direito em CONTD(Order Id) e clique em `Formatar Número> Moeda personaliza`
Porque às vezes podemos ter número que precisam dessa formatação para não dificultar a leitura.

- Formatando a planilha de trabalho inteira:
No painel superior vá em Formatar > Planilha > escolha as opção de formatação

Se quiser mudar a cor é só clicar em `Cor` no painel `Marcas`

- Classificação Estado

1° Vamos criar a nossa terceira planilha chamada *Classificação Estado*

Para criar uma classificação de estado, um Ranking, vamos precisar criar um campo calculado:

2° Para criar um campo calculado vá em `Análise > Criar campo calculado`

3° Vamos nomear esse campo como *Classificação* 

4° Vamos utilizar a seguinte função: `RANK(SUM([Price]))`

- Criando a tabela de classificação:

1° Arraste o campo calculado `Classificação` para `linhas`, mude para `discreto`

2° O campo `Estado` vai para linhas

3° *Costumer Id* para Texto no painel de Marcas, mude para contagem distinta

4° Arraste o campo `Classificação` para para filtros, e insira a quantidade máxima que pretende classificar. Exemplo: 10. Vão aparecer os 10 estado que mais tiveram pedidos.Para mudar ranking vá em `filtro > editar filtro > digite o numero que deseja> aplicar > ok`

5° No campo `Classificação` que está em linha `clique com o botão direito > Calcular usando >Tabela Abaixo`


- Deixando o formato na tabela com °

Na métrica *Linhas* clique com o botão direito em `Classificação`, em seguida em Formatar Número > Número personalizado> em casa decimais você deixa no 0 e no sufixo você coloca o ° (simbolo grau)



---

Terminou o exercício? Dá uma olhada nessa checklist e confere se tá tudo certinho, combinado?!

- [ ] Fiz o fork do repositório.
- [ ] Clonei o fork na minha máquina (`git clone url-do-meu-fork`).
- [ ] Resolvi o exercício.
- [ ] Adicionei as mudanças. (`git add .` para adicionar todos os arquivos, ou `git add nome_do_arquivo` para adicionar um arquivo específico)
- [ ] Commitei a cada mudança significativa ou na finalização do exercício (`git commit -m "Mensagem do commit"`)
- [ ] Pushei os commits na minha branch (`git push origin nome-da-branch`)
