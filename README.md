# Mesa 4x - Teste Técnico Frontend

Este projeto consiste na implementação de dois cenários distintos para avaliar domínio em *HTML/CSS*:
- *Email Marketing em HTML* - considerando as limitações dos clientes, compatibilidade, responsividade e suporte a dark mode.
- *Landing Page* - página estática, responsiva, acessível e sem uso de JavaScript ou frameworks.

O objetivo é demonstrar código limpo, organizado, compatível e com atenção aos detalhes do mundo real.

---

# Parte 1 - Email Marketing (Desafio Técnico) 

## Conteúdo

- Headline: "Seu marketing não precisa ser um tiro no escuro."
- Subheadline: "Em 2 dias, você sai com um plano executável para gerar demanda, converter e acompanhar números."
- CTA principal e secundário
- Seção de Benefícios
- Prova Social
- Agenda
- Footer com endereço fictício e links placeholder

---

## Como rodar localmente

1. Baixe o arquivo `index.html` da pasta `email`
2. Abra diretamente no seu navegador (Chrome, Edge ou Safari)
3. Para testar o dark mode: 
    - Ative o modo escuro nas configurações de seu sistema operacional;
    - Ou utilize o Inspecionar Elementos para simular `prefers-color-scheme`

## Decisões Técnicas

### Layout baseado em tabelas
- Uso de `table-based layout` para compatibilidade com Gmail, Outlook, Apple Mail e apps mobile.  
- Garantia de fallback visual para clientes que ignoram CSS externo ou `<style>`.

### Container fixo de 600px
- Largura fixa de 600px, padrão do mercado;  
- `max-width` e media query simples aplicados para garantir legibilidade em mobile.

### CSS Inline
- CSS principal inline para compatibilidade máxima;  
- `<style>` mínimo usado para reset, media query mobile e dark mode;  
- Dark mode aplicado com consistência, evitando detalhes excessivos.  

### Botões
- CTAs implementados com tabela, `<td bgcolor>` e `<a>` estilizado;  
- Estratégia "bulletproof" garante funcionamento em todos os clientes de email.

### Considerações
- Imagem com atributo `alt` presente;
- Uso de `role="presentation"` quando aplicável;  

---

# Mesa 4x - Landing Page (Desafio Técnico)

## Conteúdo

### Hero 
    - Headline + subheadline
    - CTA 
    - Elemento visual (mockup)

### Como funciona
    - Grid com 3 passos
    - Ícones visuais (Emoji)

### Planos/Ingressos
    - 3 Cards (Classic, VIP, Camarote)
    - Destaque visual no plano recomendado
    - CTA por card, com destaque no plano recomendado

## Como rodar localmente

- Baixe os arquivos `index.html` e `styles.css` da pasta `lp`
- Abra o `index.html` no navegador
- Para testar mobile:
    - Reduza a largura da janela do navegador
    - Ou utilize Inspecionar Elementos para simular o dispositivo móvel

## Decisões Técnicas

### HTML Semântico

A página foi construída utilizando:

- `header` para seção Hero
- `main` para o conteúdo principal
- `section` para o conteúdo de "Como Funciona" e "Planos"
- `article` para cada card de Plano
- Hierarquia de headings (`h1`, `h2`, `h3`) respeitada para SEO e acessibilidade.

### CSS Modularizado
- Arquivo `styles.css` separado
- Mobile-first: estilos básicos aplicados para dispositivos menores e media queries para telas maiores

### Acessibilidade
- Contraste de cores adequado para os cards, seções e CTA
- Foco nos links e botões (`focus`)
- Utilização de `aria-label`
- Elementos interativos semanticamente corretos, tendo `a` com href

# Observações Finais

Não foi utilizada nenhuma linguagem de programação ou framework no desenvolvimento do teste, garantindo e respeitando a compatibilidade e performance. A criação do layout responsivo buscou focar na acessibilidade, experiência do usuário.

# O que eu faria diferente com mais tempo?

Eu construiria as seções com mais conteúdo, sem fugir do escopo do projeto, e utilizaria alguma linguagem de programação, como JavaScript, para funcionalidades extras.