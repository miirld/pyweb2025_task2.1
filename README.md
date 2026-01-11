## Отчёт. Задание 2.1. Создание и развертывание статического сайта

> Дисциплина "Проектирование и развертывание веб-решений в эко-системе Python"

### Выполнение работы

1. Создание репозитория в github
   
<img width="1493" height="647" alt="image" src="https://github.com/user-attachments/assets/7d4b1be4-0ba0-4129-981d-432a319d6dee" />

2. Клонирование репозитория, создание и использование виртуального окружения

<img width="1494" height="896" alt="image" src="https://github.com/user-attachments/assets/a7afa4d4-d9c1-40a4-ac79-a6edfbc1c2bf" />

3. Создание проекта с помощью mkdocs

<img width="1500" height="855" alt="image" src="https://github.com/user-attachments/assets/fc970599-5725-4e0f-bace-e35654a26628" />

4. Наполнение сайта контентом

<img width="1496" height="761" alt="image" src="https://github.com/user-attachments/assets/911b8181-3812-42b5-8154-76d2cd4870f0" />

5. Сборка статического сайта

<img width="1492" height="896" alt="image" src="https://github.com/user-attachments/assets/44df63b9-f7bf-402d-9abc-5d2566cce79d" />

6. Деплой сайта на github pages вручную (mkdocs gh-deploy)

<img width="1498" height="720" alt="image" src="https://github.com/user-attachments/assets/dac79d8e-68d5-4870-b36c-587d6ddca437" />

7. Демонстрация сайта, опубликованного вручную

<img width="1497" height="775" alt="image" src="https://github.com/user-attachments/assets/7c1a047d-5534-4844-9607-90ecfbceaac9" />

8. Перевод github pages на деплой source github actions
   
<img width="1504" height="733" alt="image" src="https://github.com/user-attachments/assets/734821ba-0112-4237-af4d-3fe43e159dfa" />

9. Создание github actions workflow для автоматического деплоя на github pages при пуше в main

<img width="1493" height="893" alt="image" src="https://github.com/user-attachments/assets/2a9593b2-887e-403d-8a61-c5eda71b0b92" />

10. Добавление доп. контента на сайт для проверки актуальности

<img width="1498" height="898" alt="image" src="https://github.com/user-attachments/assets/7b4b2a4f-4dff-4f9a-bf25-f0e1c5d9d364" />

11. Выполнение github action

<img width="1494" height="722" alt="image" src="https://github.com/user-attachments/assets/ccfa140c-1cdc-4a5d-97b6-68e209b1aba1" />

12. Запись в deployments

<img width="1498" height="718" alt="image" src="https://github.com/user-attachments/assets/965f7514-4224-4f41-a7db-36f9e1290d52" />

13. Автоматически опубликованная актуальная версия сайта с тестовым доп. контентом

<img width="1499" height="768" alt="image" src="https://github.com/user-attachments/assets/169c1535-213d-4a7c-a89e-b9a77a695412" />

### Исследование

1. Возможности использования отечественных CDN для ускорения доставки контента.
   
На отечественном рынке предоставление CDN является распространенной услугой. 
Существуют как специализированные платформы: Ngenix, EdgeЦентр.
Так и провайдеры, которые предоставляют CDN как доп. услугу: Yandex Cloud, Selectel, Cloud.ru и др.

2. Возможности Gitverse для реализации CI/CD.
   
Gitverse поддерживает GitVerse Actions, схожие с GitHub Actions.
Конфигурационные yaml файлы GitVerse Actions должны располагаться в директории .gitverse/workflows/ репозитория (аналогично GitHub).

3. Какие существуют варианты деплоя статического сайта в продакшен среду и какие технические инструменты для этого могут потребоваться, приведите примеры.

**Ручной деплой.** Передача файлов результата сборки на сервер вручную с помощью FTP/SFTP-клиентов, таких как FileZilla или WinSCP. Как правило, разработчик запускает сборку локально и затем копирует папку dist или build на сервер.

**Деплой через Git.** Ряд хостинг-платформ умеют автоматически отслеживать изменения в выбранной ветке репозитория, забирать код, выполнять сборку и выкладывать приложение без ручного вмешательства. Пример: Vercel, Netlify.

**Деплой через CI/CD пайплайн.** Настраивается автоматизированный конвейер, который при каждом коммите или мерже в репозиторий последовательно запускает тесты, сборку и деплой проекта. Примеры инструментов: GitHub Actions, GitLab CI/CD (позволяют описывать пайплайны в виде конфигурационных файлов и скриптов).







