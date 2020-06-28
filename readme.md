# Bash Preprocessor: replace snippets with their output


## Example

```bash
#!/bin/bash

@@@START@@@
echo "# Build date: $(date)"
@@@END@@@

echo "Hello World!"
```

By running the preprocessor on this file, the code between `@@@START@@@` and `@@@END@@@` will be executed and replaced by its output.

```bash
#!/bin/bash

# Build date: Sun Jun 28 15:31:07 CEST 2020

echo "Hello World!"
```

## Usage

1. Get `preprocess.sh`:
    - grab and extract a [release](https://github.com/dodie/bash-preprocessor/releases)
    - clone this repository
    - simply copy `preprocess.sh`

2. Run the script to preprocess a file (it will change its contents in place):
    ```
    ./preprocess.sh <path-to-file>
    ```

If needed the `@@@START@@@` and `@@@END@@@` tokens can be customized with an optional 2nd and 3rd argument:
```
./preprocess.sh <path-to-file> "<custom start token>" "<custom end token>"
```

