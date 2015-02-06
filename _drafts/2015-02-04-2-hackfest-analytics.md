---
layout: post
title: 2º Hackfest Analytics
categories: []
tags: [programacao ufcg]
published: True

---

No final de janeiro eu participei do [2º Hackfest Analytics][1] promovido pelo [Laboratório Analytics][2], onde me reuni com vários outros alunos e alguns professores para passar o final de semana desenvolvendo as ideias que bolamos no primeiro dia do hackfest.

A ideia que ajudei a desenvolver era analisar os tweets do ano de 2014 sobre as bandas finalistas do programa de TV [Superstars][3] (Malta, Jamz, Suricato e Luan Estilizado) e tentar descobrir alguma relação entre a quantidade de tweets e a colocação final do programa.

Nossa primeira tarefa, era recuperar e armazenar todos os tweets sobre os artistas no ano de 2014. Para burlar a [limitação da API do Twitter][7] (só libera 450 tweets a cada 15 minutos), planejamos em utilizar vários tokens, uma para cada pessoa do hackfest, e fazer requests paralelos.

Depois de algum tempo investido e quase tudo pronto pra começar a coleta dos dados, descobrimos o maior problema que tivemos durante o hackfest: a API do Twitter só libera os tweets dos ultimos 7 dias. Perdemos algum tempo resolvendo outro meio de recuperar os dados, mas por fim descobrimos que o twitter não limita a quantidade de tweets que podem aparecer em sua [pesquisa][5], então com a ajuda de [jsoup][6] e um pouco de paciencia para carregar uma boa quantidade de tweets, consiguimos todos os tweets que precisavamos.

Então veio a parte mais interessante, analisar os dados! Assim que geramos um sumário dos dados, já poderiamos prever o campeão do programa. A popularidade da banda Malta em todos os momentos foi superior as demais.

O mais interessante era que a popularidade das demais bandas também casou com suas posições. Principalmente na ultima semana do programa.


Como é de se esperar, todas as bandas ganharam muita popularidade durante o programa da Globo, mesmo não tendo nenhuma atenção antes do inicio do programa. Por outro lado, no momento em que o programa acabou, todas as bandas perderam quase toda a atenção que vinham tendo no Twitter. A excessão é a banda Malta, que nas ultimas semanas do ano, voltou a ser comentada, mas atribuimos esse pico devido ao lançamento do seu CD pela Som Livre, como podem ver na imagem abaixo.

![Análise Temporal de Popularidade]({{ site.url }}/assets/tweets-all-bands.png)

É sempre muito bacana participar de eventos como esse. Aprendemos muito com a experiencia das outras pessoas e percebemos o quão rapido é produzir um protótipo de uma ideia em alguns dias. Talvez aquela sua ideia que está guardada a anos, possa ser feita em alguns dias e depois conseguir a atenção necessária para você emplaca-la de vez. (:

[1]: https://www.facebook.com/media/set/?set=a.898644253501560.1073741834.825911050774881&type=1&ref=notif&notif_t=like
[2]: https://www.facebook.com/analytics.ufcg?fref=photo
[3]: superstars
[4]: https://github.com/geoffjentry/twitteR
[5]: https://twitter.com/search
[6]: http://jsoup.org/
[7]: https://dev.twitter.com/rest/public/rate-limiting