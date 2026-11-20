# rea-engenharia-reversa

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Engenharia reversa com IA](guia/assets/banner.jpg)](https://inematds.github.io/rea-engenharia-reversa/guia/)

**ðŸ‡§ðŸ‡· PortuguÃªs Â· [ðŸ‡ºðŸ‡¸ English](README.en.md) Â· [ðŸ‡ªðŸ‡¸ EspaÃ±ol](README.es.md)**

Guia em portuguÃªs sobre o **REA (Reverse Engineer Anything)**, a ferramenta aberta que dÃ¡ ao seu agente de IA (Claude Code, Codex, Cursor, Geminiâ€¦) as ferramentas de engenharia reversa. ReÃºne os links, explica a tecnologia em linguagem simples, traz uma avaliaÃ§Ã£o honesta de para quem isso Ã© Ãºtil e um teste feito aqui. Os repositÃ³rios citados sÃ£o de terceiros: este repo sÃ³ organiza e explica.

## ðŸŽ¬ VÃ­deo

- **[LÃª o app, nÃ£o o servidor](https://inematds.github.io/rea-engenharia-reversa/videos/#servidor)**: por que o REA lÃª o app do banco e nÃ£o mexe na conta, o que vaza e a regra (1min36) Â· [reel](https://www.youtube.com/shorts/Wz1XZyEyFI8)
- **[REA por dentro (tÃ©cnico)](https://inematds.github.io/rea-engenharia-reversa/videos/#tecnico)**: por que funciona, arquitetura, evidÃªncia, o teste antes e depois na 6.4.0 e os limites.
- **[REA na prÃ¡tica](https://inematds.github.io/rea-engenharia-reversa/videos/#na-pratica)**: clone um app em 4 passos (2 min) Â· [reel](https://www.youtube.com/shorts/B9D1phZJXWM)
- **[REA, a IA que faz engenharia reversa](https://inematds.github.io/rea-engenharia-reversa/videos/#completo)** (6 min, capÃ­tulos e legendas)
- No YouTube: [dÃ¡ pra clonar o app que vocÃª usa](https://www.youtube.com/watch?v=dwxV0xXdElk) Â· [recria quase qualquer app?](https://www.youtube.com/watch?v=QQFhiUch0kk) Â· reels [1](https://www.youtube.com/shorts/eTgtEf5bnvU) [2](https://www.youtube.com/shorts/Hlmma9RB-UM) [3](https://www.youtube.com/shorts/HwbWFVrWC4w) [4](https://www.youtube.com/shorts/QWLSY0LfUAY)

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/rea-engenharia-reversa/guia/**

## O que Ã©

Engenharia reversa Ã© descobrir como um programa funciona olhando sÃ³ o executÃ¡vel, sem o cÃ³digo-fonte. O REA (Reverse Engineer Anything) Ã© uma ferramenta aberta que liga o seu agente de IA a descompiladores como o Ghidra, da NSA, e devolve as conclusÃµes com a prova e os limites de cada uma. Serve para desenvolvedores, gente de seguranÃ§a e quem estuda software. Para usar, vocÃª precisa de Node.js e de um agente de IA no terminal.

## Em 4 frases

- **Engenharia reversa** Ã© entender como um programa funciona olhando sÃ³ o executÃ¡vel, sem o cÃ³digo-fonte.
- O **Ghidra** (da NSA, grÃ¡tis), o **Hopper** e o **IDA Pro** sempre fizeram isso, mas exigiam dias ou semanas de especialista.
- O **REA** Ã© um servidor **MCP**: uma ponte entre o seu agente e esses programas. O agente pede "abre esse binÃ¡rio", "quem chama essa funÃ§Ã£o?", e recebe pseudocÃ³digo, assembly e ligaÃ§Ãµes, **com evidÃªncia, limites e o que ficou sem resposta**.
- Tudo roda **na sua mÃ¡quina**; o programa analisado nÃ£o Ã© enviado.

## Links

| Projeto | O que Ã© | LicenÃ§a |
|---|---|---|
| [morluto/rea](https://github.com/morluto/rea) | O REA: MCP + CLI de engenharia reversa para agentes (TypeScript, ~144 mil estrelas, versÃ£o 6.4.0 em 12/10/2026) | MIT |
| [rea.tools](https://rea.tools/) | Site oficial: guias ilustrados e casos reais | â€” |
| [NationalSecurityAgency/ghidra](https://github.com/NationalSecurityAgency/ghidra) | Ghidra, o descompilador gratuito da NSA (Java, ~82 mil estrelas, 12.1.4) | Apache-2.0 |
| [N0zoM1z0/dx-ball](https://github.com/N0zoM1z0/dx-ball) | ReconstruÃ§Ã£o do jogo DX-Ball 1.07 em C/C++ com REA + Ghidra, testada byte a byte | MIT |
| [N0zoM1z0/th04](https://github.com/N0zoM1z0/th04) | ReconstruÃ§Ã£o do Touhou 4 (PC-98, DOS 16 bits) | MIT |
| [storytold/photocraft](https://github.com/storytold/photocraft) | PhotoCraft: Photoshop refeito do zero em Rust, *clean room* (nÃ£o usa o REA) | MIT / Apache-2.0 |
| [storytold/filmcraft](https://github.com/storytold/filmcraft) Â· [lightcraft](https://github.com/storytold/lightcraft) Â· [artcraft](https://github.com/storytold/artcraft) | Premiere, Lightroom e a suÃ­te ArtCraft, mesmo mÃ©todo | Apache-2.0 |
| [SRE-Bench (Columbia)](https://daplab.cs.columbia.edu/projects/sre-bench/) | Benchmark de agentes em engenharia reversa de binÃ¡rios protegidos | â€” |

## Os casos que mostram o que dÃ¡ pra fazer

- **Cofre fechado:** um app compilado sem nomes de funÃ§Ã£o (242+ funÃ§Ãµes `FUN_â€¦`). O agente achou a funÃ§Ã£o certa em poucas chamadas, recuperou as 3 regras do cÃ³digo de desbloqueio e escreveu um gerador de cÃ³digos. O cofre abriu.
- **DX-Ball (anos 90):** 528 funÃ§Ãµes candidatas, 283 jÃ¡ reescritas, **140 idÃªnticas byte a byte** ao original (22.674 bytes). O cÃ¡lculo do som esquerda/direita passou em 3.205 testes contra o x86 original. Ciclo: rastrear no Ghidra â†’ escrever em C â†’ compilar com o Visual C++ 4 â†’ comparar.
- **Fone de ouvido:** um usuÃ¡rio criou, em ~30 min de idas e vindas, um app prÃ³prio de um botÃ£o para ligar a reduÃ§Ã£o de vento, no lugar do app oficial.
- **Notion:** o agente seguiu o "copiar e colar" do app atÃ© o processo principal do Electron e o formato da Ã¡rea de transferÃªncia.
- **PhotoCraft:** outro caminho, sem olhar o binÃ¡rio: documentaÃ§Ã£o pÃºblica + testes contra o Photoshop. Ainda em alfa, com recursos faltando.

## Como comeÃ§ar

```bash
# precisa de Node.js 22.19+, 24.11+ ou 26+
npx rea-agents setup          # mostra o plano, faz backup da config e pergunta antes
rea doctor --client claude_code --json   # confere sÃ³ o que a sua tarefa precisa
```

O teste mais barato, sem Ghidra nem MCP, Ã© a anÃ¡lise estÃ¡tica de um app Electron:

```bash
npx -y rea-agents@latest analyze-javascript-application /caminho/absoluto/do/app.asar --json
```

Para binÃ¡rios nativos (Mac, Windows, Linux) Ã© preciso um descompilador instalado: Ghidra (grÃ¡tis), Hopper ou IDA.

**Quer fazer a sua prÃ³pria versÃ£o de um app?** Veja o roteiro [Como reconstruir um app com o REA](pratica/RECONSTRUIR.md): escolher o alvo (o que Ã© local vem, o que Ã© nuvem nÃ£o), montar o ambiente, entender antes de construir, iterar nos detalhes e ir alÃ©m do original.

## Vale a pena? AvaliaÃ§Ã£o

**Ãštil de verdade para:**

- **Desenvolvedores** que querem entender como um app muito bom resolve busca, sincronizaÃ§Ã£o ou Ã¡rea de transferÃªncia, e fazer a prÃ³pria versÃ£o.
- **SeguranÃ§a e privacidade:** auditar os apps instalados na sua mÃ¡quina e ver o que eles mandam pra fora.
- **Recuperar lÃ³gica** de um programa seu cujo cÃ³digo se perdeu.
- **Estudo, CTF e preservaÃ§Ã£o** de software antigo (jogos, sistemas legados).
- **Quem constrÃ³i ferramentas para LLM:** o formato de resposta do REA (evidÃªncia Â· mapa Â· limites Â· desconhecidos) Ã© um bom modelo para qualquer agente.

**NÃ£o Ã© para:**

- Leigos sem terminal: exige Node, linha de comando e paciÃªncia com versÃµes que mudam todo dia (5.0 â†’ 6.3 em trÃªs dias).
- Copiar o produto de um concorrente: Ã© arriscado juridicamente e perde o ponto. Entenda a ideia e faÃ§a melhor.
- Programas muito protegidos (VMProtect, ofuscaÃ§Ã£o pesada) ou cuja lÃ³gica roda no servidor: aÃ­ o REA ajuda pouco. O resultado tambÃ©m depende muito do modelo de IA usado.

### Reteste na 6.4.0 (12/10/2026)

O mesmo app Electron que travou na 6.3.0 terminou em **94,5 s** na 6.4.0, com pico de 1,26 GB: 202 arquivos JS lidos, 0 falhas, 13.500 achados. O arquivo que travava guardou os fatos estÃ¡ticos e o resto virou limitaÃ§Ã£o declarada. Rodamos isolado (HOME de teste, teto de memÃ³ria e de tempo) com `--max-heap-mb 1024 --analysis-timeout-ms 60000`. Detalhes e o comando no [guia](https://inematds.github.io/rea-engenharia-reversa/guia/#teste64).

### Teste feito aqui (10/10/2026)

Rodamos o REA 6.3.0 (`analyze-javascript-application`, sem Ghidra e sem MCP) num servidor Linux ARM. **Funcionou** num app Node nosso (97 arquivos, 3,5 MB): em 20 s e 1,3 GB de RAM devolveu um grafo com 2.109 nÃ³s e 3.104 ligaÃ§Ãµes, 2.508 achados e 5 limitaÃ§Ãµes declaradas, sem executar o app. **Travou** em dois alvos que tinham um Ãºnico arquivo JS gigante (o bundle de um app Electron instalado e o `typescript/_tsc.js`, de 6 MB): ficou a 100% de CPU por mais de 20 min no mesmo arquivo, ignorou o SIGTERM e sÃ³ parou com `kill -9`. ConclusÃ£o: funciona bem em projetos de tamanho normal; em apps grandes, rode com teto de tempo (`timeout -s KILL`) e sem `node_modules`. O JSON completo Ã© enorme (241 MB aqui): no dia a dia, deixe o agente consultar pelo MCP em vez de ler o arquivo inteiro.

## Cuidados

1. **Lei e licenÃ§a:** muitas licenÃ§as proÃ­bem engenharia reversa; quebrar proteÃ§Ã£o contra cÃ³pia Ã© outro problema. Terreno seguro: programas seus, cÃ³digo aberto, desafios de seguranÃ§a e o que vocÃª tem autorizaÃ§Ã£o para testar.
2. **NÃ£o Ã© sandbox:** se o REA executar o alvo, ele roda com as suas permissÃµes. Um binÃ¡rio estranho pode esconder instruÃ§Ãµes para enganar o agente. Use mÃ¡quina isolada e mantenha as aprovaÃ§Ãµes do agente ligadas.
3. **Muda todo dia:** atualize (`rea update` ou `npx rea-agents@latest setup`) antes de abrir um problema.

---

Mais conteÃºdo aberto e gratuito em **[inema.club](https://inema.club)**.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>