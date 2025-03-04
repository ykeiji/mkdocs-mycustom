# mkdocs-mycustom

- Official links:
  - Generater: [MkDocs](https://www.mkdocs.org/)
  - Theme: [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)

## install
```python
pip install mkdocs mkdocs-material
```

## make mkdoc project
```bash
mkdocs new sampledoc
```

## start with exist config file
-> move same directory of mkdocs.yml then type build
```bash 
mkdocs build
```

## buid
```bash
mkdocs build
```
```bash
uv run mkdocs build
```
after run, generate site directory and make static files.

## run server 
```bash
mkdocs serve
```
```bash
uv run mkdocs serve
```
go to access http://127.0.0.1:8000/