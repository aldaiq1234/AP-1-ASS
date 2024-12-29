

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

1. **Request example**:
   - ![image](https://github.com/user-attachments/assets/25802fec-3d2a-4180-a524-a529390f5a90)
   - ![image](https://github.com/user-attachments/assets/db1f5d8e-de1a-4144-a5f2-a2885b8c5120)


---

## Project Repository Structure

```
Project Repository structure:
  - README.md                
  - LICENSE                 
  - requirements.txt         
  - src/                    
      └── app.py             
  - test/                    
      └── test_app.py        
```

---

## Notes

- **History Storage**: All questions are saved in the ChromaDB database for further search.
- **Search**: The generation of vector representations of text (embedding) is used for the search. Random numbers are currently used, but in the future they can be replaced with a more advanced model.
- ![image](https://github.com/user-attachments/assets/c0d9a314-4423-4d95-a57f-58db8c217d9c)



