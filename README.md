# Anti-AI slop psaní v češtině

Pravidla, díky kterým AI píše český text jako člověk a nikoliv jako AI generátor. Funguje ve dvou režimech: jako krátký prompt do AI chatu (ChatGPT, Claude, Gemini, Copilot) a jako skill pro AI agenty (Claude Code, Codex, Cursor, Gemini CLI).

Inspirováno [jalaalrd/anti-ai-slop-writing](https://github.com/jalaalrd/anti-ai-slop-writing), přepracováno pro češtinu a běžné firemní použití.

## Co to řeší

AI slop je text, který vypadá správně, ale nic neříká. Zní univerzálně, používá silná slova bez důkazů, opakuje stejné větné rytmy a tváří se sebevědomě i tam, kde nemá data. Tahle pravidla ho odstraňují přes čtyři vrstvy: slovní zásobu, větné vzorce, interpunkci a formátování.

## Co balík obsahuje

| Co | K čemu je |
| --- | --- |
| `kratka-verze.md` | Krátký text ke zkopírování do AI chatu. |
| `cela-verze.md` | Plný průvodce se všemi vzorci a příklady přepisů. |
| `skill/` | Adresář se skillem pro AI agenty (`SKILL.md` + `references/`). |

## Použití

### AI chat (ChatGPT, Claude.ai, Gemini, Copilot)

Zkopíruj obsah `kratka-verze.md` a vlož ho na začátek konverzace, nebo si ho ulož jako vlastního AI asistenta: GPT v ChatGPT, Projekt v Claude, Gem v Gemini, Agent v Copilotu. Pak píše podle pravidel automaticky. Když chceš jít do hloubky, přidej `cela-verze.md`.

### Claude Code

Zkopíruj adresář se skillem do `~/.claude/skills/`:

```bash
cp -r skill ~/.claude/skills/anti-ai-slop
```

### Cursor, Codex, Gemini CLI a další

Zkopíruj obsah adresáře `skill/` (`SKILL.md` a složku `references/`) do adresáře se skilly daného nástroje. Formát SKILL.md je kompatibilní s většinou kódovacích agentů.

## Krátký prompt ke zkopírování

```text
Piš česky jako konkrétní člověk, ne jako generická AI. Drž se těchto pravidel u všeho, co píšeš.

KONKRÉTNOST
- Místo tvrzení dej příklad, místo přídavného jména dej důkaz.
- Nevymýšlej čísla, citace ani zákazníky. Když data nemáš, řekni to.

ZAKÁZANÉ VZORCE
- "V dnešní době...", "Stojí za zmínku, že...", "Pojďme se ponořit do...".
- Kontrast "nejde jen o X, ale o Y" / "není to X, je to Y". Řekni rovnou, o co jde.
- Otázka-odpověď copy: "Výsledek? Rychlost.".
- Falešné prozření: "Potvrdilo mi to jednu věc.", "Otevřelo mi to oči.".
- Ohrané metafory: "AI je kopilot, ne autopilot.", "data jsou nová ropa.".
- Falešně hluboké závěry: "Technologie sama o sobě nestačí.", "Na konci dne...".
- "Posunout na další úroveň", "odemknout potenciál", "game changer", "transformační".
- Začátky vět "Určitě,", "Samozřejmě,", "Navíc,", "Upřímně řečeno,". Začni rovnou obsahem.

RYTMUS
- Míchej délku vět, nedávej tři stejně dlouhé za sebou.
- Nedělej automaticky trojice. Žádné jednoslovné dramatické věty ("Brutální." "Tečka.").
- Žádné útržkovité nadpisy "Dvě věci, kterým se věnovat" / "Jedna hodina. Tři úkoly.".
- Odrážky jen pro skutečné seznamy.

INTERPUNKCE A FORMÁT
- Normální pomlčka (-), nikdy dlouhá pomlčka (—). Vykřičník výjimečně.
- Žádný markdown ani emoji odrážky v textu do pole bez formátování.

NA LINKEDINU NAVÍC
- Žádný háček se šipkou, žádné "Většina lidí to dělá špatně.".
- Žádná generická anekdota bez jména a detailu, nekonči "Jak to vidíte vy? 👇".

POSTOJ
- Zaujmi názor, piš pro konkrétního čtenáře a dej mu jasný další krok.

Než odpovíš, odstraň cokoliv, co by mohl napsat kdokoliv pro jakoukoliv firmu.
```

## Licence

MIT. Viz [LICENSE](LICENSE).
