

This is an application that I created to work with the Ollama model and keep a history of interactions. It can answer your questions using the locally running Ollama API, and also allows you to search through saved questions using the ChromaDB database.
What does this app do? First, you ask a question in a text field. This question is passed to the Ollama API, which returns the answer to you. All your questions are saved in the database so that they can be found later. At any time, you can use the search function to remember what you asked earlier.ChromaDB is used to store the history. I made it so that each request is converted into a vector representation (embedding), and then saved along with the text. This allows you to quickly find queries similar to your search query.

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

1. Run the application with the command:
   ```bash
   streamlit run src/app.py
   ```
2. Go to the browser at `http://localhost:8501`.
3. Enter the question in the first text field and press Enter to get the answer from Ollama.
4. Use the second text field to search through the query history. Enter keywords to find similar questions.

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
