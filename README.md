# Grok-Commit: AI-Powered Git Commit Messages Using Grok API

This is a simple Ruby CLI tool that generates concise Git commit messages using the xAI Grok API (e.g., Grok-3 model). It analyzes your staged changes (git diff --cached), sends them to the API, generates a message in Conventional Commits format (e.g., "feat: adds new feature"), and automatically commits them.
Features

Automatic commit message generation in English.
Uses xAI's Grok API for intelligent summaries.
Limits diff size to avoid token overuse.
Handles errors gracefully (e.g., no staged changes, API failures).

Prerequisites

Ruby 2.7+ (installed on most Unix systems; check with ruby -v).
Git installed.# Grok-Commit: AI-Powered Git Commit Messages Using Grok API

This is a simple Ruby CLI tool that generates concise Git commit messages using the xAI Grok API (e.g., Grok-3 model). It analyzes your staged changes (`git diff --cached`), sends them to the API, generates a message in Conventional Commits format (e.g., "feat: adds new feature"), and automatically commits them.

## Features

- Automatic commit message generation in English.
- Uses xAI's Grok API for intelligent summaries.
- Limits diff size to avoid token overuse.
- Handles errors gracefully (e.g., no staged changes, API failures).

## Prerequisites

- Ruby 2.7+ (installed on most Unix systems; check with `ruby -v`).
- Git installed.
- An xAI API key (obtain from https://console.x.ai; requires credits or subscription).
- Access to a terminal (Linux/macOS recommended; Windows may need adjustments).

## Installation

1. **Download the Repository:**

- Clone or download from GitHub:

```bash
git clone https://github.com/your-username/grok-commit.git
cd grok-commit
```

1. **Set Up the Script:**

- Copy the script to a global bin directory (e.g., `/usr/local/bin` for system-wide access):

```bash
sudo cp grok-commit /usr/local/bin/
```

- Set permissions to 766 (owner/group execute/read/write, others read/write):

```bash
sudo chmod 766 /usr/local/bin/grok-commit
```

*Note: 766 is unusual for executables (755 is standard). Use with caution, as it allows group/others to write.*

1. **Set Your API Key:**

- Add to your shell profile (e.g., `~/.bashrc` or `~/.zshrc`):

```bash
export GROK_API_KEY="your-xai-api-key-here"
```

- Reload your shell:

```bash
source ~/.bashrc
```

1. **Set Your LANGUAGE:**
   - Add to your shell profile (e.g., `~/.bashrc` or `~/.zshrc`):
   - Examples: en, pt-BR...

```bash
export GROK_COMMIT_LANGUAGE="en"
```

- Reload your shell:

```bash
source ~/.bashrc
```

1. **Test Installation:**

- Run `grok-commit` in a Git repo with staged changes. It should generate and commit automatically.

## Usage

1. In a Git repository, stage your changes:

```bash
git add .
grok-commit
```

- It will generate a message like `feat: update vehicle location job`

## Troubleshooting

- **No staged changes:** Add files with `git add`.
- **API Key Error:** Verify with `echo $GROK_API_KEY` and ensure credits in https://console.x.ai.
- **API Errors (e.g., 500):** Check xAI status at https://status.x.ai or try model 'grok-4' in the script.
- **Commit Fails:** Ensure Git is configured (`git config --global user.name/email`).
- **Large Diffs:** The script limits to 5,000 chars; for bigger, edit manually.

## Customization

- Edit `grok-commit` to change the model (e.g., 'grok-4'), prompt language, or add features like confirmation prompts.
- Costs: ~$0.0004 per call with Grok-3 (monitor in xAI console).

## License

MIT License. Feel free to fork and contribute!

## Contributing

Pull requests welcome! Open issues for bugs or features.
An xAI API key (obtain from https://console.x.ai; requires credits or subscription).
Access to a terminal (Linux/macOS recommended; Windows may need adjustments).

Installation

Download the Repository:

Fork, clone and download from GitHub:

```bash
git clone https://github.com/your-username/grok-commit.git
cd grok-commit
```

Set Up the Script:

Copy the script to a global bin directory (e.g., /usr/local/bin for system-wide access):

```bash
sudo cp grok-commit /usr/local/bin/
```

Set permissions to 766 (owner/group execute/read/write, others read/write):

```bash
sudo chmod 766 /usr/local/bin/grok-commit
```

Note: 766 is unusual for executables (755 is standard). Use with caution, as it allows group/others to write.

Set Your API Key:

Add to your shell profile (e.g., ~/.bashrc or ~/.zshrc):

```
export GROK_API_KEY="your-xai-api-key-here"
export GROK_COMMIT_LANGUAGE="en"
```

Reload your shell:

```bash
source ~/.bashrc
```

Test Installation:

Run grok-commit in a Git repo with staged changes. It should generate and commit automatically.

Usage

In a Git repository, stage your changes:

```bash
git add .
grok-commit
```

It will generate a message like feat: update vehicle location job, commit it, and output "Commit successful!".

Troubleshooting

No staged changes: Add files with git add.
API Key Error: Verify with echo $GROK_API_KEY and ensure credits in https://console.x.ai.
API Errors (e.g., 500): Check xAI status at https://status.x.ai or try model 'grok-4' in the script.
Commit Fails: Ensure Git is configured (git config --global user.name/email).
Large Diffs: The script limits to 5,000 chars; for bigger, edit manually.

Customization

Edit grok-commit to change the model (e.g., 'grok-4'), prompt language, or add features like confirmation prompts.
Costs: ~$0.0004 per call with Grok-3 (monitor in xAI console).

License
MIT License. Feel free to fork and contribute!
Contributing
Pull requests welcome! Open issues for bugs or features.