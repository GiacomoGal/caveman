# AGENTS.md — ingresso agenti, fork GiacomoGal/caveman

Guida di ingresso in prosa ordinaria. Non è uno stile di sessione e non è la skill.

Stessi limiti della [guida umana](README.md#guida-fork) e della [matrice](README.md#matrice). `CLAUDE.md` tiene il manuale upstream per chi modifica il prodotto, più il blocco fork in cima. Se un passo di questa pagina e il pitch del README sembrano in conflitto, vale il rango nella matrice, non la frase di marketing.

## Ordine di lettura

1. Prefazione, cifre e matrice in `README.md`.
2. Blocco «Fork checkout» in `CLAUDE.md`, poi il corpo upstream di quel file.
3. Un file di skill solo se il compito è il comportamento del prodotto e scatta il trigger scritto nel frontmatter di quel file.

## Cosa non fa questo file

- Non importa il testo delle skill con `@`. Il file precedente era solo quell'import e rendeva il prompt applicativo lo stile di ogni sessione che legge `AGENTS.md`.
- Non ordina di scrivere README, AGENTS o CLAUDE in stile cavernicolo. I file sotto `skills/`, `caveman-compress/SKILL.md` e le copie sincronizzate restano artefatti, non modificati in questo lotto.
- Non certifica un risparmio di token. «65%», «~75%», «~46%» e le altre cifre del pitch sono claim upstream, non una misura rifatta qui.
- Non deduce identità, VPS, host o uso vivo dal nome `caveman`. Inventario: fork, non archiviato, `nextdocscope=unresolved`, identità non provata, uso sconosciuto, UNMAPPED.
- Non apre segreti, env, backup, memorie, dati privati, né i path host citati in `README.md`.
- Non esegue install, hook, eval, benchmark, provider, API, SSH, sync, merge, deploy, archive.
- Non apre una PR upstream.

## Obblighi che restano

| Artefatto | Obbligo che resta | Condizione |
| --- | --- | --- |
| `skills/caveman/SKILL.md` | Prosa compressa, livelli, auto-clarity, stop con «stop caveman» o «normal mode». Codice, commit e PR in prosa normale. | Utente invoca `/caveman` o le frasi del frontmatter, oppure una copia always-on già nel tree inietta il corpo breve. Non per riscrivere le guide. |
| `skills/caveman-commit/SKILL.md` | Messaggio Conventional Commits, soggetto corto, il perché. Non esegue `git commit`. | Invocazione del commit skill. |
| `skills/caveman-review/SKILL.md` | Commento di review in una riga. Non approva e non modifica il codice. | Invocazione della review skill. |
| `skills/caveman-help/SKILL.md` | Scheda one-shot. Non cambia modo e non scrive flag. | Invocazione dell'help. |
| `caveman-compress/SKILL.md` | Comprime solo prosa nei tipi ammessi. Non tocca codice, config, env, lock, html. Non comprime `*.original.md`. | Invocazione esplicita del compress. |
| `rules/caveman-activate.md` e copie `.cursor/rules/caveman.mdc`, `.windsurf/rules/caveman.md`, `.clinerules/caveman.md`, `.github/copilot-instructions.md` | Corpo breve always-on, già nel tree. | Quegli agenti. File non modificati qui. La loro presenza non autorizza a cavernizzare questa guida. |
| `GEMINI.md` | Importa ancora le quattro skill con `@`. | Gemini CLI. File non modificato. Non è lo stile di questa guida. |
| `CLAUDE.md` corpo upstream | Sorgenti uniche, niente edit delle copie sync, hook che non bloccano la sessione, numeri di benchmark non inventati, delta eval contro terse. | Chi modifica il prodotto. |
| `LICENSE`, `CONTRIBUTING.md` | MIT, copyright Julius Brussee. Flusso di contributo descritto lì. | File non modificati. Nessuna PR upstream da questo lotto. |

Il claim «~75%» dentro il frontmatter delle skill resta nel file. Non è un risparmio verificato e non va ricopiato come fatto.

## Testo precedente di questo file

Sulla base `63e797cd753b301374947a5ed975c21775d962b9` il file conteneva solo quattro righe attive. Ogni riga era il carattere `@` seguito subito dal percorso:

1. `./skills/caveman/SKILL.md`
2. `./skills/caveman-commit/SKILL.md`
3. `./skills/caveman-review/SKILL.md`
4. `./caveman-compress/SKILL.md`

I quattro percorsi restano nella tabella sopra. Il testo dei file non è stato copiato qui. Questa citazione non reimmette quelle righe come direttive.
