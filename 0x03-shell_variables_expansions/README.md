# 0x03. Shell, init files, variables and expansions

This project focuses on understanding how shell variables, environment variables, expansions, and other Bash features work. Each task explores specific commands and shell behaviors.

## Tasks

### 0. <o>
**File:** `0-alias`  
Creates an alias `ls` that deletes all files in the current directory.  
```bash
alias ls='rm *'
```

---

### 1. Hello you
**File:** `1-hello_you`  
Prints `hello` followed by the current Linux user.  
```bash
echo "hello $(whoami)"
```

---

### 2. The path to success is to take massive, determined action
**File:** `2-path`  
Adds `/action` to the end of the `PATH` environment variable.

---

### 3. If the path be beautiful, let us not ask where it leads
**File:** `3-paths`  
Counts the number of directories in the current `$PATH` using `tr` and `wc -l`.

---

### 4. Global variables
**File:** `4-global_variables`  
Lists all the environment variables using `printenv`.

---

### 5. Local variables
**File:** `5-local_variables`  
Lists all local variables, environment variables, and functions using `set`.

---

### 6. Local variable
**File:** `6-create_local_variable`  
Creates a local variable named `BEST` with value `School`.

---

### 7. Global variable
**File:** `7-create_global_variable`  
Creates a global variable named `BEST` with value `School` using `export`.

---

### 8. Every addition to true knowledge is an addition to human power
**File:** `8-true_knowledge`  
Prints the result of `128 + $TRUEKNOWLEDGE`.

---

### 9. Divide and rule
**File:** `9-divide_and_rule`  
Prints the result of `$POWER` divided by `$DIVIDE`.

---

### 10. Love is anterior to life...
**File:** `10-love_exponent_breath`  
Prints `$BREATH` raised to the power of `$LOVE` using `**`.

---

### 11. There are 10 types of people...
**File:** `11-binary_to_decimal`  
Converts a binary number stored in `$BINARY` to decimal.

---

### 12. Combination
**File:** `12-combinations`  
Prints all possible 2-letter lowercase combinations, excluding `oo`.

---

### 13. Floats
**File:** `13-print_float`  
Prints a number with 2 decimal places from the variable `$NUM` using `printf`.

---

## Notes

- All scripts use `/bin/bash`
- All scripts are exactly 2 lines long
- No use of `awk`, `sed`, `bc`, `&&`, or `||`
- Line endings are Unix-style (LF)
- Tested on Ubuntu 20.04 LTS
