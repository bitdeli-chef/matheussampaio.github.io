---
layout: post
title: 2º Hackfest Analytics
categories: []
tags: [programacao ufcg]
published: True

---

No final de janeiro eu participei do [2º Hackfest Analytics][1] promovido pelo [Laboratório Analytics][2], onde me reuni com vários outros alunos e alguns professores para passar o final de semana desenvolvendo as ideias que bolamos no primeiro dia do hackfest.

A ideia que ajudei a desenvolver era analisar os tweets do ano de 2014 sobre as bandas finalistas do programa de TV [Superstars][3] (Malta, Jamz, Suricato e Luan Estilizado) e tentar descobrir alguma relação entre a quantidade de tweets e a colocação final do programa.

Nossa primeira tarefa, era recuperar e armazenar todos os tweets sobre os artistas no ano de 2014. Já estavamos ciente da limitação da API do Twitter: só poderiamos recuperar 450 tweets a cada 15 minutos, então planejamos em usar vários tokens para acelerarmos o processo.

Depois de algum tempo investido e quase tudo pronto pra começar a coleta dos dados, descobrimos o maior problema que tivemos durante o hackfest: a API do Twitter só libera os tweets dos ultimos 7 dias. Perdemos algum tempo resolvendo outro meio de recuperar os dados, mas por fim descobrimos que o twitter não limita a quantidade de tweets que podem aparecer em sua [pesquisa][5], então com a ajuda de [jsoup][6] e um pouco de paciencia para carregar uma boa quantidade de tweets, consiguimos todos os tweets que precisavamos.

Começamos então a estudar os dados e pensar em boas visualizações.

Começamos então a preparar as visualizações que seriam utilizadas no nosso site final
![Análise Temporal de Popularidade]({{ site.url }}/assets/tweets-all-bands.png)


[1]: https://www.facebook.com/media/set/?set=a.898644253501560.1073741834.825911050774881&type=1&ref=notif&notif_t=like
[2]: https://www.facebook.com/analytics.ufcg?fref=photo
[3]: superstars
[4]: https://github.com/geoffjentry/twitteR
[5]: https://twitter.com/search
[6]: http://jsoup.org/