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
ItemConfig: this is more data-based on each item, and also manages the properties of each item

InventoryRemoteEvent: this is how the server sends data or talks to the client (this is a specific remote name)

type Character: we declared that Character is a type model and a specific armor folder

local armorRemovalMap: this map correlates each armorSubtype with each accessoryType (we will use this later to remove specific accessories due to armor subtypes)

local function setAccessoriesByArmorSubtype: this loops through the character and uses the map in order to remove specific accessories due to what armor subtype you equipt

game.Player.PlayerAdder: When a player joins our game, we go inside the data of that player, and then we give them the specific items based on a bool value called ReceivedStarterPack

for_, uniqueItem in items: we are looping through the set of items and using datapaths module to set the data for that specific person

InventoryEquipRemote.OnServerEvent: this happens when the client (player) tries to equip a piece of gear. It then goes to the server and gets validated, and then there is an else if statement correlating to what is going to happen. If it is a piece of gear, we generate a new weld and weld it to the corresponding armor subtype, and remove the accessories held within the map. ELSE if it is already equipt then it will unequip it, and then the accessories will be put back on. ELSE IF it is a tool, then it will equip the tool


