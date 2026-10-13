# Bússola da Cidadania

Ferramenta de literacia cívica para Portugal. Ficheiro único, funciona offline, não recolhe qualquer dado.

**Experimentar:** https://engjuliocez4r.github.io/bussola-da-cidadania/

---

## O que é

Vinte afirmações sobre decisões públicas que afetam o dia a dia em Portugal. Cada uma descreve uma escolha real e declara o que ela custa, porque toda a decisão pública é uma troca.

O resultado situa quem responde em seis temas — impostos, serviços públicos, valores sociais, imigração e segurança, funcionamento das instituições, ambiente e território — e indica a proximidade face ao que é defendido por quem tem assento na Assembleia da República.

A segunda metade é um guia prático de participação: como apresentar um pedido a um órgão público, o que é o direito de petição, que número de subscritores produz que efeito, e como chegar aos órgãos do próprio concelho.

## Porque existe

A opinião sobre assuntos públicos costuma formar-se ao contrário: primeiro a pertença, depois as posições. Esta ferramenta inverte a ordem — parte da experiência concreta de quem responde e só no fim mostra onde isso se situa no mapa.

E não termina no diagnóstico. Saber onde se está serve de pouco a quem não sabe que pode escrever a um deputado ou a uma câmara municipal e obter resposta. A segunda metade existe para isso.

## O que este projeto resolve, em termos de engenharia

Um questionário que classifica posições é trivial de construir e muito fácil de enviesar. Os problemas tratados aqui:

- **Enviesamento pela formulação.** Cada afirmação declara o custo da escolha, para não existirem opções que ninguém recusaria.
- **Viés de aquiescência.** Quem responde sempre a mesma coisa tenderia a acumular num extremo. Resolvido com itens em sentidos opostos dentro de cada tema e com medição separada por sentido antes da combinação.
- **Confiança do utilizador.** Zero pedidos de rede, zero armazenamento, verificável por qualquer pessoa sem conhecimentos técnicos.
- **Distribuição.** Ficheiro único, sem dependências, sem build, sem instalação. Funciona aberto do disco.

## Como é calculado

Cada resposta desloca quem responde num dos seis temas. Respostas marcadas como importantes pesam o dobro. "Não tenho opinião formada" não conta para nada.

Três decisões de desenho que valem mais do que o código:

**Cada afirmação declara o custo da escolha.** "Baixar o IRS mesmo que isso obrigue a cortar despesa do Estado." Sem o custo explícito, ninguém discorda de "menos impostos" e a pergunta não mede nada.

**Cada tema tem afirmações nos dois sentidos.** Em alguns itens concordar puxa para um lado, noutros puxa para o outro. Quem responde "concordo" a tudo termina no centro de todos os eixos, e não num extremo. É a proteção contra o viés de quem escreveu o teste, e não depende da boa-fé de ninguém: está no código e é verificável.

**Os dois sentidos são medidos em separado antes de serem combinados.** Sem isto, um tema com mais afirmações num sentido do que no outro enviesaria o resultado de quem responde sempre a mesma coisa. Ver `userAxes()` em `index.html`.

Nenhuma afirmação apresenta como facto algo que está em disputa política.

## Privacidade

Não há servidor, conta, cookies, analytics nem qualquer pedido de rede. As respostas são calculadas no navegador e desaparecem ao fechar a página.

**Verificação em cinco segundos:** com a página já aberta, desligue a rede e faça o questionário até ao fim. Funciona na íntegra, porque depois de carregada a página não faz mais nenhum pedido. Em alternativa, descarregue `index.html` e abra-o sem rede nenhuma — dá o mesmo resultado.

Quem quiser confirmar ao detalhe: abra as ferramentas de programador do navegador, separador *Network*, e verá que durante todo o questionário não sai um único pedido.

## Posicionamento

O array `PARTIES` em `index.html` situa as nove forças com representação parlamentar numa escala de −2 a +2 em cada um dos seis temas, a partir das posições que defendem publicamente.

Esta é a parte discutível do projeto, e está isolada de propósito. Se discorda de um posicionamento, abra uma *issue* com o partido, o tema e a referência — programa eleitoral, declaração pública ou sentido de voto no Parlamento. Correções fundamentadas são bem-vindas e ficam registadas no histórico do repositório.

As posições são uma síntese e desatualizam-se. Última revisão: outubro de 2026.

## Limites

- Seis temas não esgotam a política.
- A ferramenta não mede competência, honestidade nem capacidade de governar, que talvez sejam o que mais importa.
- A ordem e a forma das afirmações influenciam sempre alguma coisa, por mais cuidado que se tenha.

## Correr localmente

Não é preciso instalar nada. Descarregue `index.html` e abra-o no navegador.

## Publicar uma cópia

Faça *fork*, vá a **Settings → Pages**, escolha *Deploy from a branch*, ramo `main`, pasta `/ (root)`.

## Licença

MIT. Ver `LICENSE`.

## Autor

Julio Lacerda (Eng. de Software - CREA-PA/BR), mestrando em Engenharia Informática no ISCTE-IUL.

Projeto pessoal, feito por conta própria, sem encomenda nem financiamento de qualquer partido, candidatura, campanha ou organização.
