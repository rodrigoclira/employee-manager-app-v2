[![Django Continuous Integration](https://github.com/rodrigoclira/employee-manager-app-v2/actions/workflows/django.yml/badge.svg)](https://github.com/rodrigoclira/employee-manager-app-v2/actions/workflows/django.yml)

# Employee Manager Application (Frontend + Backend)

Esse repositório baseia-se em https://github.com/rodrigoclira/employee-manager-app-v1 . Na versão v2 do repositório foi adicionada uma aplicação de frontend para acessar a API disponibilizada com DRF. Sendo assim duas aplicações são inicializadas por _containers_ docker, a _frontend_ e a _backend_.

Ambas as aplicações podem ser inicializadas usando o comando abaixo
```
sudo docker-compose up --build
```


![image](https://user-images.githubusercontent.com/276077/174942615-b4e7e945-2d89-4c23-836e-9ab8931b5ed3.png)


A aplicação de _frontend_ fica disponível na porta 8000

![image](https://user-images.githubusercontent.com/276077/174942679-b3aa5eaa-ab51-4c51-aa21-36f55fb13a49.png)



Ela se comunica com a aplicação de backend que está disponível na porta 8001

![image](https://user-images.githubusercontent.com/276077/174942952-37e7e1f6-75b8-4db0-ba93-87933617a63e.png)


Na aplicação de _frontend_ apenas os endpoints GET /employee e o GET /employee/ID da API estão sendo utilizados. 
Todas as views que utilizam esses endpoints estão implementadas no arquivo _views.py_ do app _web_, como exibido na imagem abaixo.

![image](https://user-images.githubusercontent.com/276077/174943242-8d6cd8ff-691f-45bb-846e-0e029004bc00.png)

Navegue na aplicação disponível na porta 8000 (_frontend_) e avalie o código dela. 

![image](https://user-images.githubusercontent.com/276077/175022904-fbe4d379-0fc8-4ce0-8e5e-9d55171e1921.png)


Para finalizar as aplicações inicializadas com o _docker-compose_, utilize o comando abaixo:

```
sudo docker-compose down
```

ou ```CTRL+C```

----- 

## Referência

https://medium.com/@nutanbhogendrasharma/consume-rest-api-in-django-web-application-130c0daa6f70

https://docs.djangoproject.com/en/4.0/topics/cache/

https://github.com/rodrigoclira/devweb2/tree/main/caching#exemplo-de-cache-de-baixo-n%C3%ADvel
