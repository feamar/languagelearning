# languagelearning

A Claude skill that builds a personal, top-down language programme together with you. Claude does
not start teaching straight away. It first finds out how you learn, then designs a learning plan
with you, and only then begins the first learning phase. The lessons adapt to what you actually
understand, remember and can apply independently.

## Two versions

- `language-tutor` (default, English): the programme taught from your mother tongue.
  Claude asks for your mother tongue first, holds the whole conversation in it, explains the new
  language by comparing it with your mother tongue, and watches for mistakes you carry over from it.
  If you just say you want to learn a language, Claude starts this version.
  See [skills/language-tutor/SKILL.md](skills/language-tutor/SKILL.md).
- `taalopleiding` (original, Dutch): the original prompt, unchanged. It only starts when you call it
  by name. See [skills/taalopleiding/SKILL.md](skills/taalopleiding/SKILL.md).

## Startup shortcut: `I-am:<language>`

Tell Claude your mother tongue when you start, and it will not ask for it:

```
/languagelearning:language-tutor I-am:Dutch
```

You can also put `I-am:Dutch` anywhere in your first message. The language can be a name in any
language (`Dutch`, `Nederlands`, `Deutsch`) or an ISO 639-1 code (`nl`, `de`, `es`).

## Install in Claude Code

```
/plugin marketplace add feamar/languagelearning
```

```
/plugin install languagelearning@languagelearning
```

## Use in claude.ai or the Claude app

Zip the folder `skills/language-tutor` and upload it under Settings > Capabilities > Skills.
Then start a chat with, for example, `I want to learn Spanish. I-am:Dutch`.

## Use with other AI assistants (ChatGPT, Gemini, Le Chat, ...)

Open [skills/language-tutor/SKILL.md](skills/language-tutor/SKILL.md), copy
everything below the second `---` line, paste it as your first message, and add your shortcut
on the last line, for example `I-am:Dutch`. Or save it as custom instructions in a custom GPT or
Gemini Gem, and start each chat with `I-am:Dutch`.
