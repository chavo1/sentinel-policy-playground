# This repo contains a sample sentinel policies

## Requirements 

- Install [Sentinel](https://docs.hashicorp.com/sentinel/downloads/)

### How to use it:

```
$sentinel test policy.sentinel
PASS - policy.sentinel
  PASS - test/policy/9-am.json
  PASS - test/policy/good.json
```

### Change the rule to 10 and it should fail

```
sentinel test policy.sentinel
FAIL - policy.sentinel
  FAIL - test/policy/9-am.json
    expected "main" to be true, got: false

    trace:
      policy.sentinel:3:1 - Rule "main"
        Value:
          false

    legacy warning:
      test case uses legacy config, please migrate it to an HCL configuration.
  FAIL - test/policy/good.json

    trace:
      policy.sentinel:3:1 - Rule "main"
        Value:
          false

    legacy warning:
      test case uses legacy config, please migrate it to an HCL configuration.
```
