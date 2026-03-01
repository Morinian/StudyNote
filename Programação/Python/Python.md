## Plataforma do Python

- PRL : Python Language Reference - O primeiro e mais importante componente é a PLR (Python Language Reference) que é o documento contendo toda a especificação da linguagem, aqui estão as regras gramaticais da linguagem, aqui estão as palavras reservadas e todos os comportamentos esperados de uma implementação de Python, PLR é um extenso conjunto de textos escrito pelo criador do Python.
- Código de conduta
![[implementaçãoPython.png]]
### PSF

A Python Software Foundation é a fundação internacional criada para proteger e gerir os recursos e direitos do Python, a linguagem é open-source e livre não existe uma empresa dona do Python, porém existe uma fundação oficial que faz a gestão de coisas como copyright da marca Python, avaliação de propostas de melhoria para a linguagem e apoio a comunidades locais.

### PyPI

O Python Package Index é um repositório com mais de 300 mil pacotes e ferramentas para você reutilizar em seus projetos Python, esta infraestrutura é mantida por um sub grupo da PSF chamado Python Package Authority e é através do PyPI usando a ferramenta `pip` que instalamos bibliotecas e ferramentas.

----
# Tipos em python :

![[tipospy.png]]
# Funções

## DIR

Sem argumentos retorna a lista de nomes no escopo local atual, retornando uma lista de atributos válidos para o objeto.
Tudo que vou declarando ele mostra.

```python
dir()
dir(100)
```

## Help
Invoca um sistema de ajuda integrado. É possível fazer buscas em modo interativo
```python
help()
help(100)
```