Вот готовый `README.md`, соответствующий вашей структуре:

```markdown
# Ollama Chatbot with ChromaDB Integration

Этот проект — это простой бот для общения, который использует модель Ollama для обработки запросов и ChromaDB для хранения истории запросов. Вы можете задавать вопросы, получать ответы и искать свои прошлые запросы.

---

## Installation

1. Убедитесь, что у вас установлен Python версии 3.8 или выше.
2. Установите зависимости. Для этого выполните команду:
   ```bash
   pip install -r requirements.txt
   ```
3. Убедитесь, что API Ollama запущен локально на `http://localhost:11434`.

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
