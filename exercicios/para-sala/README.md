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



---

Terminou o exercício? Dá uma olhada nessa checklist e confere se tá tudo certinho, combinado?!

- [ ] Fiz o fork do repositório.
- [ ] Clonei o fork na minha máquina (`git clone url-do-meu-fork`).
- [ ] Resolvi o exercício.
- [ ] Adicionei as mudanças. (`git add .` para adicionar todos os arquivos, ou `git add nome_do_arquivo` para adicionar um arquivo específico)
- [ ] Commitei a cada mudança significativa ou na finalização do exercício (`git commit -m "Mensagem do commit"`)
- [ ] Pushei os commits na minha branch (`git push origin nome-da-branch`)
