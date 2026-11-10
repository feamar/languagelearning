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

`I-am:` is your mother tongue: the language the tutor talks and explains in. It is not the
language you want to learn. A Dutch speaker learning Danish types `I-am:Dutch`.

You can also put `I-am:Dutch` anywhere in your first message. `I am:Dutch` works too. The language
can be a name in any language (`Dutch`, `Nederlands`, `Deutsch`) or an ISO 639-1 code (`nl`, `de`,
`es`).

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

1. Start a new chat and type your shortcut on the first line, for example `I-am:Dutch`. In
   ChatGPT, use a Temporary Chat, so that memories of earlier chats do not interfere.
2. Open [skills/language-tutor/SKILL.md](skills/language-tutor/SKILL.md), copy everything below
   the second `---` line, and paste it under your shortcut.
3. Send it. The first reply should start with a stage marker such as
   `[Stage 1 · Intake · 0/11 done · now: Q1 other languages]`, in your mother tongue, and ask
   exactly one question.

Every reply during the intake should look the same: the marker, at most one short sentence about
your answer, and the next question. If the assistant drifts, for example it starts teaching, tests
your level or stops using your language, remind it: `Follow the hard rules.`

You can also save the instructions in a Gemini Gem or a custom GPT, and start each chat with
`I-am:Dutch`. That works better than pasting, because the instructions then stay in force for the
whole chat.
