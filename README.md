# README

A Perl script to interact with the Groq API using a chain-of-thought reasoning
strategy.

## Usage

```bash
groq [options]
```

### Options

- `--help` | `-h`: Display this help message
- `--query` | `-q`: Prompt to send to the API (required)
- `--model` | `-m`: Model to use (default: deepseek-r1-distill-llama-70b)
- `--rounds` | `-r`: Number of rounds of thinking (default: 3)
- `--list-models`: List available models

## Description

This script sends prompts to the Groq API and receives responses. It supports
multiple rounds of thinking and can format the output using glow if installed.

## Installation

1. Make sure `perl` is installed on your system.
2. Ensure that `perl` is at least at version `v5.14` (`perl -v`).
3. Set your Groq API key as an environment variable:
   ```bash
   export GROQ_API_KEY='your_api_key_here'
   ```
4. Make the script executable:
   ```bash
   chmod +x groq
   ```
5. Optionally install [glow](https://github.com/charmbrace/glow) for formatted output.

## Example Usage

List available models:
```bash
./groq --list-models
```

Send a query:
```bash
./groq --query "What is the meaning of life?"
```

Specify a different model:
```bash
./groq --query "What is the airspeed velocity of an unladen swallow?" --model "deepseek-r1-distill-llama-70b"
```

Specify the number of thinking rounds:
```bash
./groq --query "What is the meaning of life?" --rounds 5
```

Pipe multiple queries:
```bash
echo -e "What is the meaning of life?\nWhat is the airspeed velocity of an unladen swallow?" | ./groq
```

## Dependencies

- Perl v5.14 or higher
- [glow](https://github.com/charmbrace/glow) (optional; for formatted output)

## Environment Variables

- `GROQ_API_KEY`: Your Groq API key.

## License

This project is licensed under the MIT License.
