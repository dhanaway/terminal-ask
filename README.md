# ask

A terminal command assistant that gives you answers, not essays.

Powered by **Gemini 3.1 Flash Lite** — responses come back near-instantly.

## What it does

```bash
$ ask how do i rename a git branch
git branch -m old-name new-name

$ ask undo last commit but keep changes
git reset --soft HEAD~1

$ ask find all png files larger than 1mb
find . -name "*.png" -size +1M

$ ask ways to check disk usage
• df -h (filesystem overview)
• du -sh * (current directory breakdown)
• ncdu (interactive explorer)
```

By default, you get just the command. Say "explain" when you want more:

```bash
$ ask explain what chmod 755 does
755 sets permissions: owner can read/write/execute (7),
group and others can read/execute (5). In binary:
rwxr-xr-x. Common for scripts and executables that
everyone should be able to run but only the owner can edit.
```

## Install

```bash
git clone https://github.com/dhanaway/terminal-agent.git
pip3 install google-genai
```

Add to your PATH:

```bash
echo 'export PATH="$HOME/terminal-agent:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

## API Key

Grab a free key from [Google AI Studio](https://aistudio.google.com/apikey), then:

```bash
echo 'export GEMINI_API_KEY="your-key"' >> ~/.zshrc
source ~/.zshrc
```

## Usage

```
ask <question>
```

That's it.
