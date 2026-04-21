Oh my days, here we go, laddies and gentlemen!
-- In Lua, it means to comment out.

In Lua and many other game engines, there is a server that is authoritative and a client that requests data from the server.

InventoryClient is the requesting subject, and the InventoryServer is the authoritative subject.

Inventory Server is what I covered in the class, so I am going to recap what each line means.

ReplicatedStorage: is a server-sided storage facility for anything you could need (static meshes, sound, other scripts)

HttpService : is a service we call in order to make unique item identifiers (34jokj-34jkmn-kn234nk)

DataService: is a module script that allows us to run/use specific code (#include kinda)
DataTemplate: is a module script that contains all our predefined saving information (what we save and how)
DataPaths: is a module script that contains a map to all the pathways we need to in a more easier to use way (this is going to be how we get inside of the data template to manipulate the data)

Types: is a module script that has all the information for each piece of gear/tool
ItemConfig: this is more data-based on each item and also manages that properties of each item

InventoryRemoteEvent: this is how the server sends data or talks to the client (this is a specific remote name)

type Character: we declared that character is type model and a specific armor folder
