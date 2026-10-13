# Bússola Eleitoral

Um questionário de orientação política para Portugal, em ficheiro único, que funciona offline e não recolhe dados.

**Experimentar:** https://engjuliocez4r.github.io/bussola-eleitoral/

---

## O que é

Vinte afirmações sobre política portuguesa. O resultado coloca quem responde em seis temas — impostos, serviços públicos, valores sociais, imigração e segurança, sistema político, ambiente — e mostra que partidos ficam mais perto ou mais longe em cada um.

Não é uma recomendação de voto. É um ponto de partida para ler os programas.

## Porque existe

A maior parte das pessoas escolhe um partido primeiro e as opiniões depois. Esta ferramenta inverte a ordem: começa pelo que falta na vida de quem responde, e só no fim mostra onde isso cai no mapa político.

## Como é calculado

Cada resposta desloca quem responde num dos seis temas. Respostas marcadas como importantes pesam o dobro. "Não tenho opinião formada" não conta para nada.

Três decisões de desenho que valem mais do que o código:

**Cada afirmação declara o custo da escolha.** "Baixar o IRS mesmo que isso obrigue a cortar despesa do Estado." Sem o custo explícito, ninguém discorda de "menos impostos" e a pergunta não mede nada.

**Cada tema tem afirmações nos dois sentidos.** Em alguns itens concordar puxa para um lado, noutros puxa para o outro. Quem responde "concordo" a tudo termina no centro de todos os eixos, e não num extremo. É a proteção contra o viés de quem escreveu o teste, e não depende da boa-fé de ninguém: está no código e é verificável.

**Os dois sentidos são medidos em separado antes de serem combinados.** Sem isto, um tema com mais afirmações num sentido do que no outro enviesaria o resultado de quem responde sempre a mesma coisa. Ver `userAxes()` em `index.html`.

Nenhuma afirmação apresenta como facto algo que está em disputa política.

## Privacidade

Não há servidor, conta, cookies, analytics nem qualquer pedido de rede. As respostas são calculadas no navegador e desaparecem ao fechar a página.

**Verificação em cinco segundos:** desligue o wi-fi e faça o questionário à mesma. Funciona na íntegra. Uma página que funciona offline não tem para onde enviar nada.

## Posição dos partidos

O array `PARTIES` em `index.html` coloca nove partidos numa escala de −2 a +2 em cada um dos seis temas, a partir das posições que defendem publicamente.

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

Projeto feito por conta própria, sem encomenda nem financiamento de qualquer partido, candidatura ou campanha.
