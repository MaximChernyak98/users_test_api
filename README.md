# Пример тестирования API
Данный проект разработан для тестирования сервиса Users (http://users.bugred.ru/).
Проект использует python - requests - pytest.

### Подготовка окружения

1. Клонируйте репозиторий, создайте виртуальное окружение
2. Установите зависимости `pip install -r requirements.txt`
3. Находясь в папке проект совершите команду:
```pytest -v --capture=tee-sys tests\test_base_func_001.py```
    
### На данный момент реализованы 2 теста:

1) Проверяется возможность создания пользователя с уникальным email и login (уникальность через системное время)
2) Выполняется проверка невозможности создания пользователя при заполнении только поля email

### Примечание по импорту в tests\test_base_func_001.py:

Странный импорт реализован для запуска кода как из командой из пункта 3, так и из IDE (через __name__ == "__main__")
Если есть способ лучше - буду рад услышать на собеседовании:)