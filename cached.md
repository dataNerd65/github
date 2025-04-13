## Removing cached files
```bash
git rm --cached file_name

# multiple similar files 
git rm -- cached *.out *.exe *.o

# multiple dirs
git rm --cached -r pracoo/ .vscode/
```

## Removing a staged file
```cpp
git restore --staged pracoo
```
