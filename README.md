# ⚽ Sorteio de Times

Sistema simples e gratuito para sortear times de futebol equilibrados, feito para o **Clube Monte Líbano — Nosso Racha (10 anos)**.

Cadastre os jogadores com nome, posição e nível, e o sistema monta dois times balanceados por posição e nível de habilidade — sem precisar de servidor, banco de dados ou instalação.

## ✨ Funcionalidades

- Cadastro de jogadores com **nome**, **posição** (Goleiro, Zagueiro, Lateral, Meio-campo, Atacante) e **nível** (0 a 1)
- Composição fixa: **2 goleiros + 14 jogadores de linha** (8 por time)
- Sorteio automático que equilibra:
  - a quantidade de jogadores por posição em cada time
  - o nível médio somado entre os dois times
- Barra visual comparando o equilíbrio entre os times
- Botão para **reembaralhar** o sorteio (empates usam aleatoriedade, então cada sorteio pode variar mantendo o equilíbrio)
- **Envio direto para o WhatsApp**: gera a escalação formatada e abre o WhatsApp para você escolher o grupo do futebol
- **Dados salvos no navegador** (`localStorage`): a lista de jogadores e o último sorteio continuam lá mesmo se você fechar a aba
- 100% front-end — não depende de internet além de carregar a página (funciona até offline, exceto a fonte do Google Fonts)

## 🖥️ Como usar

1. Abra o arquivo `sorteio-times.html` no navegador (ou acesse o link publicado, veja abaixo). Será excluído em breve, e estará no lugar o index.html. Também está disponível na Vercel - https://escalacao-racha.vercel.app
2. Cadastre os 16 jogadores (2 goleiros + 14 de linha)
3. Clique em **"Sortear times"**
4. Se quiser, clique em **"Enviar para o WhatsApp"** para compartilhar a escalação com o grupo
5. Use **"Limpar tudo"** para começar um novo sorteio do zero

## 📁 Arquivos do projeto

| Arquivo | Descrição |
|---|---|
| `sorteio-times.html` | Aplicação completa (HTML + CSS + JS em um único arquivo) |
| `logo-nosso-racha.png` | Logo exibido no topo do sistema e como favicon |

> ⚠️ Os dois arquivos precisam estar na **mesma pasta** — o HTML referencia o logo pelo caminho relativo `logo-nosso-racha.png`.

## 🌐 Como publicar gratuitamente (GitHub Pages)

1. Vá em **Settings → Pages** neste repositório
2. Em "Source", selecione a branch `main` e a pasta `/root`
3. Salve — em alguns minutos o link fica disponível em:
   ```
   https://<seu-usuario>.github.io/<nome-do-repositorio>/sorteio-times.html
   ```

## 🔧 Tecnologias

- HTML5, CSS3 e JavaScript puro (vanilla) — sem frameworks, sem build, sem dependências de backend
- `localStorage` para persistência local dos dados
- Fonte via Google Fonts (Bebas Neue, Inter, JetBrains Mono)

## ⚙️ Como funciona o algoritmo de sorteio

1. Os **2 goleiros** são distribuídos, um para cada time
2. Para cada posição de linha (Zagueiro → Lateral → Meio-campo → Atacante), os jogadores são ordenados por nível e distribuídos priorizando:
   - manter a mesma quantidade daquela posição em cada time
   - equilibrar o nível médio acumulado entre os times
   - em caso de empate, a escolha é aleatória (por isso o sorteio pode variar a cada clique)

## 📝 Limitações conhecidas

- `localStorage` é local ao navegador/dispositivo — não sincroniza entre pessoas ou aparelhos diferentes
- O envio para o WhatsApp abre a tela de compartilhamento; a escolha do grupo é sempre manual (limitação da própria plataforma do WhatsApp)

## 📄 Licença

Uso livre para o Clube Monte Líbano e demais interessados.
