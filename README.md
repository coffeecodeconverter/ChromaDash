Introducing ChromaDash<br>
<Br>
A hassle-free **HTTP Client for ChromaDB**<Br>
<Br>
![image](https://github.com/user-attachments/assets/78046edf-7ab1-4b5f-8177-136e4b7c753d)
<Br>
<br>

A Simple Web UI to to connect to a Chroma DB HTTP Server <br>
<br>
<br>

- No Dependancies
- Nothing to install
- just a single **index.html**
- that's it!
<br>
<br>

**Usage**:<br>
1. assuming you've installed ChromaDB in python using:
~~~~~~~~~~~~~~~~~~
pip install chromadb
~~~~~~~~~~~~~~~~~~
<Br>

2. you'd start the ChromaDB HTTP Server with this command:
~~~~~~~~~~~~~~~~~~~~
chroma run --path [/path/to/persist/data]
~~~~~~~~~~~~~~~~~~~~
for example:<Br>
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
chroma run --path C:\Program Files\ChromaDB\Data
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Which defaults to listening on **http://127.0.0.1:8000**
<br>

3. Add a system environment variable:
~~~~~~~~~~~~~~~~~~
name
CHROMA_SERVER_CORS_ALLOW_ORIGINS

value
["*"]
~~~~~~~~~~~~~~~~~~

4. download ChromaDash's **index.html**
and run it!
<br>
<br>
<br>

ChromaDash is just a basic viewer<br>
you can:<br>
- create, view, delete collections
- create, view, edit, delete documents (but WITHOUT embeddings, as its missing from chromas HTTP Client library)
<Br>
<br>

**A more Comprehensive Solution**<br>
Ive also released a FULLY FEATURED Python Client for Chroma DB called:<bR>
<br>
**Chroma Flow Studio**<br>
**https://github.com/coffeecodeconverter/ChromaFlowStudio**
<br>
This might be more what you're after<br>
<br>
<Br>
<br>

other tools - document stripper to plain text in batches 
https://github.com/coffeecodeconverter/DocStrip

Tags:
#chromadash #chromadb ui
#chroma ui 
#chromadb ui 
#chroma dash 
#ui for chroma
#ui for chromaDB

