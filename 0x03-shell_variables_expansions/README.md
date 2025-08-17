# 0x03. Shell, init files, variables and expansions

This project covers variable manipulation, expansions, and basic shell scripting principles on Ubuntu 20.04. All scripts are compliant with the following constraints:

- All scripts are exactly 2 lines long
- No usage of `&&`, `||`, `;`, `awk`, `sed`, or `bc`
- Scripts must be executable and edited using `vi`, `vim`, or `emacs`
- Each script ends with a new line

## 📜 Scripts

### `0-alias`
Creates an alias named `ls` with the value `rm *`.

### `1-hello_you`
Prints `hello` followed by the current Linux user.

### `2-path`
Adds `/action` to the end of the `PATH` environment variable.

### `3-paths`
Counts the number of directories in the current `PATH`.

### `4-global_variables`
Lists all environment variables.

### `5-local_variables`
Lists all local variables, environment variables, and functions.

### `6-create_local_variable`
Creates a new local variable `BEST` with the value `School`.

### `7-create_global_variable`
Creates a global environment variable `BEST` with the value `School`.

### `8-true_knowledge`
Prints the result of `128 + $TRUEKNOWLEDGE`, assuming TRUEKNOWLEDGE is an environment variable.

### `9-divide_and_rule`
Prints the result of `POWER / DIVIDE`, both provided via environment variables.

### `10-love_exponent_breath`
Prints `BREATH` raised to the power `LOVE`, both passed as environment variables.

### `11-binary_to_decimal`
Converts a binary number in the `BINARY` environment variable to decimal.

### `12-combinations`
Prints all 2-letter combinations from `a` to `z`, excluding `oo`. One combination per line.

### `13-print_float`
Prints a floating-point number stored in `NUM`, rounded to two decimal places.

### `100-decimal_to_hexadecimal`
Converts a decimal number (from `DECIMAL` env variable) to hexadecimal.

### `101-rot13`
Applies rot13 encryption to standard input.

### `102-odd`
Prints every other line from standard input, starting with the first.

### `103-water_and_stir`
Adds two custom base-8 encoded values (`WATER` and `STIR` from environment), and prints the result in base `bestchol`.

---

## ✅ Example Usage

```bash
chmod +x 0-alias
source ./0-alias
ls  # Actually runs `rm *` due to alias

