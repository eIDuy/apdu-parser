# apdu-parser

APDU-parser lets you parse your APDU commands' and APDU responses' hex bytes into their descriptions.
Project includes default APDU commands and APDU responses default lists with descriptions.

## Usage

```sh
python apdu_parser.py -i <input_file>

Options:
  -h, --help  show this help message and exit
  
  -i INPUT_FILE, --input=INPUT_FILE specify input file
  
  -o OUTPUT_FILE, --output=OUTPUT_FILE  specify output file
  
  -c, --commands  specify if input file contains only APDU commands
  
  -r, --responses specify if input file contains only APDU responses
  
  -C COMMAND_DESCRIPTIONS, --command-descriptions=COMMAND_DESCRIPTIONS  specify custom command descriptions file
  
  -R RESPONSE_DESCRIPTIONS, --response-descriptions=RESPONSE_DESCRIPTIONS specify custom response descriptions file
  
  -T, --colors	show terminal output in different colors
```
  
# Examples

Basic usage:

```sh
python apdu_parser.py -i sample_files/default_log.txt
```

Set output file:

```sh
python apdu_parser.py -i sample_files/default_log.txt -o outputs/default_log_output.txt
```

Parse every line in input file as an APDU command:

```sh
python apdu_parser.py -i sample_files/commands_log.txt -c
```

Parse every line in input file as an APDU response:

```sh
python apdu_parser.py -i sample_files/responses_log.txt -r
```

Set custom command descriptions file:

```sh
python apdu_parser.py -i sample_files/default_log.txt -C sample_files/custom_command_descriptions.txt
```

Set custom command responses file:

```sh
python apdu_parser.py -i sample_files/default_log.txt -R sample_files/custom_responses_descriptions.txt
```

Show output results in different colors in terminal (works only on Linux / MacOS):

```sh
python apdu_parser.py -i sample_files/default_log.txt -T
```

## Requirements

To properly run the apdu-parser, [Python](http://www.python.org/download/) **2.6.x** or **2.7.x** is required.