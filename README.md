# LexBrasil — Navegador da Legislação Brasileira

Interface web para pesquisar e ler as leis brasileiras, construída inteiramente
sobre o repositório aberto [ctresb/leis](https://github.com/ctresb/leis)
(323.849 normas em Markdown: Constituição Federal, legislação federal desde
1822 e leis de 25 estados + DF).

## Funcionalidades

- **Pesquisa por número + ano** — ex.: 10406/2002 (Código Civil)
- **Pesquisa por tema** — índice curado das principais leis federais
- **Navegação completa** na árvore de pastas do acervo (API do GitHub)
- **Leitor integrado** — metadados (ementa, situação, URN, fonte oficial),
  busca dentro do texto, controle de fonte, impressão e download do .md
- **Histórico de leitura** e links compartilháveis (rotas por hash)
- Arquivo único (HTML + CSS + JS), sem build e sem servidor

## Como rodar localmente

Basta abrir o index.html no navegador, ou servir a pasta:

    python3 -m http.server 8080

e acessar http://localhost:8080

## Notas técnicas

- Os dados vêm em tempo real de api.github.com e raw.githubusercontent.com
- Sem autenticação, a API do GitHub permite 60 requisições/hora por IP;
  o site aceita um token pessoal opcional (salvo só no navegador) para
  elevar o limite a 5.000/hora
- Listagens de pastas e textos são cacheados no localStorage

## Aviso

Os textos têm caráter informativo e **não substituem a publicação no
Diário Oficial**. Parte do acervo vem de OCR de PDF escaneado. Confira
sempre a fonte oficial indicada no cabeçalho de cada norma.

## Créditos

- Acervo das leis: [ctresb/leis](https://github.com/ctresb/leis)
- Atos oficiais não são protegidos por direito autoral (art. 8º, I, Lei 9.610/98)
- Bibliotecas: marked.js, DOMPurify, Fontsource (Inter e Playfair Display)
EOF
