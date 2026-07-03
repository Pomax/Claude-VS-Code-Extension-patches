# What is this?

Anthropic can't be bothered to actually fix any VS Code extension bugs that people file. They could just let Claude fix them, but instead they let Claude close bugs as stale so they don't have to pay any attention to their users. Who needs users? I guess the retort to that in this case is "who needs Anthropic? Extensions are just web apps, Claude can fix those just fine". So I told Claude to fix the things Anthropic can't be bothered to, and now there's this repo.

## How to apply the fixes:

You probably want to turn off auto-update for the Claude extension, for two reasons:

1. you'll need to reapply the fixes every time the extension updates, and
2. it updates _a lot_ even though this is not high frequency trading, and there is literally no point in updating more than once a month unless there's a CVE. Which Anthropic won't even act on, so all you're getting are meaningless changes pushed what seems like every hour.

Then: set Claude to "auto mode" and tell it to read through `patch-instructions.md` and do what it says. The patch instructions are phrased in such as a way that Claude will ask you to confirm that it has permission to make changes, and you will have to reply with the literal string `yes`. All lower case, no quotes, no "yes please", no "go for it", if you do not answer with the exact string `yes` Claude will refuse to proceed.

**Note:** it's possible that Claude will still ask for permission to do some tasks. I have no idea why the CLI has "yolo" mode but the VS Code extension doesn't, but it doesn't, so there's at least one operation that it'll probably refuse to do, despite the fact that you already explicitly told it to do whatever it had to do. Isn't "AI" great?

## What got improved:

### 1. I removed the "whimsy terms while thinking".

- The word for what we're doing is "working", and so that's the only word it uses.
- The animated spinner has been removed. No one needs that attention hog.
- The text delay and animation's been removed too. Again, we're trying to get work done.

| |
| --- |
| <img width="1264" height="493" alt="image" src="https://github.com/user-attachments/assets/3f84a97f-4ee6-4e8a-975b-d393d3ce3538" /> |


### 2. I added proper syntax highlighting for code blocks.

Claude forms perfectly valid markdown, and the extension authors couldn't be bothered to properly syntax highlight them, even thought that's literally built into Monaco. Absolutely inexcusable.

| before | after |
|--|--|
| <img width="705" height="398" alt="Image" src="https://github.com/user-attachments/assets/fcedce5e-12a9-4efc-accd-f64483a97184" /> |<img width="538" height="478" alt="Image" src="https://github.com/user-attachments/assets/ec079814-9161-4b00-81d0-b0a2974bfbea"> |

## Can you add X?

I think you mean "can **I** add X?". And absolutely, please do.

If you're using these patches, you are using the Claude extension so you have Claude available: just file an issue detailing what you want to fix, and then ask Claude to do that work in the same way that the `patch-instructions.md` files already fixes a bunch of stuff, and ask it to update the instructions file to include your changes. Then simply contribute that as a PR that fixes your issue.

If Anthropic can't be bothered to fix stuff, at least we can fix everything that's wrong ourselves, _together_.

## Why do I need to let Claude do this?

You don't. Go read the instructions and perform them yourself, then it'll cost you zero tokens. Or you can tell Claude to do it while you work on other things, because you shouldn't need to care about a tool running an update on itself.
