# # Docker-команда FROM вказує базовий образ контейнера
# # Наш базовий образ - це Linux з попередньо встановленим python-3.10
FROM python:3.10

# # Встановимо робочу директорію всередині контейнера
WORKDIR /app

# Скопіюйте файли pyproject.toml та poetry.lock
COPY pyproject.toml poetry.lock /app/

# Встановимо poetry та налаштування для створення віртуального середовища
RUN pip install poetry
RUN poetry config virtualenvs.create false

# Скопіюйємо всі інші файли у контейнер
COPY . /app/

# Вказуємо правильний шлях до файлу
CMD ["python", "Assistent/Menu_project.py"]















# # Docker-команда FROM вказує базовий образ контейнера
# # Наш базовий образ - це Linux з попередньо встановленим python-3.10
# FROM python:3.10

# # Встановимо змінну середовища
# ENV APP_HOME /

# # Встановимо робочу директорію всередині контейнера
# WORKDIR $APP_HOME

# COPY  pyproject.toml $APP_HOME/pyproject.toml
# COPY poetry.lock $APP_HOME/poetry.lock


# # Встановимо залежності всередині контейнера
# RUN pip install poetry
# RUN poetry config virtualenvs.create false 
# # RUN poetry install --only main


# # Скопіюємо інші файли в робочу директорію контейнера
# COPY .  .

# # Позначимо порт, де працює застосунок всередині контейнера
# EXPOSE 5000

# # Запустимо наш застосунок всередині контейнера
# CMD ["python", "Assistent/Menu_project.py"]