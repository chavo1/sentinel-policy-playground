# This repo contains a sample sentinel policies

## Requirements 

- Install [Sentinel](https://docs.hashicorp.com/sentinel/downloads/)
- Inspiration [Repo](https://docs.hashicorp.com/sentinel/configuration) 

### How to use it:

```
# Check if true or false
sentinel apply minimal.sentinel

# all numbers in a list are even
sentinel apply number.sentinel

# mocking working time policy
$ sentinel apply -config=config.json policy.sentinel 
Pass
$ sentinel apply -config=config.json working_time.sentinel 
Pass
# change hour or day in `config.json` and try again

# test
$ sentinel test policy.sentinel
PASS - policy.sentinel
  PASS - test/policy/7-am.json
  PASS - test/policy/good.json
```
