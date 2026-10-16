# Plano — Atlas interativo da Teoria do Crime

## Escopo aprovado
Website permanente em HTML para estudo da Teoria do Crime no Direito Penal brasileiro. A primeira página será um mapa mental panorâmico em paisagem, com todos os eixos principais e sub-ramos conectados por setas e nós clicáveis. Cada nó conduzirá à explicação detalhada correspondente. O conteúdo será desenvolvido com base no esquema fornecido, no e-book *Direito Penal — Parte Geral*, 7.ª edição (2026), e na *Coletânea Básica Penal*, 16.ª edição, atualizada até janeiro de 2026. Imprecisões e trechos desatualizados do esquema serão identificados e corrigidos, distinguindo texto legal de síntese doutrinária.

## Direção visual confirmada
- **Design movement:** atlas editorial jurídico cruzado com diagrama de mapa mental/wayfinding, inspirado na referência de fluxos fornecida pelo usuário.
- **Princípios:** panorama primeiro e aprofundamento progressivo; ramos e setas tornam relações explícitas; lei e doutrina visualmente distinguíveis; leitura longa com densidade organizada.
- **Filosofia cromática:** paleta botânica indicada pelo usuário. Superfícies claras e tons neutros para leitura; verdes e oliva para hierarquia, conexões e categorias; o lime `#e8fb85` realça artigos, alertas e pontos de foco sem comprometer contraste. Cores-base: `#e8fb85`, `#cada73`, `#a4b15c`, `#808a47`, `#5d6532`, `#3d421f`, `#1f220d`, `#d4e673`, `#aebd5d`, `#899548`, `#666f34`, `#454c22`, `#272b10`, `#101204`, `#d5e674`, `#afbd5e`, `#8a9549`, `#677035`, `#464c22`, `#e9fa8d`, `#cbd97a`, `#a5b162`, `#808a4b`, `#5e6535`, `#1f220e`, `#f0f1ec`, `#d0d2cc`, `#a9aba6`, `#848581`, `#60615e`, `#3f3f3d`, `#20201f`.
- **Layout:** uma prancha horizontal de página única com conceito central, três substratos ramificados, eixos transversais inferiores (iter criminis, concurso de pessoas e punibilidade); depois, navegação lateral/por tópicos com aprofundamento.
- **Elementos-símbolo:** conectores/setas tipo fluxograma; nós arredondados de cor botânica; marcadores compactos de artigos e de alertas doutrinários.
- **Interação:** os nós do mapa levam ao estudo; índice navegável, pesquisa/filtros, secções expansíveis, comparações clicáveis e revisão interativa, sem exigir dependências externas.
- **Animação:** transições breves em foco/hover, realce suave de ramos e revelação progressiva de conteúdo; desativar movimentos não essenciais com `prefers-reduced-motion`.
- **Tipografia:** títulos em serif editorial (Georgia ou equivalente de sistema); corpo e UI em sans-serif de sistema, com hierarquia explícita e tamanho confortável.
- **Essência da marca:** um atlas visual e claro para estudantes de Direito localizarem rapidamente a estrutura analítica do crime; personalidade: didática, rigorosa, navegável.
- **Voz:** objetiva e explicativa. Exemplos de microcopy: “Siga o fluxo: do fato à reprovação.” / “Lei e doutrina não são a mesma camada.”
- **Marca/logotipo:** monograma “T” em selo botânico/geometria de folha-livro, sem logotipo institucional de terceiros.
- **Cor-assinatura:** `#5d6532` (oliva profunda), com `#e8fb85` como realce.

## Organização de conteúdo
1. Conceito analítico, classificações e teorias do delito (tripartite e observação sobre a teoria bipartite).
2. Fato típico: conduta e teorias da ação; ação/omissão e posição de garantidor; dolo; culpa; resultado e suas classificações; nexo causal e concausas; tipicidade; erro de tipo e demais erros pertinentes.
3. Ilicitude: regra de análise, causas justificantes (arts. 23–25), requisitos, excesso, descriminantes putativas e consentimento do ofendido como construção doutrinária, com limites.
4. Culpabilidade: imputabilidade (arts. 26–28), potencial consciência da ilicitude/erro de proibição (art. 21), exigibilidade de conduta diversa/coação e obediência hierárquica (art. 22); consequências da inimputabilidade sem confundir sanção penal e medida de segurança.
5. Iter criminis: cogitação, preparação, execução, consumação, exaurimento; tentativa, desistência voluntária, arrependimento eficaz/posterior e crime impossível (arts. 14–17).
6. Concurso de pessoas: pressupostos, autoria/coautoria/participação, desvio subjetivo, participação de menor importância, comunicabilidade e participação impunível (arts. 29–31).
7. Punibilidade e causas de extinção (art. 107), explicitamente fora do rol de substratos da teoria tripartite.
8. Quadros de contraste, exemplos hipotéticos didáticos, alertas de erro comum e revisão ao fim de cada macrotema.

## Fontes e tratamento jurídico
- Base doutrinária: material de referência enviado pelo usuário e capítulos 10–16 do e-book CP Iuris, *Direito Penal — Parte Geral*, 7.ª ed. (2026).
- Base normativa enviada: Senado Federal, *Coletânea Básica Penal*, 16.ª ed., atualização até janeiro de 2026.
- Conferência normativa adicional: texto compilado oficial do Código Penal no Planalto: https://www.planalto.gov.br/ccivil_03/decreto-lei/del2848compilado.htm.
- Referências por artigo serão associadas às proposições correspondentes. Citações curtas ou sínteses serão identificadas como tais; não tratar conclusões doutrinárias como redação literal do Código. Assinalar a data de atualização da coletânea e recomendar conferência da legislação oficial para alterações posteriores.
- Material educacional, não aconselhamento jurídico para um caso concreto.

## Implementação e estrutura do projeto
Website estático/autocontido, sem contas, servidor de aplicação, banco de dados ou APIs; não instalar dependências sem necessidade. HTML, CSS e JavaScript no artefato principal, com SVG semântico clicável para o mapa.

- `public/index.html` — site, mapa, secções, interações, metadados e CSS de impressão.
- `public/manus-routes.json` — declaração da rota pública `/`.
- `public/favicon.svg` — símbolo do Atlas Penal.
- `public/atlas-simbolo.svg` — marca vetorial original, reutilizada no cabeçalho e no metadado da plataforma.
- `app.config.ts` — URL HTTPS literal da marca do projeto para a integração com WebDev.
- `plan.md` — este plano aprovado.
- `TODO.md` — outcomes e requisitos de aceitação.

No Preview, servir o site na porta configurada 3000 em `0.0.0.0`. Para publicação permanente, gerar saída estática diretamente de `public/` com configuração de build sem dependências (`command: true`, `outputDirectory: public`), registrar checkpoint no ramo canônico `main` e solicitar/publicar a versão aprovada pelo usuário. Publicação é etapa separada de checkpoint.
