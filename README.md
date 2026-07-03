# What is this?

Anthropic can't fucking bother to actually fix any VS Code extenion bugs people file. They'll let Claude close them "because they're stale" but they won't let it just fucking fix shit. They literally own Claude, they could fix all the issues in less than a day if they even remotely bothered, but no: fuck the user, why spend time on something that makes life better for them?

So: fuck it, I made Claude fix the shit Anthropic can't be bothered to.

## How to apply them:

Tell your LLM to read through `patch-instructions.md` and do what it says.

## What got improved:

### 1. rip out the stupid "whimsy terms while thinking" bullshit.

- the word is "working". It's also the _only_ word.
- there is no animated whimsy spinner.
- there is no "cursor writing the text", just fucking show you're still working.

| |
| --- |
| <img width="1057" height="403" alt="Image" src="https://github.com/user-attachments/assets/1be4a1e6-10e6-4931-a8f8-ead98c38f1e0" /> |

### 2. Add in proper syntax highlighting for code blocks.

| before | after |
|--|--|
| <img width="705" height="398" alt="Image" src="https://github.com/user-attachments/assets/fcedce5e-12a9-4efc-accd-f64483a97184" /> |<img width="538" height="478" alt="Image" src="https://github.com/user-attachments/assets/ec079814-9161-4b00-81d0-b0a2974bfbea"> |

### 3. `/clear` preserves your prompt history.

`/clear` should wipe the LLM slate clean, it should _not_ also magically wipe your prompt history. You should be able to have it fuck up, run `/clear`, and then hit "up" a few times to restart on your original prompt. The point of clearing is to clear the LLM, not to start a completely new context-free chat. There's already a fucking option for that, it's called "new chat".

## Can you add X?

You mean "can _we_ add", because we all have access to Claude: file an issue detailing what you want to fix, and then Claude to do that work in the same way that the `patch-instructions.md` already fix a bunch of stuff (so: fix it and then update the instructions with the new fix). Then simply contribute that as a PR that fixes your issue. If Anthropic can't be bothered to fix stuff, at least we can bypass them and fix the shit they refuse to, _together_.
