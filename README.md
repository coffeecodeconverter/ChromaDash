Introducing ChromaDash, a hassle-free dashboard for ChromaDB

![image](https://github.com/user-attachments/assets/78046edf-7ab1-4b5f-8177-136e4b7c753d)

I built ChromaDash with a singular goal: to make managing your ChromaDB as simple and smooth as possible. 
You don’t need to mess with dependencies, install Python or Node.js, or worry about complicated setups, in order to view or manage your Vector Database.  
Just open your browser, and it works—straight out of the box. 

It's all packaged in a single HTML file (with a few images), so all you need to do is launch it, and you’re good to go!

With ChromaDash, you can easily:
- view, add, delete, and edit collections
- view, add, delete, and edit documents - BUT CANT add documents with embddings (see further below)
- perform basic text-based search on documents (doesnt yet support vector search, there is a reason)
  
Whether you're managing data or simply checking your document counts, everything is just a click away. 
And, because I wanted to make it as user-friendly as possible, I've included links to all the ChromaDB documentation, helpful resources, and even other GitHub projects to inspire your journey.

ChromaDash interacts with ChromaDB exclusively through FastAPI (i.e. appending '/docs' to the chromaServer Endpoint 'http://localhost:8000/docs'), which presents several limitations. Notably, FastAPI lacks the capability to automatically generate embeddings; it only allows you to provide pre-generated embeddings. This limitation is problematic unless you intend to use a custom embedding model outside of ChromaDB. Embedding functions are available only in client libraries (in Python or Node.js) and are not included in FastAPI. Consequently, while ChromaDash can add documents, it's advisable not to do so because they will be stored in plain text, which is unsuitable for vector searches. However, plain text searches are still possible.

The frustration here is that Chroma's developers have created a Python-based server and exposed a FastAPI for it but have omitted critical functions such as embedding generation. When inquiring about this, you are advised to write your own client from scratch and expose the embedding functions through your API. It seems illogical that after developing the server, client libraries, and 98% of FastAPI, users are expected to recreate the remaining 2% themselves before they can add the final functionality. This approach feels inefficient and convoluted.

Another option, given that ChromaDB is open-source, is to fork it and add the missing functionality yourself. However, this requires knowledge that I currently lack—perhaps someone else might be able to contribute.

If FastAPI were as functional as the client libraries, you would have more flexibility. This would allow you to create a user interface in any language that supports HTTP requests, including standard HTML and JavaScript, which are cross-platform and require no additional dependencies.

The situation is further frustrating because Chroma's developers have not released an official management tool or GUI. This gap is why I developed this project. Unfortunately, I only realized the limitations of FastAPI when I was over 80% through my project, which was a significant setback.

It appears that many developers encounter the same obstacles repeatedly with no progress. For ChromaDB to gain wider adoption, the process needs to be made significantly easier. ChromaDash represents one attempt to address this, but its potential is limited by the underlying constraints. Nevertheless, it remains a useful "viewer" tool that is quick and easy to use. It can provide insights into your Chroma database and assist in the development of other Chroma tools. I hope it proves helpful to others despite its limitations.

alternative projects you should also check out if you havent: <Br>
https://chroma-ui.vercel.app/ <Br>
https://github.com/Pawandeep-prog/chroma-peek <Br>
https://github.com/msteele3/chromagraphic <br>
https://github.com/Mintplex-Labs/vector-admin <bR>

for ANY ChromaDB Questions, or troubleshooting, i HIGHLY recommend you check this out:
https://wiki.mutable.ai/chroma-core/chroma

other tools - document stripper to plain text in batches 
https://github.com/coffeecodeconverter/DocStrip

Tags:
#chromadash #chromadb ui
#chroma ui 
#chromadb ui 
#chroma dash 
#ui for chroma
#ui for chromaDB

