University: [SPBU](https://spbu.ru/)  
Faculty: [MM](https://math.spbu.ru/rus/)  
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)  
Year: 2022/2023  
Group: 19.Б05  
Author: Sagatdinov Artur Rinatovich  
Lab: Lab1  
Date of create: 10.12.2022  
Date of finished: 15.12.2022  

## Ответы на вопросы  
  
### 1) Что сейчас произошло и что сделали команды указанные ранее? 
- Сначала запустили minikube, с помощью команды `minikube start`.
- Далее создали кластер vault, заранее загрзив контейнер, с помощью команды `kubectl create deployment vault --image=vault`
- Получили доступ к данному объекту "извне" `kubectl expose deployment vault --type=NodePort --port=8200`
- Проверили, что все работает 
![image1](./images/image2.png)
- С помощью команды `minikube service vault --url` получили URL сервеса.

### 2. Где взять токен для входа в Vault?
- С помощью команды `kubectl logs vault`.
