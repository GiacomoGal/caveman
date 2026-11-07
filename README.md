<a id="guida-fork"></a>

# Guida del fork — GiacomoGal/caveman

Testo ordinario, per una persona. Non è voce da caverna. La skill di prodotto resta un artefatto: non è l'ordine di riscrivere questa guida.

Questa pagina è la guida del checkout `GiacomoGal/caveman` sul ramo inventario `main`. Sotto, dopo la matrice, c'è il README di prodotto upstream, conservato. Lotto documentale t127u, sezione 3. Snapshot inventario locale del 7 novembre 2026. Nessuna verifica remota nuova: il remote locale non certifica il ref sul forge, la sincronizzazione, la canonicità né un uso vivo.

Base git osservata prima di questa guida: `63e797cd753b301374947a5ed975c21775d962b9`. Lo SHA del commit che introduce la guida sta nel PR, non in questa frase.

## Stato

Identità di runtime e uso corrente restano **sconosciuti**. Il nome `caveman` non abbina questo repository a una VPS, a un servizio o a un owner di macchina. UNMAPPED esplicito. Nessun giudizio di inutilità. `nextdocscope=unresolved` è ambito di guida esplorativa: non attesta che il repository sia attivo, né che vada archiviato.

| Campo | Valore usato qui | Rango |
| --- | --- | --- |
| URL nel mandato | https://github.com/GiacomoGal/caveman | Citato. Non riaperto via API. |
| Origin locale | `github.com/GiacomoGal/caveman` | Path del remote di questo checkout. Credenziali non lette e non riportate. |
| Ref inventario | `main` | Inventario. Non ricontrollato sul forge. |
| Fork / archived | fork sì; archiviato no | Inventario. Parent sul forge non interrogato. |
| Linguaggio inventario | non rilevato | Non dedotto dal tree. |
| Descrizione inventario | «Claude Code skill that cuts 65% of tokens by talking like caveman» | Testo del mandato. Non è un risparmio misurato qui. |
| identity_proven | false | Nessuna evidenza di identità nel brief (`identity_evidence` vuoto). |
| Uso corrente | sconosciuto | `unknowncurrentuse=true`. |
| Proposte, decisioni, ricevute | elenchi vuoti | Nessuna proposta `executed=false` da promuovere a esito. |
| Autore nel testo upstream | Julius Brussee, `JuliusBrussee/caveman` | Copyright in `LICENSE` e URL già scritti nel tree. Non è un host e non è una VPS. |

Nel tree, senza chiamata al forge, risultano citati `https://github.com/JuliusBrussee/caveman` (README, `plugins/caveman/.codex-plugin/plugin.json`) e l'autore Julius Brussee (`LICENSE`, manifest del plugin). I manifest pubblici sono stati letti solo per questa citazione e non sono stati modificati. Non provano il legame fork parent sul forge.

## Come leggere il resto

1. Questa prefazione e la matrice sono la guida di questo fork.
2. Il corpo che inizia a [Testo upstream conservato](#testo-upstream-conservato) è il pitch di prodotto. La voce cavernicola lì è marca upstream, tenuta di proposito. Before/After resta il pitch, non la guida di inventario.
3. I comandi in quel corpo (install, hook, eval, benchmark) sono procedure soggette a un mandato diverso. Qui non sono stati eseguiti.
4. `AGENTS.md` e `CLAUDE.md` ripetono gli stessi limiti per gli agenti. Non sono una seconda matrice.
5. `CONTRIBUTING.md` descrive ancora un flusso di PR verso il progetto upstream. Questo lotto non apre una PR upstream.

## Cifre di token

Nel pitch compaiono, tra le altre, «~75%», «~71%», «65%» di media, l'intervallo «22%–87%», «~3x», «accuratezza 100%» e «~46%» per il compress. Sono claim upstream, lasciati nel testo. Non sono un risparmio verificato in questo lotto.

Controllo solo sui nomi dei file, senza aprirli e senza eseguirli:

- `benchmarks/results/` contiene `.gitkeep`. Nessun JSON di risultati in quell'elenco.
- `benchmarks/prompts.json` e `benchmarks/run.py` non sono stati aperti né eseguiti.
- `evals/snapshots/results.json` è presente e non è stato aperto. `evals/` non è stato eseguito.
- I manifest del plugin ripetono «~75%». Restano metadati di prodotto, non una misura.

`CLAUDE.md` vieta di inventare o arrotondare i numeri di benchmark. Qui i numeri non sono ricalcolati e non sono certificati.

## Cosa non fa questa guida

- Non installa skill, non aggiorna skill globali, non tocca profili.
- Non legge segreti, `.env`, `.env.local`, backup, memorie o dati privati. `CLAUDE.original.md` non è stato letto: è un backup del compress.
- Non modifica codice, config, script, dati, media, lock, né i file di skill. `docs/index.html` non è stato letto né aggiornato.
- Non apre path host citati nel prodotto: `~/.claude/.caveman-active`, `~/.claude/settings.json`, `~/.claude/hooks/`, `~/.config/caveman/config.json`. Non legge `ANTHROPIC_API_KEY` né `CAVEMAN_DEFAULT_MODE`.
- Non fa runtime, import applicativo, test dell'app, chiamata a provider o API, SSH, sync, merge, deploy, archive.
- Non inferisce identità o uso dal nome.
- Non dichiara PASS. Review indipendente, distinta da «integrato» o «funzionante».

<a id="matrice"></a>

## Matrice precedente → nuovo

Base delle righe: `63e797cd753b301374947a5ed975c21775d962b9`. «Riga» è il file prima di questa guida. Il rango nuovo non cancella l'obbligo: ne dice quando vale.

| ID | Precedente (fonte:riga) | Nuovo | Destinatario | Rango | Condizioni | Destinazione |
| --- | --- | --- | --- | --- | --- | --- |
| M1 | Assente nel repo. Brief, perimetro L3–L11 e §3 L39–L51 | Prefazione di stato unresolved / uso ignoto | Persone e agenti | Perimetro del lotto. Non è decisione di lifecycle | Snapshot locale 7 nov 2026. Nessuna verifica remota | Questa sezione |
| M2 | Assente. Brief §3, UNMAPPED | Divieto di dedurre VPS, servizio o owner dal nome | Persone e agenti | Limite | Nessun abbinamento per nome; nessun giudizio di inutilità | README, `AGENTS.md`, `CLAUDE.md` |
| M3 | `README.md` L1–L403, pitch intero | Stesso testo, più due note «Fork note» su cifre e «prove» | Lettori del prodotto | Istruzione upstream. Voce del pitch intenzionale | Comandi non eseguiti. Cifre non certificate qui | Sotto «Testo upstream conservato» |
| M4 | Claim in `README.md` L28, L69, L110–L120, L349–L368, L372, L378; `CLAUDE.md` L22; descrizione skill e manifest «~75%»; compress «~46%» / «~65%» | Numeri lasciati. Rango: claim upstream, non risparmio verificato | Lettori | Claim. Il numero resta citato | Elenco file sopra. Nessun run, nessun JSON aperto | Note nel pitch e frase in `CLAUDE.md` |
| M5 | Procedure `README.md` L123–L283, hook L174–L185, Gemini L213–L216, eval L382–L387; `hooks/README.md`; `evals/README.md` | Stesse procedure, non eseguite | Chi installa, sotto altro mandato | Testo procedurale upstream | Soggette a mandato. Non lanciate da questa guida. Tabelle install non riaudite sul codice | Pitch README invariato tranne le due note. `hooks/README.md` e `evals/README.md` non modificati |
| M6 | Snippet always-on `README.md` L264–L273 | Resta nel pitch. Non è lo stile di questa prefazione | Utenti senza hook, altrove | Snippet opzionale di prodotto | Non promosso a stile universale di sessione | Corpo upstream |
| M7 | `AGENTS.md` L1–L4, quattro righe `@` verso le skill | Percorsi tenuti. Niente `@`. Trigger nel frontmatter di ogni skill | Agenti che leggono `AGENTS.md` | Mappa di ingresso | La skill vale se invocata, o se una copia always-on già nel tree inietta il corpo breve. Non per riscrivere le guide | `AGENTS.md` |
| M8 | `GEMINI.md` L1–L4, stessi `@` | Invariato | Gemini CLI | Meccanismo upstream lasciato | Non è ordine di stile per queste guide | File non modificato |
| M9 | `rules/caveman-activate.md` L1–L15 e copie `.cursor/rules/caveman.mdc` (`alwaysApply`), `.windsurf/rules/caveman.md` (`always_on`), `.clinerules/caveman.md`, `.github/copilot-instructions.md` | File non modificati. Documentati come iniettori già presenti | Quegli agenti | Regola di prodotto generata, non guida documentale | CI le rigenera dalla sorgente. Editarle qui le farebbe perdere o toccherebbe config | Invariati |
| M10 | `skills/caveman/SKILL.md`, commit, review, help; `caveman-compress/SKILL.md`; copie in `skills/compress`, `compress/`, `plugins/`, `.cursor/skills`, `.windsurf/skills`, `caveman/` | Byte invariati | Runtime della skill, quando scatta | Artefatto. Non ordine di riscrittura guide | Trigger nel frontmatter. Confini interni: codice, commit e PR in prosa normale; stop con «stop caveman» o «normal mode»; commit non lancia git; review non approva; compress non tocca codice, config, env, lock, html e non comprime `*.original.md` | Path invariati |
| M11 | `CLAUDE.md` L1–L199 | Corpo upstream tenuto. Blocco fork in cima. Tre precisazioni: voce, cifra, riga Copilot | Agenti che modificano il repo | Obblighi vigenti | Vedi tabella annidata | `CLAUDE.md` |
| M12 | `CONTRIBUTING.md` L1–L21 | Invariato | Contributor del progetto upstream | Flusso PR descritto lì | Questa guida non apre PR upstream. Link issue non verificato in rete | File non modificato |
| M13 | `.github/ISSUE_TEMPLATE/bug_report.md`, `feature_request.md` | Invariati | Chi apre issue | Moduli. Non norme di sessione | Non promossi a stile o a roadmap eseguita | File non modificati |
| M14 | `skills/caveman-help/SKILL.md` L39–L59, env e `~/.config/caveman/config.json` | Invariato | Chi invoca `/caveman-help` | Artefatto one-shot | Path e env non aperti. URL upstream non richiesto in rete | File non modificato |
| M15 | `caveman-compress/SECURITY.md` | Invariato | Lettori del compress | Nota di sicurezza del file | Claim Snyk e «false positive» non riverificati | File non modificato |
| M16 | `hooks/README.md`, path `~/.claude/` | Invariato | Chi installa hook, sotto mandato | Procedura upstream | Path non aperti. Script non eseguiti | File non modificato |
| M17 | `evals/README.md` L70–L84: niente fedeltà, costo, significatività; tokenizer approssimato | Invariato | Chi legge le eval | Limite di misura già scritto | Snapshot non usato come prova | File non modificato |
| M18 | `LICENSE` L1–L21, MIT, copyright Julius Brussee 2026 | Invariato | Destinatari della licenza | Licenza | Non è identità di VPS | File non modificato |
| M19 | `docs/index.html`, `docs/.nojekyll` | Non letti, non modificati | Pagine GitHub, se pubblicate | Fuori dalle guide Markdown | Possibile deriva rispetto a questo README. Non allineata di proposito | Invariati |
| M20 | `commands/*.toml`, `.codex/hooks.json`, workflow, `FUNDING.yml` | Non aperti, non modificati | Secondo il file, non secondo questa guida | Config o prompt non promossi | Non letti, per non elevare prompt o config a norma | Invariati |
| M21 | Path host e segreti citati in M14, M16 e in `CLAUDE.md` sui benchmark (`.env.local`) | Restano citazioni chiuse | Nessuno in questo lotto | Divieto di lettura | Non aperti | Nessuna destinazione nuova |
| M22 | URL upstream nel pitch e origin `GiacomoGal/caveman` | Separazione tenuta | Lettori | Fatto di checkout, non parent forge provato | Niente API. Inventario: fork sì | Prefazione |
| M23 | Brief: `proposalOct`, `decisionlater`, `executionreceipt` vuoti | Nessuna archiviazione, nessuna riattivazione | Review | unresolved resta unresolved | Una proposta non eseguita non è un esito. Qui non c'è neppure la proposta | Prefazione |

### Clausole annidate di `CLAUDE.md` (M11)

| ID | Precedente (fonte:riga) | Nuovo | Destinatario | Rango | Condizioni | Destinazione |
| --- | --- | --- | --- | --- | --- | --- |
| M11a | Regole README L5–L16: leggibile, Before/After, tabella install, tabella funzioni, voce, numeri reali, blocco dettagli, prova dei 60 secondi | Tengono per il pitch. La prefazione resta in prosa ordinaria e sta prima del pitch | Chi edita il README | Obbligo upstream, con eccezione esplicita | Non normalizzare il pitch. Non cavernizzare la prefazione | `CLAUDE.md` |
| M11b | Sorgenti uniche L29–L37; copie sync L41–L53 | Invariato come regola. Questo lotto non edita quelle sorgenti né le copie | Chi cambia comportamento | Obbligo | Una modifica di comportamento non si fa in questa guida | Corpo `CLAUDE.md` |
| M11c | CI `.github/workflows/sync-skill.yml` L57–L67 | Descrizione tenuta. Workflow non aperto e non lanciato | Chi fa merge a main upstream | Descrizione di config | Config non letta. Nessun sync | Corpo `CLAUDE.md` |
| M11d | Hook L71–L122, fail silenzioso, flag `~/.claude/.caveman-active` | Descrizione tenuta. Path non aperti. Script non eseguiti | Chi tocca gli hook, sotto mandato | Obbligo di non bloccare la sessione | Vale sul codice hook, non modificato qui | Corpo `CLAUDE.md` |
| M11e | Livelli, auto-clarity, compress, commit, review L126–L145 | Restano definiti nei file skill | Chi edita una skill | Obbligo nel file skill | File non riscritti | Rinvio, non copia del prompt |
| M11f | Tabella agenti L150–L163, frase Copilot via `AGENTS.md` | Tabella tenuta. Nota: `AGENTS.md` non importa più le skill per `@`. Il testo breve Copilot resta in `.github/copilot-instructions.md` | Agenti del repo | Obbligo corretto, non ristretto in silenzio | Conflitto esplicito col vecchio `@` | Nota nel corpo `CLAUDE.md` |
| M11g | Eval: delta onesto skill contro terse, non contro baseline L167–L180 | Tenuto | Chi rigenera gli snapshot | Obbligo di misura | Non eseguito. JSON non aperto | Corpo `CLAUDE.md` |
| M11h | Benchmark L184–L188, `ANTHROPIC_API_KEY` in `.env.local` | Procedura tenuta, non eseguita. Env non letto | Chi riproduce, sotto mandato | Procedura | Segreto non aperto | Corpo `CLAUDE.md` |
| M11i | Regole finali L192–L199 | Tenute, sotto i limiti del fork | Agenti | Obbligo | Non autorizzano a cancellare la prefazione né a inventare un risparmio | Corpo `CLAUDE.md` più blocco fork |

Conflitto esplicito, risolto senza spegnere gli iniettori: in questo workspace Cursor la copia `.cursor/rules/caveman.mdc` può ancora imporre il corpo breve a ogni turno. Questa guida non la modifica. Il testo nuovo della prefazione, di `AGENTS.md` e del blocco fork è comunque prosa ordinaria, perché il mandato vieta di trattare la skill come ordine di riscrittura.

## Limiti del controllo link

Nessuna richiesta HTTP. Nessuna API. Controllo statico sui tre file di questa guida, dopo gli inserimenti: ogni link relativo visibile (fuori dai blocchi di codice) punta a un file presente nel checkout. Ancore esplicite di questa prefazione: `guida-fork`, `matrice`, `testo-upstream-conservato`. I link esterni del pitch non sono stati contattati; la sintassi è quella upstream. Il link issue in `CONTRIBUTING.md` non è stato risolto in rete. Le tabelle di install non sono state riaudite contro il codice.

<a id="testo-upstream-conservato"></a>

## Testo upstream conservato

Il corpo che segue è il README di prodotto com'era sulla base `63e797cd753b301374947a5ed975c21775d962b9`, con due soli inserimenti: le citazioni «Fork note» accanto alla tabella benchmark e accanto alla frase «prove». Il resto di quel corpo non è stato riscritto.

<p align="center">
  <img src="https://em-content.zobj.net/source/apple/391/rock_1faa8.png" width="120" />
</p>

<h1 align="center">caveman</h1>

<p align="center">
  <strong>why use many token when few do trick</strong>
</p>

<p align="center">
  <a href="https://github.com/JuliusBrussee/caveman/stargazers"><img src="https://img.shields.io/github/stars/JuliusBrussee/caveman?style=flat&color=yellow" alt="Stars"></a>
  <a href="https://github.com/JuliusBrussee/caveman/commits/main"><img src="https://img.shields.io/github/last-commit/JuliusBrussee/caveman?style=flat" alt="Last Commit"></a>
  <a href="LICENSE"><img src="https://img.shields.io/github/license/JuliusBrussee/caveman?style=flat" alt="License"></a>
</p>

<p align="center">
  <a href="#before--after">Before/After</a> •
  <a href="#install">Install</a> •
  <a href="#intensity-levels">Levels</a> •
  <a href="#caveman-skills">Skills</a> •
  <a href="#benchmarks">Benchmarks</a> •
  <a href="#evals">Evals</a>
</p>

---

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill/plugin and Codex plugin that makes agent talk like caveman — cutting **~75% of output tokens** while keeping full technical accuracy. Now with [文言文 mode](#文言文-wenyan-mode), [terse commits](#caveman-commit), [one-line code reviews](#caveman-review), and a [compression tool](#caveman-compress) that cuts **~46% of input tokens** every session.

Based on the viral observation that caveman-speak dramatically reduces LLM token usage without losing technical substance. So we made it a one-line install.

## Before / After

<table>
<tr>
<td width="50%">

### 🗣️ Normal Claude (69 tokens)

> "The reason your React component is re-rendering is likely because you're creating a new object reference on each render cycle. When you pass an inline object as a prop, React's shallow comparison sees it as a different object every time, which triggers a re-render. I'd recommend using useMemo to memoize the object."

</td>
<td width="50%">

### 🪨 Caveman Claude (19 tokens)

> "New object ref each render. Inline object prop = new ref = re-render. Wrap in `useMemo`."

</td>
</tr>
<tr>
<td>

### 🗣️ Normal Claude

> "Sure! I'd be happy to help you with that. The issue you're experiencing is most likely caused by your authentication middleware not properly validating the token expiry. Let me take a look and suggest a fix."

</td>
<td>

### 🪨 Caveman Claude

> "Bug in auth middleware. Token expiry check use `<` not `<=`. Fix:"

</td>
</tr>
</table>

**Same fix. 75% less word. Brain still big.**

**Pick your level of grunt:**

<table>
<tr>
<td width="25%">

#### 🪶 Lite

> "Your component re-renders because you create a new object reference each render. Inline object props fail shallow comparison every time. Wrap it in `useMemo`."

</td>
<td width="25%">

#### 🪨 Full

> "New object ref each render. Inline object prop = new ref = re-render. Wrap in `useMemo`."

</td>
<td width="25%">

#### 🔥 Ultra

> "Inline obj prop → new ref → re-render. `useMemo`."

</td>
<td width="25%">

#### 📜 文言文

> "物出新參照，致重繪。useMemo Wrap之。"

</td>
</tr>
</table>

**Same answer. You pick how many word.**

```
┌─────────────────────────────────────┐
│  TOKENS SAVED          ████████ 75% │
│  TECHNICAL ACCURACY    ████████ 100%│
│  SPEED INCREASE        ████████ ~3x │
│  VIBES                 ████████ OOG │
└─────────────────────────────────────┘
```

- **Faster response** — less token to generate = speed go brrr
- **Easier to read** — no wall of text, just the answer
- **Same accuracy** — all technical info kept, only fluff removed ([science say so](https://arxiv.org/abs/2604.00025))
- **Save money** — ~71% less output token = less cost
- **Fun** — every code review become comedy

## Install

Pick your agent. One command. Done.

| Agent | Install |
|-------|---------|
| **Claude Code** | `claude plugin marketplace add JuliusBrussee/caveman && claude plugin install caveman@caveman` |
| **Codex** | Clone repo → `/plugins` → Search "Caveman" → Install |
| **Gemini CLI** | `gemini extensions install https://github.com/JuliusBrussee/caveman` |
| **Cursor** | `npx skills add JuliusBrussee/caveman -a cursor` |
| **Windsurf** | `npx skills add JuliusBrussee/caveman -a windsurf` |
| **Copilot** | `npx skills add JuliusBrussee/caveman -a github-copilot` |
| **Cline** | `npx skills add JuliusBrussee/caveman -a cline` |
| **Any other** | `npx skills add JuliusBrussee/caveman` |

Install once. Use in every session for that install target after that. One rock. That it.

### What You Get

Auto-activation is built in for Claude Code, Gemini CLI, and the repo-local Codex setup below. `npx skills add` installs the skill for other agents, but does **not** install repo rule/instruction files, so Caveman does not auto-start there unless you add the always-on snippet below.

| Feature | Claude Code | Codex | Gemini CLI | Cursor | Windsurf | Cline | Copilot |
|---------|:-----------:|:-----:|:----------:|:------:|:--------:|:-----:|:-------:|
| Caveman mode | Y | Y | Y | Y | Y | Y | Y |
| Auto-activate every session | Y | Y¹ | Y | —² | —² | —² | —² |
| `/caveman` command | Y | Y¹ | Y | — | — | — | — |
| Mode switching (lite/full/ultra) | Y | Y¹ | Y | Y³ | Y³ | — | — |
| Statusline badge | Y⁴ | — | — | — | — | — | — |
| caveman-commit | Y | — | Y | Y | Y | Y | Y |
| caveman-review | Y | — | Y | Y | Y | Y | Y |
| caveman-compress | Y | Y | Y | Y | Y | Y | Y |
| caveman-help | Y | — | Y | Y | Y | Y | Y |

> [!NOTE]
> Auto-activation works differently per agent: Claude Code uses SessionStart hooks, this repo's Codex dogfood setup uses `.codex/hooks.json`, Gemini uses context files. Cursor/Windsurf/Cline/Copilot can be made always-on, but `npx skills add` installs only the skill, not the repo rule/instruction files.
>
> ¹ Codex uses `$caveman` syntax, not `/caveman`. This repo ships `.codex/hooks.json`, so caveman auto-starts when you run Codex inside this repo. The installed plugin itself gives you `$caveman`; copy the same hook into another repo if you want always-on behavior there too. caveman-commit and caveman-review are not in the Codex plugin bundle — use the SKILL.md files directly.
> ² Add the "Want it always on?" snippet below to those agents' system prompt or rule file if you want session-start activation.
> ³ Cursor and Windsurf receive the full SKILL.md with all intensity levels. Mode switching works on-demand via the skill; no slash command.
> ⁴ Available in Claude Code, but plugin install only nudges setup. Standalone `install.sh` / `install.ps1` configures it automatically when no custom `statusLine` exists.

<details>
<summary><strong>Claude Code — full details</strong></summary>

The plugin install gives you skills + auto-loading hooks. If no custom `statusLine` is configured, Caveman nudges Claude to offer badge setup on first session.

```bash
claude plugin marketplace add JuliusBrussee/caveman
claude plugin install caveman@caveman
```

**Standalone hooks (without plugin):** If you prefer not to use the plugin system:
```bash
# macOS / Linux / WSL
bash <(curl -s https://raw.githubusercontent.com/JuliusBrussee/caveman/main/hooks/install.sh)

# Windows (PowerShell)
irm https://raw.githubusercontent.com/JuliusBrussee/caveman/main/hooks/install.ps1 | iex
```

Or from a local clone: `bash hooks/install.sh` / `powershell -File hooks\install.ps1`

Uninstall: `bash hooks/uninstall.sh` or `powershell -File hooks\uninstall.ps1`

**Statusline badge:** Shows `[CAVEMAN]`, `[CAVEMAN:ULTRA]`, etc. in your Claude Code status bar.

- **Plugin install:** If you do not already have a custom `statusLine`, Claude should offer to configure it on first session
- **Standalone install:** Configured automatically by `install.sh` / `install.ps1` unless you already have a custom statusline
- **Custom statusline:** Installer leaves your existing statusline alone. See [`hooks/README.md`](hooks/README.md) for the merge snippet

</details>

<details>
<summary><strong>Codex — full details</strong></summary>

**macOS / Linux:**
1. Clone repo → Open Codex in the repo directory → `/plugins` → Search "Caveman" → Install

**Windows:**
1. Enable symlinks first: `git config --global core.symlinks true` (requires Developer Mode or admin)
2. Clone repo → Open VS Code → Codex Settings → Plugins → find "Caveman" under local marketplace → Install → Reload Window

This repo also ships `.codex/hooks.json`, so caveman auto-activates while you run Codex inside this repo. The installed plugin gives you `$caveman`; if you want always-on behavior in other repos too, add the same SessionStart hook there.

</details>

<details>
<summary><strong>Gemini CLI — full details</strong></summary>

```bash
gemini extensions install https://github.com/JuliusBrussee/caveman
```

Update: `gemini extensions update caveman` · Uninstall: `gemini extensions uninstall caveman`

Auto-activates via `GEMINI.md` context file. Also ships custom Gemini commands:
- `/caveman` — switch intensity level (lite/full/ultra/wenyan)
- `/caveman-commit` — generate terse commit message
- `/caveman-review` — one-line code review

</details>

<details>
<summary><strong>Cursor / Windsurf / Cline / Copilot — full details</strong></summary>

`npx skills add` installs the skill file only — it does **not** install the agent's rule/instruction file, so caveman does not auto-start. For always-on, add the "Want it always on?" snippet below to your agent's rules or system prompt.

| Agent | Command | Not installed | Mode switching | Always-on location |
|-------|---------|--------------|:--------------:|--------------------|
| Cursor | `npx skills add JuliusBrussee/caveman -a cursor` | `.cursor/rules/caveman.mdc` | Y | Cursor rules |
| Windsurf | `npx skills add JuliusBrussee/caveman -a windsurf` | `.windsurf/rules/caveman.md` | Y | Windsurf rules |
| Cline | `npx skills add JuliusBrussee/caveman -a cline` | `.clinerules/caveman.md` | — | Cline rules or system prompt |
| Copilot | `npx skills add JuliusBrussee/caveman -a github-copilot` | `.github/copilot-instructions.md` + `AGENTS.md` | — | Copilot custom instructions |

Uninstall: `npx skills remove caveman`

Copilot works with Chat, Edits, and Coding Agent.

</details>

<details>
<summary><strong>Any other agent (opencode, Roo, Amp, Goose, Kiro, and 40+ more)</strong></summary>

[npx skills](https://github.com/vercel-labs/skills) supports 40+ agents:

```bash
npx skills add JuliusBrussee/caveman           # auto-detect agent
npx skills add JuliusBrussee/caveman -a amp
npx skills add JuliusBrussee/caveman -a augment
npx skills add JuliusBrussee/caveman -a goose
npx skills add JuliusBrussee/caveman -a kiro-cli
npx skills add JuliusBrussee/caveman -a roo
# ... and many more
```

Uninstall: `npx skills remove caveman`

> **Windows note:** `npx skills` uses symlinks by default. If symlinks fail, add `--copy`: `npx skills add JuliusBrussee/caveman --copy`

**Important:** These agents don't have a hook system, so caveman won't auto-start. Say `/caveman` or "talk like caveman" to activate each session.

**Want it always on?** Paste this into your agent's system prompt or rules file — caveman will be active from the first message, every session:

```
Terse like caveman. Technical substance exact. Only fluff die.
Drop: articles, filler (just/really/basically), pleasantries, hedging.
Fragments OK. Short synonyms. Code unchanged.
Pattern: [thing] [action] [reason]. [next step].
ACTIVE EVERY RESPONSE. No revert after many turns. No filler drift.
Code/commits/PRs: normal. Off: "stop caveman" / "normal mode".
```

Where to put it:
| Agent | File |
|-------|------|
| opencode | `.config/opencode/AGENTS.md` |
| Roo | `.roo/rules/caveman.md` |
| Amp | your workspace system prompt |
| Others | your agent's system prompt or rules file |

</details>

## Usage

Trigger with:
- `/caveman` or Codex `$caveman`
- "talk like caveman"
- "caveman mode"
- "less tokens please"

Stop with: "stop caveman" or "normal mode"

### Intensity Levels

| Level | Trigger | What it do |
|-------|---------|------------|
| **Lite** | `/caveman lite` | Drop filler, keep grammar. Professional but no fluff |
| **Full** | `/caveman full` | Default caveman. Drop articles, fragments, full grunt |
| **Ultra** | `/caveman ultra` | Maximum compression. Telegraphic. Abbreviate everything |

### 文言文 (Wenyan) Mode

Classical Chinese literary compression — same technical accuracy, but in the most token-efficient written language humans ever invented.

| Level | Trigger | What it do |
|-------|---------|------------|
| **Wenyan-Lite** | `/caveman wenyan-lite` | Semi-classical. Grammar intact, filler gone |
| **Wenyan-Full** | `/caveman wenyan` | Full 文言文. Maximum classical terseness |
| **Wenyan-Ultra** | `/caveman wenyan-ultra` | Extreme. Ancient scholar on a budget |

Level stick until you change it or session end.

## Caveman Skills

| Skill | What it do | Trigger |
|-------|-----------|---------|
| **caveman-commit** | Terse commit messages. Conventional Commits. ≤50 char subject. Why over what. | `/caveman-commit` |
| **caveman-review** | One-line PR comments: `L42: 🔴 bug: user null. Add guard.` No throat-clearing. | `/caveman-review` |
| **caveman-help** | Quick-reference card. All modes, skills, commands, one command away. | `/caveman-help` |

### caveman-compress

Caveman make Claude *speak* with fewer tokens. **Compress** make Claude *read* fewer tokens.

Your `CLAUDE.md` loads on **every session start**. Caveman Compress rewrites memory files into caveman-speak so Claude reads less — without you losing the human-readable original.

```
/caveman:compress CLAUDE.md
```

```
CLAUDE.md          ← compressed (Claude reads this every session — fewer tokens)
CLAUDE.original.md ← human-readable backup (you read and edit this)
```

| File | Original | Compressed | Saved |
|------|----------:|----------:|------:|
| `claude-md-preferences.md` | 706 | 285 | **59.6%** |
| `project-notes.md` | 1145 | 535 | **53.3%** |
| `claude-md-project.md` | 1122 | 636 | **43.3%** |
| `todo-list.md` | 627 | 388 | **38.1%** |
| `mixed-with-code.md` | 888 | 560 | **36.9%** |
| **Average** | **898** | **481** | **46%** |

Code blocks, URLs, file paths, commands, headings, dates, version numbers — anything technical passes through untouched. Only prose gets compressed. See the full [caveman-compress README](caveman-compress/README.md) for details. [Security note](./caveman-compress/SECURITY.md): Snyk flags this as High Risk due to subprocess/file patterns — it's a false positive.

## Benchmarks

Real token counts from the Claude API ([reproduce it yourself](benchmarks/)):

<!-- BENCHMARK-TABLE-START -->
| Task | Normal (tokens) | Caveman (tokens) | Saved |
|------|---------------:|----------------:|------:|
| Explain React re-render bug | 1180 | 159 | 87% |
| Fix auth middleware token expiry | 704 | 121 | 83% |
| Set up PostgreSQL connection pool | 2347 | 380 | 84% |
| Explain git rebase vs merge | 702 | 292 | 58% |
| Refactor callback to async/await | 387 | 301 | 22% |
| Architecture: microservices vs monolith | 446 | 310 | 30% |
| Review PR for security issues | 678 | 398 | 41% |
| Docker multi-stage build | 1042 | 290 | 72% |
| Debug PostgreSQL race condition | 1200 | 232 | 81% |
| Implement React error boundary | 3454 | 456 | 87% |
| **Average** | **1214** | **294** | **65%** |

*Range: 22%–87% savings across prompts.*

> **Fork note (not a new measurement).** The percentages in the table above are upstream wording kept verbatim. In this checkout, `benchmarks/results/` contains `.gitkeep` only (filename listing). Result JSON was not opened and `benchmarks/run.py` was not run. This documentary lot does not certify the "65%" average, the 22%–87% range, or any other token saving.
<!-- BENCHMARK-TABLE-END -->

> [!IMPORTANT]
> Caveman only affects output tokens — thinking/reasoning tokens are untouched. Caveman no make brain smaller. Caveman make *mouth* smaller. Biggest win is **readability and speed**, cost savings are a bonus.

A March 2026 paper ["Brevity Constraints Reverse Performance Hierarchies in Language Models"](https://arxiv.org/abs/2604.00025) found that constraining large models to brief responses **improved accuracy by 26 percentage points** on certain benchmarks and completely reversed performance hierarchies. Verbose not always better. Sometimes less word = more correct.

## Evals

Caveman not just claim 75%. Caveman **prove** it.

> **Fork note.** The word "prove" above is upstream wording. This lot did not run `evals/`. `evals/snapshots/results.json` is present and was not opened. The sentence is not a certified result for this fork.

The `evals/` directory has a three-arm eval harness that measures real token compression against a proper control — not just "verbose vs skill" but "terse vs skill". Because comparing caveman to verbose Claude conflate the skill with generic terseness. That cheating. Caveman not cheat.

```bash
# Run the eval (needs claude CLI)
uv run python evals/llm_run.py

# Read results (no API key, runs offline)
uv run --with tiktoken python evals/measure.py
```

## Star This Repo

If caveman save you mass token, mass money — leave mass star. ⭐

[![Star History Chart](https://api.star-history.com/svg?repos=JuliusBrussee/caveman&type=Date)](https://star-history.com/#JuliusBrussee/caveman&Date)

## Also by Julius Brussee

- **[Cavekit](https://github.com/JuliusBrussee/cavekit)** — specification-driven development for Claude Code. Caveman language → specs → parallel builds → working software.
- **[Revu](https://github.com/JuliusBrussee/revu-swift)** — local-first macOS study app with FSRS spaced repetition, decks, exams, and study guides. [revu.cards](https://revu.cards)

## License

MIT — free like mass mammoth on open plain.
