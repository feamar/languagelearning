# languagelearning

Een Claude-skill die samen met jou een persoonlijke, top-down taalopleiding bouwt. Claude geeft niet
meteen les. Eerst onderzoekt Claude hoe je leert, dan ontwerpt het samen met jou een leerplan, en pas
daarna begint de eerste leerfase. De lessen passen zich aan op wat je werkelijk begrijpt, onthoudt en
zelfstandig kunt toepassen.

De volledige instructie staat in [skills/taalopleiding/SKILL.md](skills/taalopleiding/SKILL.md).

## Twee versies

- `taalopleiding`: de oorspronkelijke prompt, ongewijzigd. Start alleen als je hem bij naam
  aanroept (`/languagelearning:taalopleiding`).
- `taalopleiding-moedertaal`: dezelfde prompt, met één extra stap vooraf (stap 0). Claude vraagt eerst
  naar je moedertaal, voert het hele gesprek daarin, legt de nieuwe taal uit in vergelijking met je
  moedertaal en let op fouten die je uit je moedertaal meeneemt. Bruikbaar voor leerlingen met elke
  moedertaal. Zie [skills/taalopleiding-moedertaal/SKILL.md](skills/taalopleiding-moedertaal/SKILL.md).
  Dit is de standaard: zeg je dat je een taal wilt leren, dan start Claude deze versie.

## Installeren in Claude Code

```
/plugin marketplace add feamar/languagelearning
```

```
/plugin install languagelearning@languagelearning
```

Start daarna met `/languagelearning:taalopleiding` of `/languagelearning:taalopleiding-moedertaal`,
of zeg gewoon dat je een taal wilt leren (dan start de moedertaalversie).

## Gebruiken in claude.ai of de Claude-app

Pak de map `skills/taalopleiding` (of `skills/taalopleiding-moedertaal`) in als zip-bestand en upload die onder
Settings > Capabilities > Skills.
