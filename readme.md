# ☕ Grão & Arte - Torrefação e Café Especial

## 1. Visão Geral e Objetivo do Projeto

O projeto **Grão & Arte** é uma aplicação web front-end desenvolvida como parte da avaliação prática do curso (Turma A), simulando um ambiente profissional de desenvolvimento para um cliente fictício do segmento de torrefação artesanal de cafés especiais.

O objetivo principal é construir uma *landing page* moderna, acessível, semântica e totalmente responsiva. A página atua como vitrine digital da marca, apresentando o catálogo de microlotes exclusivos (grãos 100% Arábica com pontuação SCA > 85), o processo artesanal de torra, os planos do clube de assinatura mensal, uma seção de dúvidas frequentes (FAQ) e um canal de contato direto via WhatsApp.

---

## 2. Tecnologias e Conceitos Aplicados

### Tecnologias
* **HTML5 Semântico:** Estruturação da página focada em acessibilidade e SEO, utilizando tags semânticas (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<details>`, `<summary>`, `<footer>`).
* **CSS3 Moderno:** Estilização sem a utilização de estilos inline ou blocos embutidos no HTML, garantindo total separação de responsabilidades.
* **Google Fonts:** Importação das famílias tipográficas oficiais do projeto: *Merriweather* (pesos 400 e 700) e *Open Sans* (pesos 400, 600 e 700).
* **API do WhatsApp:** Integração de link interativo para atendimento direto com o número oficial da Escola SENAI Henrique Lupo.

### Conceitos e Metodologias
* **Metodologia BEM (Block Element Modifier):** Convenção rigorosa de nomenclatura de classes no HTML e seletores no CSS (`bloco__elemento--modificador`), garantindo modularidade e reuso do código.
* **Design System & Variáveis CSS (`:root`):** Centralização de tokens visuais como cores, fontes, bordas, sombras e transições no topo da camada de estilo.
* **Escala Tipográfica & Unidades Relativas (`rem`):** Definição da escala base no elemento raiz (`html`) e resgate da dimensão no `body`, aplicando `rem` em todas as tipografias, espaçamentos e bordas.
* **Layout Fluido & Responsividade:** Utilização de porcentagem (`%`) para dimensões de containers flexíveis com Flexbox, unidades de tela cheia (`vh`/`vw`) para seções principais e *breakpoints* ajustados para smartphones, tablets e desktops.
* **Navegação Suave e Recuo do Header Fixo:** Aplicação de `scroll-behavior: smooth` acompanhada de compensação de altura para evitar que o menu fixo sobreponha os títulos das seções.
* **Microinterações:** Efeitos visuais em pseudo-classes (`:hover`) com transições e sombras suaves para os cards e links de navegação.

---

## 3. Organização da Arquitetura de Arquivos Adotada

A estrutura de arquivos do repositório foi organizada para garantir a separação de responsabilidades e facilitar a manutenção do código:

```
grao-e-arte/
├── assets/
│   ├── css/
│   │   ├── variables.css      # Tokens globais do Design System (:root)
│   │   ├── reset.css          # Reset CSS e configuração da escala base (html/body em REM)
│   │   ├── components.css     # Estilos dos componentes estruturados com BEM
│   │   └── main.css           # Arquivo principal que unifica e importa o CSS
│   └── images/                # Imagens e recursos visuais do projeto
├── index.html                 # Estrutura HTML5 da landing page
└── README.md                  # Documentação oficial do repositório
```

---

## 4. Instruções de Visualização/Execução

Para visualizar e testar o projeto localmente, siga as instruções abaixo:

1. **Clonar o repositório do GitHub:**
   ```bash
   git clone https://github.com/SEU-USUARIO/grao-e-arte.git
   ```

2. **Acessar a pasta do projeto:**
   ```bash
   cd grao-e-arte
   ```

3. **Executar a aplicação:**
   * **Opção 1 (Direta):** Abra o arquivo `index.html` em qualquer navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge ou Safari).
   * **Opção 2 (Servidor Local):** Se estiver utilizando o VS Code, abra o diretório e inicie o arquivo via extensão **Live Server** (`http://127.0.0.1:5500`).

---

## 5. Principais Desafios Técnicos e Aprendizados

* **Compensação da Navbar Fixa no Scroll:** Um dos principais aprendizados foi implementar a navegação suave por âncoras sem que o cabeçalho fixo (`position: fixed`) cobrisse os títulos das seções. A solução foi resolvida com o uso de `scroll-margin-top` nas seções de destino.
* **Padronização com a Metodologia BEM:** Manter a consistência na nomenclatura de classes no HTML sem reutilizar nomes genéricos ou cair em acoplamento exigiu disciplina e planejamento estrutural.
* **Dimensionamento Fluido com Escala REM:** Ajustar o layout sem recorrer a valores fixos em pixels (restritos apenas a bordas finas) exigiu um alinhamento preciso entre porcentagens, unidades de viewport (`vh`/`vw`) e a escala relativa `rem`.
* **Uso Semântico de FAQ sem JavaScript:** Estruturar o FAQ utilizando apenas as tags nativas `<details>` e `<summary>` permitiu criar um componente retrátil e interativo focado em acessibilidade sem necessidade de scripts externos.

---
© 2026 **Grão & Arte**. Todos os direitos reservados.