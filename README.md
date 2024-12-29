

This is an application that I created to work with the Ollama model and keep a history of interactions. It can answer your questions using the locally running Ollama API, and also allows you to search through saved questions using the ChromaDB database.

---

## Installation

1. First we need to install Python version 3.8 and higher.
2. Download the library specified in the folder requirements.txt
   ```bash
   pip install -r requirements.txt
   ```
3. Launching Ollama on `http://localhost:11434 `.

---

## Usage

1. Запустите приложение командой:
   ```bash
   streamlit run src/app.py
   ```
2. Перейдите в браузер по адресу `http://localhost:8501`.
3. Введите вопрос в первое текстовое поле и нажмите Enter, чтобы получить ответ от Ollama.
4. Используйте второе текстовое поле для поиска по истории запросов. Введите ключевые слова, чтобы найти похожие вопросы.

---

## Examples

1. **Пример запроса**:
   - Вопрос: "Какая погода сегодня?"
   - Ответ: "Сегодня солнечно и тепло."

2. **Пример поиска**:
   - Ввод: "погода"
   - Результат: "Какая погода сегодня?"

---

## Project Repository Structure

```
Project Repository structure:
  - README.md                # Описание проекта
  - LICENSE                  # Лицензия
  - requirements.txt         # Зависимости проекта
  - src/                     # Исходный код
      └── app.py             # Основное приложение Streamlit
  - test/                    # Тесты
      └── test_app.py        # Тестирование функциональности
```

---

## Notes

- **Хранение истории**: Все вопросы сохраняются в базе данных ChromaDB для дальнейшего поиска.
- **Поиск**: Для поиска используется генерация векторных представлений текста (embedding). Сейчас используются случайные числа, но в будущем можно заменить на более продвинутую модель.

Если у вас возникнут вопросы, не стесняйтесь спрашивать!
```

Этот файл готов к добавлению в ваш проект. Если нужно что-то уточнить или доработать, напишите!
