# README

A perl script to interact with the Groq API using a chain-of-thought reasoning strategy.
This script sends prompts to the Groq API and receives responses.
It supports multiple rounds of thinking and can format the output using `glow` if installed.

## Installation

1. Make sure `perl` is installed on your system and is at least version `v5.14` (check with `perl -v`).
2. Set your Groq API key as an environment variable: `export GROQ_API_KEY='your_api_key_here'`.
3. Make the script executable: `chmod +x groq`
4. Optionally install [glow](https://github.com/charmbrace/glow) for formatted output.

## Example Usage

List available models:
```bash
groq --models
```

Send a query:
```bash
groq --query "What is the meaning of life?"
```

Specify a different model:
```bash
groq --query "What is the airspeed velocity of an unladen swallow?" --model "deepseek-r1-distill-llama-70b"
```

Specify the number of thinking rounds:
```bash
groq --query "What is the meaning of life?" --rounds 5
```

Pipe multiple queries:
```bash
echo -e "What is the meaning of life?\nWhat is the airspeed velocity of an unladen swallow?" | groq
```

Include a file in the prompt:
```bash
groq --query "Walk me through the behavior of this script." --file ./groq
```

## Dependencies

- Perl v5.14 or higher
- [glow](https://github.com/charmbrace/glow) (optional; for formatted output)

## Environment Variables

- `GROQ_API_KEY`: Your Groq API key.

## License

This project is licensed under the MIT License.
