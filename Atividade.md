# Atividade

1. Como exibido na imagem do arquivo _views.py_, não há nenhuma estratégia de cache no app frontend. 
Use o memcached (como exibido no exemplo da aula) para adicionar uma estratégia de cache de baixo nível nas funções 'views.usuarios' e 'views.detalhes'. 
Utilize o 'json' obtido da API para ser a informação salva no cache. 

2. A aplicação de backend possui uma bateria de testes no arquivo backend/luizalabs/api/tests.py . Utilize o workflow do github (github action) para executar esse teste toda vez que o repositório for modificado. Essa abordagem vai facilitar a detecção de códigos com bugs (para ver como executar os testes, acesso o [README](https://github.com/rodrigoclira/employee-manager-app-v1) do repositório original). 
> Para mais informações de como proceder, leia [Configurando o github actions](https://cassiobotaro.dev/do_zero_a_implantacao/integracao/#configurando-o-github-actions)


Use como exemplo de arquivo abaixo. Nele ainda é necessário adicionar os comandos para executar os testes da aplicação. 

```
# This workflow will install Python dependencies, run tests and lint with a single version of Python
# For more information see: https://help.github.com/actions/language-and-framework-guides/using-python-with-github-actions
#https://hacksoft.io/github-actions-in-action-setting-up-django-and-postgres/
name: Run Backend Tests

on:
  push:
    branches:
      - master
      - main

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python 3.9
      uses: actions/setup-python@v2
      with:
        python-version: 3.9
    - name: Install dependencies
      run: |
        cd backend/
        python -m pip install --upgrade pip
        if [ -f requirements.txt ]; then pip install -r requirements.txt; fi
```

Se tudo estiver configurado corretamente, você vai ver uma imagem como abaixo ao lado do nome do projeto. 
![image](https://user-images.githubusercontent.com/276077/174945420-25ece68f-3c74-4b62-86a9-fd996300e9ec.png)

Aproveire e coloque um badge no README.md como na imagem abaixo

![image](https://user-images.githubusercontent.com/276077/174945545-81e84dfc-c56a-42c8-a368-a8f72ef2f053.png)

Para copiar o badge, você precisa ir na aba "Action" e seguir o caminho descrito na imagem abaixo. 
![image](https://user-images.githubusercontent.com/276077/174945825-dbd8f6b4-5ddc-45b9-9761-16e3c1cdd64e.png)

Por fim, salve o código do badge no README. Pronto!

> Pontuação Extra (+1 ponto)
> 
> Adicione todas as funcionalidades da API na aplicação de frontend (DELETE, PUT, POST)
