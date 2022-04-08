# test-commits-in-PR

``` bash
# get last commit message
git log -1 --pretty=%B

# get last commit hash
git log --format=%h -n1
```


The output from the workflow triggered by PR
```
Merge 862a40feb1d968dc5672b8b543f5196755460251 into d362362ce4a2e76348fb165abf0ea3e32d09405e

417371b
```

|commit # of the branch|commit message of the branch| commit # from the PR| commit message from the PR|
|---|---|---|---|
862a40feb1d968dc5672b8b543f5196755460251|3rd commit|417371b|Merge 862a40feb1d968dc5672b8b543f5196755460251 into d362362ce4a2e76348fb165abf0ea3e32d09405e

