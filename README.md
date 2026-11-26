ï»¿# rea-engenharia-reversa

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Engenharia reversa com IA](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/arckhe-/guia/)

**ê°Å¸â¡Â§ê°Å¸â¡Â· PortuguêÂªs êÂ· [ê°Å¸â¡Âºê°Å¸â¡Â¸ English](README.en.md) êÂ· [ê°Å¸â¡Âªê°Å¸â¡Â¸ EspaêÂ±ol](README.es.md)**

Guia em portuguêÂªs sobre o **REA (Reverse Engineer Anything)**, a ferramenta aberta que dêÂ¡ ao seu agente de IA (Claude Code, Codex, Cursor, Geminiê¢â¬Â¦) as ferramentas de engenharia reversa. ReêÂºne os links, explica a tecnologia em linguagem simples, traz uma avaliaêÂ§êÂ£o honesta de para quem isso êÂ© êÂºtil e um teste feito aqui. Os repositêÂ³rios citados sêÂ£o de terceiros: este repo sêÂ³ organiza e explica.

## ê°Å¸Å½Â¬ VêÂ­deo

- **[LêÂª o app, nêÂ£o o servidor](https://linnoff88-dev.github.io/arckhe-/videos/#servidor)**: por que o REA lêÂª o app do banco e nêÂ£o mexe na conta, o que vaza e a regra (1min36) êÂ· [reel](https://www.youtube.com/shorts/Wz1XZyEyFI8)
- **[REA por dentro (têÂ©cnico)](https://linnoff88-dev.github.io/arckhe-/videos/#tecnico)**: por que funciona, arquitetura, evidêÂªncia, o teste antes e depois na 6.4.0 e os limites.
- **[REA na prêÂ¡tica](https://linnoff88-dev.github.io/arckhe-/videos/#na-pratica)**: clone um app em 4 passos (2 min) êÂ· [reel](https://www.youtube.com/shorts/B9D1phZJXWM)
- **[REA, a IA que faz engenharia reversa](https://linnoff88-dev.github.io/arckhe-/videos/#completo)** (6 min, capêÂ­tulos e legendas)
- No YouTube: [dêÂ¡ pra clonar o app que vocêÂª usa](https://www.youtube.com/watch?v=dwxV0xXdElk) êÂ· [recria quase qualquer app?](https://www.youtube.com/watch?v=QQFhiUch0kk) êÂ· reels [1](https://www.youtube.com/shorts/eTgtEf5bnvU) [2](https://www.youtube.com/shorts/Hlmma9RB-UM) [3](https://www.youtube.com/shorts/HwbWFVrWC4w) [4](https://www.youtube.com/shorts/QWLSY0LfUAY)

## ê°Å¸ââ Guia de uso

Guia completo (landing + passo a passo): **https://linnoff88-dev.github.io/arckhe-/guia/**

## O que êÂ©

Engenharia reversa êÂ© descobrir como um programa funciona olhando sêÂ³ o executêÂ¡vel, sem o cêÂ³digo-fonte. O REA (Reverse Engineer Anything) êÂ© uma ferramenta aberta que liga o seu agente de IA a descompiladores como o Ghidra, da NSA, e devolve as conclusêÂµes com a prova e os limites de cada uma. Serve para desenvolvedores, gente de seguranêÂ§a e quem estuda software. Para usar, vocêÂª precisa de Node.js e de um agente de IA no terminal.

## Em 4 frases

- **Engenharia reversa** êÂ© entender como um programa funciona olhando sêÂ³ o executêÂ¡vel, sem o cêÂ³digo-fonte.
- O **Ghidra** (da NSA, grêÂ¡tis), o **Hopper** e o **IDA Pro** sempre fizeram isso, mas exigiam dias ou semanas de especialista.
- O **REA** êÂ© um servidor **MCP**: uma ponte entre o seu agente e esses programas. O agente pede "abre esse binêÂ¡rio", "quem chama essa funêÂ§êÂ£o?", e recebe pseudocêÂ³digo, assembly e ligaêÂ§êÂµes, **com evidêÂªncia, limites e o que ficou sem resposta**.
- Tudo roda **na sua mêÂ¡quina**; o programa analisado nêÂ£o êÂ© enviado.

## Links

| Projeto | O que êÂ© | LicenêÂ§a |
|---|---|---|
| [morluto/rea](https://github.com/morluto/rea) | O REA: MCP + CLI de engenharia reversa para agentes (TypeScript, ~144 mil estrelas, versêÂ£o 6.4.0 em 12/10/2026) | MIT |
| [rea.tools](https://rea.tools/) | Site oficial: guias ilustrados e casos reais | ê¢â¬â |
| [NationalSecurityAgency/ghidra](https://github.com/NationalSecurityAgency/ghidra) | Ghidra, o descompilador gratuito da NSA (Java, ~82 mil estrelas, 12.1.4) | Apache-2.0 |
| [N0zoM1z0/dx-ball](https://github.com/N0zoM1z0/dx-ball) | ReconstruêÂ§êÂ£o do jogo DX-Ball 1.07 em C/C++ com REA + Ghidra, testada byte a byte | MIT |
| [N0zoM1z0/th04](https://github.com/N0zoM1z0/th04) | ReconstruêÂ§êÂ£o do Touhou 4 (PC-98, DOS 16 bits) | MIT |
| [storytold/photocraft](https://github.com/storytold/photocraft) | PhotoCraft: Photoshop refeito do zero em Rust, *clean room* (nêÂ£o usa o REA) | MIT / Apache-2.0 |
| [storytold/filmcraft](https://github.com/storytold/filmcraft) êÂ· [lightcraft](https://github.com/storytold/lightcraft) êÂ· [artcraft](https://github.com/storytold/artcraft) | Premiere, Lightroom e a suêÂ­te ArtCraft, mesmo mêÂ©todo | Apache-2.0 |
| [SRE-Bench (Columbia)](https://daplab.cs.columbia.edu/projects/sre-bench/) | Benchmark de agentes em engenharia reversa de binêÂ¡rios protegidos | ê¢â¬â |

## Os casos que mostram o que dêÂ¡ pra fazer

- **Cofre fechado:** um app compilado sem nomes de funêÂ§êÂ£o (242+ funêÂ§êÂµes `FUN_ê¢â¬Â¦`). O agente achou a funêÂ§êÂ£o certa em poucas chamadas, recuperou as 3 regras do cêÂ³digo de desbloqueio e escreveu um gerador de cêÂ³digos. O cofre abriu.
- **DX-Ball (anos 90):** 528 funêÂ§êÂµes candidatas, 283 jêÂ¡ reescritas, **140 idêÂªnticas byte a byte** ao original (22.674 bytes). O cêÂ¡lculo do som esquerda/direita passou em 3.205 testes contra o x86 original. Ciclo: rastrear no Ghidra ê¢â â escrever em C ê¢â â compilar com o Visual C++ 4 ê¢â â comparar.
- **Fone de ouvido:** um usuêÂ¡rio criou, em ~30 min de idas e vindas, um app prêÂ³prio de um botêÂ£o para ligar a reduêÂ§êÂ£o de vento, no lugar do app oficial.
- **Notion:** o agente seguiu o "copiar e colar" do app atêÂ© o processo principal do Electron e o formato da êÂ¡rea de transferêÂªncia.
- **PhotoCraft:** outro caminho, sem olhar o binêÂ¡rio: documentaêÂ§êÂ£o pêÂºblica + testes contra o Photoshop. Ainda em alfa, com recursos faltando.

## Como comeêÂ§ar

```bash
# precisa de Node.js 22.19+, 24.11+ ou 26+
npx rea-agents setup          # mostra o plano, faz backup da config e pergunta antes
rea doctor --client claude_code --json   # confere sêÂ³ o que a sua tarefa precisa
```

O teste mais barato, sem Ghidra nem MCP, êÂ© a anêÂ¡lise estêÂ¡tica de um app Electron:

```bash
npx -y rea-agents@latest analyze-javascript-application /caminho/absoluto/do/app.asar --json
```

Para binêÂ¡rios nativos (Mac, Windows, Linux) êÂ© preciso um descompilador instalado: Ghidra (grêÂ¡tis), Hopper ou IDA.

**Quer fazer a sua prêÂ³pria versêÂ£o de um app?** Veja o roteiro [Como reconstruir um app com o REA](pratica/RECONSTRUIR.md): escolher o alvo (o que êÂ© local vem, o que êÂ© nuvem nêÂ£o), montar o ambiente, entender antes de construir, iterar nos detalhes e ir alêÂ©m do original.

## Vale a pena? AvaliaêÂ§êÂ£o

**êÅ¡til de verdade para:**

- **Desenvolvedores** que querem entender como um app muito bom resolve busca, sincronizaêÂ§êÂ£o ou êÂ¡rea de transferêÂªncia, e fazer a prêÂ³pria versêÂ£o.
- **SeguranêÂ§a e privacidade:** auditar os apps instalados na sua mêÂ¡quina e ver o que eles mandam pra fora.
- **Recuperar lêÂ³gica** de um programa seu cujo cêÂ³digo se perdeu.
- **Estudo, CTF e preservaêÂ§êÂ£o** de software antigo (jogos, sistemas legados).
- **Quem constrêÂ³i ferramentas para LLM:** o formato de resposta do REA (evidêÂªncia êÂ· mapa êÂ· limites êÂ· desconhecidos) êÂ© um bom modelo para qualquer agente.

**NêÂ£o êÂ© para:**

- Leigos sem terminal: exige Node, linha de comando e paciêÂªncia com versêÂµes que mudam todo dia (5.0 ê¢â â 6.3 em trêÂªs dias).
- Copiar o produto de um concorrente: êÂ© arriscado juridicamente e perde o ponto. Entenda a ideia e faêÂ§a melhor.
- Programas muito protegidos (VMProtect, ofuscaêÂ§êÂ£o pesada) ou cuja lêÂ³gica roda no servidor: aêÂ­ o REA ajuda pouco. O resultado tambêÂ©m depende muito do modelo de IA usado.

### Reteste na 6.4.0 (12/10/2026)

O mesmo app Electron que travou na 6.3.0 terminou em **94,5 s** na 6.4.0, com pico de 1,26 GB: 202 arquivos JS lidos, 0 falhas, 13.500 achados. O arquivo que travava guardou os fatos estêÂ¡ticos e o resto virou limitaêÂ§êÂ£o declarada. Rodamos isolado (HOME de teste, teto de memêÂ³ria e de tempo) com `--max-heap-mb 1024 --analysis-timeout-ms 60000`. Detalhes e o comando no [guia](https://linnoff88-dev.github.io/arckhe-/guia/#teste64).

### Teste feito aqui (10/10/2026)

Rodamos o REA 6.3.0 (`analyze-javascript-application`, sem Ghidra e sem MCP) num servidor Linux ARM. **Funcionou** num app Node nosso (97 arquivos, 3,5 MB): em 20 s e 1,3 GB de RAM devolveu um grafo com 2.109 nêÂ³s e 3.104 ligaêÂ§êÂµes, 2.508 achados e 5 limitaêÂ§êÂµes declaradas, sem executar o app. **Travou** em dois alvos que tinham um êÂºnico arquivo JS gigante (o bundle de um app Electron instalado e o `typescript/_tsc.js`, de 6 MB): ficou a 100% de CPU por mais de 20 min no mesmo arquivo, ignorou o SIGTERM e sêÂ³ parou com `kill -9`. ConclusêÂ£o: funciona bem em projetos de tamanho normal; em apps grandes, rode com teto de tempo (`timeout -s KILL`) e sem `node_modules`. O JSON completo êÂ© enorme (241 MB aqui): no dia a dia, deixe o agente consultar pelo MCP em vez de ler o arquivo inteiro.

## Cuidados

1. **Lei e licenêÂ§a:** muitas licenêÂ§as proêÂ­bem engenharia reversa; quebrar proteêÂ§êÂ£o contra cêÂ³pia êÂ© outro problema. Terreno seguro: programas seus, cêÂ³digo aberto, desafios de seguranêÂ§a e o que vocêÂª tem autorizaêÂ§êÂ£o para testar.
2. **NêÂ£o êÂ© sandbox:** se o REA executar o alvo, ele roda com as suas permissêÂµes. Um binêÂ¡rio estranho pode esconder instruêÂ§êÂµes para enganar o agente. Use mêÂ¡quina isolada e mantenha as aprovaêÂ§êÂµes do agente ligadas.
3. **Muda todo dia:** atualize (`rea update` ou `npx rea-agents@latest setup`) antes de abrir um problema.

---

Mais conteêÂºdo aberto e gratuito em **[ARCKHÉ AI](https://ARCKHÉ AI)**.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>