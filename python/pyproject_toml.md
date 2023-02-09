# pyproject.toml 

> Packaging python code 

- Allows you put all your project configurations within one config file

- Generally put the pyproject.toml file at the same directory level as your application folder

- Other packages such as Black and pytest allow configurations to be set within the pyproject.toml file
  
Allow others to install your package locally 
> Note the e stands for editable mode
> Prevents others have to reinstall if the source code changes

```bash
python -m pip install -e .
```
