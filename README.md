# How Do I CLI

A simple CLI tool that explains how to use shell commands using AI models.

## Installation

```bash
# From PyPI
pip install howdoi-cli

# From source
git clone https://github.com/mostlydev/howdoi-cli
cd howdoi-cli
pip install -e .
```

## Configuration

// ... existing configuration section remains unchanged ...

## Usage

```bash
# Get help
how --help

# Basic usage - be specific about what you want to achieve
how do i extract all files from a tar.gz archive to current directory
how do i expose port 8080 for a nginx docker container
how do i list all kubernetes pods in namespace production

# The "do i" is automatically added if you forget it
how extract files from images.tar.gz to ./output

# Note: The command is also available as 'howdoi' if you prefer
howdoi extract files from images.tar.gz to ./output

# For best results:
# - Include specific file names or paths
# - Mention target directories or destinations
# - Specify ports, namespaces, or other relevant parameters
# - Include format or version information when relevant

# Examples of specific queries:
how do i find all python files modified in last 7 days
how do i create a cronjob that runs every monday at 8am
how do i configure nginx to redirect http to https on port 443

# Specify provider/model
how --provider openai --model gpt-4 do i extract files from data.tar.gz
```

## Development

1. Clone the repository
2. Create a virtual environment
3. Install development dependencies:
   ```bash
   pip install -e ".[dev]"
   ```
4. Run tests:
   ```bash
   pytest
   ```

## License

MIT
