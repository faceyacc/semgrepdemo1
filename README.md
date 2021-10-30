# Semgrep CLI Demo

This is a simple demo on how to run Semgrep Rules locally using Semgrep CLI commands. 

## Semgrep Rules
- Semgrep patterns are written in a Rule file writen in YAML. No complex DSL needed 😊

### To Run Rule file: 
To run a Rule file simply run the following command:

```
semgrep --config /path/to/rules.yaml main.py
```

###### Expected Output:
Output matches [pattern syntax](https://semgrep.dev/docs/writing-rules/pattern-syntax/) written in the [rule file](https://semgrep.dev/docs/writing-rules/rule-syntax/) and output custom made message. 

```
Running 1 rules...
main.py
severity:error rule:useless-eqeq: This expression is always True: `x == x` or `x != x`. If testing for floating point NaN, use `math.isnan(x)`, or `cmath.isnan(x)` if the number is complex.
2:x == x
--------------------------------------------------------------------------------
24:print(x != x)
ran 1 rules on 1 files: 2 findings
```
Rule used in this demo is open to the public and can be found in the Semgrep [Rule Registry](https://semgrep.dev/r)
