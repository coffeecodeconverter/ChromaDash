Introducing ChromaDash, a hassle-free dashboard for ChromaDB

![image](https://github.com/user-attachments/assets/825d1302-73ab-4857-aa0b-f2647903ba06)

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

ChromaDash interacts with chromaDB using the FastAPI only, which has some limitations. 
namely, the FasAPI doesnt have the ability to generate embeddings automatically - you only have the option to provide your own generated embeddings. 
however, this is pointless unless you're intending to use your own embedding model outside of chromaDB. 
for some reason, the embedding functions are only included in the client libraries (in python or node.js) and are omitted from the FastAPI. 
Therefore, although ChromaDB can add documents, its advisable not to - simply becasue they'll be in plain text, which you cant do vector searches on. 
But you can do plain text searches. 

The annoyance here, is that effectivly - the devs at Chroma have built their server in python, exposed a FastAPI for it, but then left out some KEY funcitons, like embedding generation. 
When you enquire about this, you're told you need to write your own client, from scratch, and expose the embedding functions through an API yourself.
but hold on....why cant they just do that!? 
it seems dumb to me, that they've already written a server, and client libraires, and 98% of a fastAPI, only to then tell you as the end user / end developer to not finihs off that last 2%, but to actually have to RE-WRITE the first 98% yourself FIRST, before you can then add the last 2%!! its madness! 
the other option, seeing as chromaDB is open-source, is to fork it, and add the extra functionality yourself. 
i have no idea how to do this. maybe someone else will? 
thats all it needs. 
if the FastAPI was as functional as the client libraires, you'd have more flexibilty - you could create a UI in ANY language that supports HTTP requests, inlcuding standard HTML and javascript, which is cross-platform an requires no dependancies. 

this whole approach is even more annoying when you find the chorma devs havent release an offical management tool or GUI of their own. 
hence why i created this project. 
but it wasnt until i got over 80% of the way through my idea before realising the FastAPI is limited! (kick in the teeth) 

all i see is multiple devs repeating the same steps over and over and all getting stuck at the same point with no progress. 
if they want to see bigger adoption of this, it needs to be made easier - MUCH easier. 
ChromaDash is one attempt at this. 
but alas, i cant bring it up to its full potential given the underlying limitations. 
still, its a helpful "viewer" tool thats quick and easy to use. It can certainly help you get an insight to your chroma database, and may help you co-develop other chroma tools. 
i wish it could be made more useful. 
hopefully helps someone out along the way. 

alternative projects you should also check out if you havent: <Br>
https://chroma-ui.vercel.app/ <Br>
https://github.com/Pawandeep-prog/chroma-peek <Br>
https://github.com/msteele3/chromagraphic <br>
https://github.com/Mintplex-Labs/vector-admin <bR>

for ANY ChromaDB Questions, or troubleshooting, i HIGHLY recommend you check this out:
https://wiki.mutable.ai/chroma-core/chroma


