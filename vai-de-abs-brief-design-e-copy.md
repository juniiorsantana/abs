# Vai de ABS — Briefing de Design e Copy do Site

> Documento de referência para gerar o site no Google Stitch. Contém a direção visual recomendada e o texto completo de cada seção, pronto para uso.

---

## 1. Contexto rápido

- **Marca:** Vai de ABS — moto táxi via app em Cáceres, MT.
- **Diferencial real:** preço visível antes de confirmar, rastreio da moto chegando, pagamento sem dinheiro em espécie. A concorrência (moto-taxi tradicional) opera só por telefone/WhatsApp, sem nenhuma dessas garantias.
- **Objetivo do site:** ser a primeira presença digital de autoridade no mercado de moto-taxi de Cáceres — hoje não existe nenhuma. Precisa parecer um produto sério, não uma página improvisada.
- **Dois públicos no mesmo site:** passageiro (pede corrida) e motoboy (quer rodar com o app).

---

## 2. Conceito-âncora

ABS é, literalmente, o sistema de freio antiderrapante da moto — controle e precisão mesmo em alta velocidade. Essa ideia guia a direção visual: o site deve parecer **preciso, confiável e no controle**, não "moderno" por estética vazia.

---

## 3. Direção visual recomendada

### Paleta de cores

| Uso | Cor | Hex |
|---|---|---|
| Fundo base | Preto quase-asfalto | `#0B0B0C` |
| Acento / CTA / destaque | Amarelo elétrico | `#F4C20D` |
| Texto principal | Branco-gelo | `#F2F0EA` |
| Cards / divisores / superfícies | Cinza-grafite | `#2A2A2C` |
| Texto secundário / legendas | Cinza médio | `#8A8A8E` |

Amarelo é usado **só como acento** — linhas finas, botões, números, ícones. Nunca como bloco grande de fundo; isso pesa demais visualmente e foge da ideia de "instrumento de precisão".

### Tipografia

- **Display (headlines):** Space Grotesk, peso Bold/Black — geométrica, com personalidade técnica, sem ser fria.
- **Corpo de texto:** Inter, peso Regular/Medium — leitura limpa em qualquer tamanho de tela.
- **Números e dados (preço, percentual, contadores):** JetBrains Mono — números em monoespaçada parecem dado real, não enfeite de marketing. Usar especificamente em: "R$10", "90%", contadores animados.

### Layout

- Grid rígido, full-bleed (seções ocupam a largura inteira da tela).
- Linhas finas em amarelo dividindo seções, como um painel/velocímetro — não usar divisores grossos ou decorativos.
- Preço e percentual aparecem grandes e isolados, como uma leitura de painel, não escondidos em parágrafo.
- Fotos reais de Cáceres e de motoboy rodando à noite (nunca banco de imagem genérico) — com grading escuro/contrastado que combina com a paleta.

### Animação / motion

- Números (90%, R$10) sobem contando quando entram na tela ao rolar.
- Linha fina amarela acompanha o scroll, ligando uma seção à outra.
- Hover em botões: glow amarelo sutil, como luz de painel acendendo.
- Na seção "Como funciona": um ponto se move sozinho sobre um mapa simplificado, mostrando o rastreio em ação — o produto se demonstrando, não apenas descrito.
- **Sem vídeo em loop pesado no hero** — usar CSS/animação leve. Boa parte do público acessa por 4G em cidade do interior; o site precisa carregar rápido.
- Respeitar `prefers-reduced-motion` — desativar animações para quem tem essa preferência ativada no dispositivo.

### Elemento de assinatura

No ponto final de "Vai de ABS." pulsa um amarelo discreto, como um LED de painel. É o único elemento "vivo" do logotipo — todo o resto do site é disciplinado em volta dele.

---

## 4. Estrutura do site (sitemap)

Página única (landing page) dividida em 5 blocos, pensada para depois virar páginas separadas sem precisar refazer do zero:

1. Home / Hero
2. Como funciona
3. Seja motoboy
4. Preços
5. Sobre / Contato

---

## 5. Copy completo, seção por seção

### Hero

**Headline:**
Vai de ABS.

**Subheadline:**
A forma mais moderna de se mover em Cáceres. Você vê o preço antes de confirmar, acompanha a moto chegando e paga sem precisar ter dinheiro na mão.

**Botões:**
- Pedir uma corrida
- Quero ser motoboy ABS

**Legenda pequena abaixo dos botões:**
Feito em Cáceres, pra Cáceres.

---

### Como funciona

**Título da seção:**
Sem ligação. Sem esperar no escuro.

**Passos (numerados, é uma sequência real):**
1. Peça e diga onde você está.
2. Veja o preço antes de confirmar — sem surpresa, sem negociar.
3. Acompanhe a moto chegando até você.
4. Pague sem precisar ter dinheiro na hora.

**Frase de fechamento:**
Você sabe exatamente o que vai pagar e quando a moto chega. Simples assim.

---

### Seja motoboy

**Título da seção:**
Motoboy em Cáceres? O cliente vem até você.

**Texto de apoio:**
Cansou de ficar parado no ponto esperando passageiro? O ABS te avisa quando tem corrida por perto — você não precisa correr atrás de cliente.

**Lista de benefícios:**
- Você fica com 90% de cada corrida (o mercado costuma ficar entre 75% e 85%)
- Você escolhe seu horário, sem patrão
- Renda extra ou principal — você decide

**Botão:**
Quero rodar com o ABS

---

### Preços

**Título da seção:**
Preço claro, sem letra pequena.

**Texto principal:**
Piso de R$10 por corrida. Você vê o valor exato antes de confirmar — nunca depois.

**Frase de apoio:**
Sem depender de quanto o motoboy "sente" que deve cobrar naquele dia.

---

### Sobre / Contato

**Título da seção:**
Feito pra Cáceres.

**Texto principal:**
O Vai de ABS é operado por gente daqui, com licença exclusiva pra rodar moto na cidade. Criado pra resolver um problema que cacerense vive todo dia: pedir uma moto sem depender só de sorte.

**Contato:**
- WhatsApp: (XX) XXXXX-XXXX
- Instagram: @abscaceres
- Hashtags: #VaiDeABS #ABSCaceres

---

### Rodapé

**Vai de ABS.**

---

## 6. Notas técnicas para a implementação

- Mobile-first: a maioria do tráfego vem de celular, com conexão variável.
- Performance acima de efeito: priorizar CSS/animações leves sobre vídeo ou imagens pesadas.
- Acessibilidade: contraste alto entre preto e branco-gelo já ajuda; cuidado para nunca colocar texto amarelo sobre fundo claro (baixo contraste).
- Os campos de telefone/Instagram no "Sobre/Contato" estão como placeholder — substituir pelos dados reais antes de publicar.
