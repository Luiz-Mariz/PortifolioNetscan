# 🏢 Netscan 

Este repositório contém o código-fonte para a Landing Page (Página Inicial) da Netscan, uma empresa especializada em telecomunicação, segurança e automação para condomínios e empreendimentos inteligentes.

O projeto utiliza **HTML5** para a estrutura semântica e **CSS3** para o design responsivo, seguindo uma paleta de cores institucional.

## 📁 Estrutura do Projeto

O código é dividido em dois arquivos principais:

| Arquivo | Função |
| :--- | :--- |
| `index.html` | Estrutura principal da página, conteúdo textual e links para as seções. |
| `style.css` | Estilização, layout responsivo e definição das variáveis de cores. |

**Dependências Externas:**
* **Font-Awesome 6:** Utilizado para os ícones de serviços e CTAs.
* **Google Fonts:** Fonte 'Roboto' com diversos pesos para tipografia.

## 🎨 Paleta de Cores (Variáveis CSS)

O arquivo `style.css` utiliza variáveis CSS (`:root`) para definir a paleta de cores, garantindo consistência e facilidade em futuras alterações de marca.

| Variável | Valor | Descrição |
| :--- | :--- | :--- |
| `--net-blue` | `#004AAD` | **Azul Principal** (Botões e Destaques) |
| `--net-blue-dark` | `#003380` | Azul Escuro (Títulos e Hover) |
| `--net-dark` | `#1A1A1A` | Preto/Texto Principal e Fundo do Footer |
| `--net-white` | `#FFFFFF` | Branco |
| `--net-bg-light` | `#F0F5F9` | Fundo Secundário (Seção Hero e Cards) |
| `--maxw` | `1200px` | Largura máxima do conteúdo (`.container`) |

## 🧩 Visão Geral da Estrutura HTML

A página é construída em seções semânticas (tags `<section>`) para modularizar o conteúdo e facilitar a navegação (scroll) e manutenção.

| Classe CSS | Descrição |
| :--- | :--- |
| **`.hero-section`** | Banner principal e proposta de valor. Contém o `<h1>` e o CTA principal. |
| **`.products-section`** | Cards de destaque (`.product-card`) com as 3 principais soluções. |
| **`.photo-text-section`** | Blocos de conteúdo com imagem e texto que se alternam (efeito "zigzag" ou "Checkerboard"). |
| **`.services-list-section`** | Grade (`.cards-grid-wrapper`) de todos os serviços oferecidos. |
| **`.contact-footer`** | Rodapé com perfil do Responsável Técnico (RT) e informações de contato. |

---

## ⚙️ Classes e Componentes Reutilizáveis

### Botões (CTAs)

| Classe | Descrição |
| :--- | :--- |
| **`.btn-primary`** | Botão de destaque (azul) com sombra e efeito `hover` de leve elevação. |
| **`.btn-secondary`** | Botão auxiliar, usado no footer (fundo branco, texto azul). |

### Containers e Responsividade

| Classe | Descrição |
| :--- | :--- |
| **`.container`** | Centraliza o conteúdo, aplicando o `max-width` (`1200px`) e padding lateral. |
| **`.section-heading`** | Títulos principais (`<h2>`) das seções (negrito, cor escura, centralizado). |
| **`.section-subheading`** | Descrição curta sob o título da seção. |

### Layout de Conteúdo

* **`.content-block`**: Utilizado na seção `photo-text-section`. Define um layout flexível com dois blocos: `.text-content` e `.image-placeholder`.
* **Alternância de Ordem**: O seletor `:nth-child(even)` inverte a ordem dos blocos pares (`flex-direction: row-reverse;`), criando o layout em zigue-zague para melhor fluxo visual.
* **`.cards-grid-wrapper`**: Utiliza **CSS Grid** para exibir a lista de serviços em **3 colunas** por padrão (desktop), caindo para 2 colunas (tablet) e 1 coluna (mobile), garantindo responsividade total.

---

## 📱 Responsividade (Media Queries)

O design da página é totalmente responsivo, adaptando-se a diferentes tamanhos de tela. As principais quebras (breakpoints) usadas no `style.css` são:

| Tamanho da Tela | Ajustes Principais |
| :--- | :--- |
| **`@media (max-width: 1024px)`** | Grade de serviços muda para **2 colunas**. |
| **`@media (max-width: 900px)`** | Blocos de Foto/Texto (`.content-block`) empilham-se (coluna) e o título `<h1>` é reduzido. |
| **`@media (max-width: 768px)`** | Grade de serviços muda para **1 coluna**. |
| **`@media (max-width: 500px)`** | Redução da fonte do `<h1>` e dos botões para otimizar a visualização em smartphones. |

## 🔗 Próximos Passos e Otimizações

* **Otimização de Imagens:** Substituir os placeholders (`.jfif`) por imagens otimizadas em formatos modernos (ex: WebP).
* **Melhoria de Performance:** Carregamento assíncrono (ou `defer`) para o Font Awesome ou otimização do CSS de terceiros.
* **Link RT:** Atualizar o `href="URL_DO_PERFIL"` no footer com o link real do Responsável Técnico.
