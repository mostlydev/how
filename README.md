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

The tool can be configured in multiple ways (in order of precedence):

1. Command line arguments
2. Environment variables
3. Configuration file
4. Default values

### Configuration File

Create a `config.yaml` file in `~/.config/howdoi-cli/config.yaml`:

```yaml
provider: anthropic  # or openai
model: claude-3-5-sonnet-20241022  # or gpt-4
max_tokens: 1000
temperature: 0.7
```

### Environment Variables

```bash
export HOW_PROVIDER=anthropic
export HOW_MODEL=claude-3-5-sonnet-20241022
export HOW_MAX_TOKENS=1000
export HOW_TEMPERATURE=0.7

# API Keys
export ANTHROPIC_API_KEY=your_key_here
export OPENAI_API_KEY=your_key_here
```

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
