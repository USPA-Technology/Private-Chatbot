# Private-Chatbot
Offline Chatbot for Private Document Interaction (Free and Secure)

Architecture of a CHATBOT
<img width="930" alt="SCR-20230917-qbto" src="https://github.com/abidsaudagar/Private-Chatbot/assets/20873579/e9c34bae-b697-4f11-b332-886ae298bc2b">

## Tech-stack used:
1. Langchain
2. GPT4all LLM
3. Sentence Transformer embeddings
3. Chroma Vector DataBase
4. Python 3.10 +

## Follow this checklist to run

1. Need Python 3.10, run following commands
```
sudo apt install python-is-python3
curl -sS https://bootstrap.pypa.io/get-pip.py | sudo python3.10
sudo apt-get install python3.10-venv
pip install virtualenv
python -m venv env
source env/bin/activate
pip install -r requirements.txt
```
2. To fix RuntimeError: Your system has an unsupported version of sqlite3. Chroma requires sqlite3 >= 3.35.0. Added these 3 lines in env/lib/python3.10/site-packages/chromadb/__init__.py at the beginning:
```
    __import__('pysqlite3')
    import sys
    sys.modules['sqlite3'] = sys.modules.pop('pysqlite3')
```