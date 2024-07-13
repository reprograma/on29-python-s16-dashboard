# Exercício de Sala 🏫  

## Nome do Exercicio

## Evoluindo nosso dashboard

Para esse tutorial continuaremos a usar a base de dados do arquivo `base_final_s14_olist.csv` disponibilizada na pasta de [material](https://github.com/reprograma/on29-python-s16-dashboard/tree/main/material) 
___________________________

Primeiro, faça uma nova publicação do dashboard desenvolvido na semana 15 por você *ou* faça uma cópia do dashboard disponibilizado pela Professora Mariana.
https://public.tableau.com/app/profile/gabriela.nunes.turquetti/viz/S15-Reprograma-VisualizaodeDados/VisoGeral#1 

![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/exercicio-sala-1a-nova-publicacao-dashboard.png "Figura 1a")
![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/exercicio-sala-1a-popup.png "Figura 1a - Popup")
*Figura 1a: Instruções de como fazer uma nova publicação de um dashboard seu. Com o seu dashboard aberto já em edição, clique no menu "Arquivo" e selecione "Publicar como", ou use o atalho Ctrl+Shift+S, aparecerá uma janela onde você deve digitar o nome a sua escolha e clicar "Publicar"*

![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/exercicio-sala-1b-fazer-copia-dashboard.png "Figura 1b")
*Figura 1b: Instruções de como fazer uma cópia de um dashboard. Clique no ícone "Fazer uma cópia" na visualização de dados modelo*

Assim seguiremos aprofundando nossa análise.
___________________________

## Parte 1 - Análise de tempo de entrega usando gráfico boxplot

Vamos primeiramente criar uma nova planilha.
![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/exercicio-sala-2-nova-planilha.png "Figura 2")
*Figura 2: Instruções de como fazer uma nova planilha. Clique no ícone "Nova planilha", ou use o atalho Ctrl+Alt+T, na parte inferior da tela. Renomeie essa nova planilha clicando com o botão direito e selecionando a opção renomear, ou dê duplo clique, dê o novo nome desejado.*

Criaremos um **novo campo calculado**, chamado **Tempo de Entrega**, que retornará em **dias**, o tempo levado entre o pedido do cliente e a entrega. Para isso usaremos a seguinte função:
`DATEDIFF('day', [Order Purchase Timestamp], [Order Delivered Customer Date])`
> Você pode ver sobre as várias funções de datas disponíveis, além de outras, aqui: https://help.tableau.com/current/pro/desktop/pt-br/functions_functions_date.htm. 💡Lembre-se: a documentação é sempre sua melhor amiga. 
![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/exercicio-sala-3-campo-calculado.png "Figura 3")
*Figura 3: Instruções de como criar um campo calculado. No menu vá em "Análise" e clique em "Criar campo calculado...". Abrirá uma nova janela, renomeie o campo para **Tempo de Entrega**, construa a função de data conforme descrito ou copie do código exibido acima.*

Agora, arrastaremos a **métrica** "Tempo de Entrega" para o campo "Linhas" e a **dimensão** "Customer City" para o campo "Colunas"
![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/exercicio-sala-4-trazer-dados-para-a-visualizacao.png "Figura 4")
*Figura 4: Instruções visuais de quais dados arrastar e para onde.*

O Tableau automaticamente fez um gráfico de barras. E agregou o dado de Tempo de Entrega como soma. Vamos modificar.
![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/exercicio-sala-5-alterar-agregacao-e-tipo-grafico.png "Figura 5")
*Figura 5: Instruções de mudança de tipo de agregação. Clique em SOMA(Tempo de Entrega) em Linhas, vá para "Medida" e selecione a opção "Média".
Instruções de mudança de tipo de gráfico: Clique na opção "Mostre-me" no canto superior direito, e selecione a opção "gráfico de caixa" (também chamado de boxplot)*

Ficaremos com a visualização abaixo. Note que a dimensão "Customer City" foi para janela de "Marcas", sob "Detalhe". Agora arrastaremos "Customer State" para Colunas.
![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/exercicio-sala-6-arrastar-nova-coluna.png "Figura 6")
*Figura 6: Instruções visuais de qual dado arrastar.*

Por fim seu gráfico ficará semelhante à imagem abaixo. Agora brinque com sua nova visualização, alterne entre linhas e colunas,adicione filtros, explore. Quais insights podemos tirar dessa visualização?
![](https://raw.githubusercontent.com/reprograma/on29-python-s16-dashboard/main/assets/exercicio-sala-7-visualizacao-final-boxplot.png "Figura 7")
*Figura 6: Visualização de tempo de entrega com o gráfico de caixa.*






