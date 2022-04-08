# How to get the last commit hash and message for a PR in Github workflow

1. Pass additional parameter `fetch-depth=0` to the checkout action as below

```yml
    steps:
      - uses: actions/checkout@v3
        with:
          fetch-depth: 2
```
2. check if triggered by Pull Request by checking the environment variable `GITHUB_REF`, if it's ending with **merge**, it means it's a PR.

3. get the hash and message of the last commit with following commands
4. 
``` bash
tmp=`git log -1 --pretty=format:%s`
tokens=( $tmp )
hash=${tokens[1]:0:7}
git log -n 1 --pretty=format:%s $hash
```