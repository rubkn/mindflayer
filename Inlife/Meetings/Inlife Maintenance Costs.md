https://bt.appx.pt/view.php?id=2322
Ticket com algumas inconveniências. Particularmente 1h20 com explicações para comigo.
Explicações são essenciais, debate, brainstorming, faz parte do processo, ainda para mais tendo um colega novo. Mas deveria ser registado? Não creio. Também não sei se concordo muito em as reuniões serem todas declaradas aqui. 

https://bt.appx.pt/view.php?id=2463
Implementar NextJS é um processo demorado, sem dúvida, especialmente num processo já existente, mas como é que podemos ter a garantia que foram gastas 66h? 

https://bt.appx.pt/view.php?id=1693
Gosto da transparência ao escreverem tudo o que foi feito no código, mas isso acaba mais por ser para uso deles do que para a Inlife, que obviamente não vai perceber o que é por exemplo "Adicionado useHistory". Descrições deveriam ser mais diretas, e estes registos do que foi mudado, ficam para os developers, que também é fácil de consultar no histórico do Git. Não será também que este tempo todo que demoram a escrever estes comentários excessivo?

https://bt.appx.pt/view.php?id=1705
Limpeza de código deprecado poderia não ser um processo de 1 ticket só. Limpeza de código deveria acontecer em qualquer outro ticket quando nos deparamos com uma função que já não é utilizada por exemplo.

https://bt.appx.pt/view.php?id=2586
9 horas a resolver este issue parece-me excessivo, mas por um lado também não sei o que aconteceu, pode ter havido um bom tempo de debugging, ver onde estava o problema, etc.


Acho que o que há a reter aqui é que a comunicação deveria ser melhor. Antes de começar o trabalho, é importante definir expectativas claras com a Inlife sobre como o tempo gasto será gasto em certo issue. Isto vai ajudar a evitar mal-entendidos e garante que todos estão na mesma página. Creio que o melhor seria mover para um modelo de briefing e solução em vez de manutenção geral da plataforma. 

Sugiro a criação de ciclos de trabalho, que podem ir de 6 semanas a 8 ou 10 semanas, onde antes do ciclo começar, é feita uma análise completa da plataforma e do que é necessário mudar. Após isso, é criado o briefing. Estes ciclos serveriam também para a equipa de desenvolvimento estar mais focada numa específica implementação, pois a fase depois do ciclo acabar, que pode ser 1 semana ou 2 semanas é a fase de tratamento de bugs e issues que não estão associados a nada. Após isso, repete-se a mesma estrutura e é iniciado outro ciclo. 

O processo de criação de briefing de um projeto que vai depois fazer parte da implentação dentro de cada ciclo, é composto pelas seguintes partes. São elas:

1. ***Shaping:*** A fase de shaping envolve a identificação de uma oportunidade de projeto e a criação de um argumento de venda para esse mesmo projeto. Cada projeto pode conter várias implementações desde que todas elas vão de encontro a um fim comum. Este argumento de venda deve incluir uma declaração clara do problema, possíveis soluções e quaisquer restrições ou requisitos.
2. ***Betting:*** Nesta fase, o esse mesmo pitch que foi criado na fase de Shaping é apresentado à equipa de management, que decidirá se quer “apostar” no projeto. Se eles decidirem prosseguir, o projeto passa para a próxima fase.
3. **Planning:** Na fase de planeamento, um resumo do projeto é criado. O resumo deve fornecer uma visão geral de alto nível do projeto, incluindo o problema a ser resolvido, a solução proposta, o público-alvo e quaisquer restrições ou requisitos. Ele também deve incluir o âmbito do projeto, tempo que pode/irá ser gasto e orçamento.

*(todas estas fases são feitas internas na Inlife, e terão que passar sempre pelo product owner e product manager)*


As fases já de dentro do ciclo, onde começa o contacto com a AppX, podem ser algo assim:

1. **Planeamento:** Esta fase envolveria juntar toda a informação sobre o projeto, requisitos, âmbito, e objetivos. Isto obviamente inclui meetings Inlife - AppX onde se irão identificar possíveis roadblocks e desafios. No final desta fase, deverá estar acordada uma timeline e o plano de projeto.
2. **Design:** Nesta fase, o Miguel começará a trabalhar em desenhar o sistema necessário para a solução desejada. Isto inclui todos os wireframes no Figma e outras coisas que possam vir a ser necessárias.
3. **Development:** Uma vez finalizado o design, inicia-se a fase de desenvolvimento. Esta fase envolve a construção da solução no código, teste e debugging. No fim desta fase é deverá estar presente em staging a solução implementada.
4. **Testing and Quality Assurance:** Nesta fase, o projeto é testado para garantir que vai de encontro aos requisitos e funciona conforme esperado. Isso pode envolver testes automatizados ou testes manuais. Quaisquer problemas ou bugs identificados durante esta fase são resolvidos no mesmo ciclo.
5. **Deployment:** Estando todas as fases acima terminadas e de encontro com o briefing inicial, passamos à implementação no ambiente de produção. 