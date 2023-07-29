# 🌍 Olympus Multibot API Documentation 🤖

## 🌟 Basics

```lua
sleep(int ms) -- 🕒 Delay script execution by specified milliseconds
error() -- ❌ Stops the current script
say(string text) -- 💬 Send a message in game
getPing() -- 📶 Get current ping
connect() -- 🔗 Connect bot to game
disconnect() -- 🔓 Disconnect bot from game
runThread(function) -- 🧵 Run a function in a new thread
setJob(string jobname) -- 👷 Set the bot's job
setRid(string rid) -- 🔧 Set the bot's RID
setMac(string mac) -- 💻 Set the bot's MAC address
getRid() -- 🧰 Get the bot's RID
getMac() -- 🖥️ Get the bot's MAC address
```

## 🏃‍♂️ Movement

```lua
move(int radx, int rady, bool checkSolid) -- 👣 Move in a direction
findPath(int x, int y, int delay) -- 🧭 Find a path to a specific location
punch(int radx, int rady) -- 👊 Punch in a direction
```

## 🎮 Actions

```lua
drop(int id) -- 🗑️ Drop an item by id
drop(int id, int amount) -- 🗑️ Drop a specific amount of an item
enter() -- 🚪 Enter a door or portal
wear(int id) -- 👕 Wear a clothing item by id
place(int id, int radx, int rady) -- 🏗️ Place an item at a specific location
wrench(int x, int y) -- 🔧 Use the wrench item at a specific location
eat(int itemid) -- 🍏 Make the bot eat an item
```

##  🎁 Inventory & Items

```lua
findItem(int id) -- 🔍 Find an item in inventory by id
findClothes(int id) -- 👖 Find clothes in inventory by id
collect(int radius) -- 🧺 Collect items in a specific radius
collect(int range, int ignoreid) -- 🧺 Collect items in a specific range, ignore a specific item
collectSet(bool collect) -- 🧺 Start or stop auto item collection
collectSet(bool collect, int radius) -- 🧺 Start or stop auto item collection within a specific radius
```

## 📬 Packet Manipulation

```lua
sendPacket(string text, int type) -- 📨 Send a packet with specific type and data
sendPacketRaw(packet, flags) -- 📨 Send a raw packet with specific flags
packet = {} -- 📨 New packet
packet.type
packet.netid
packet.flags
packet.int_data
packet.pos_x
packet.pos_y
packet.pos2_x
packet.pos2_y
packet.int_x
packet.int_y
```

## 🤖 Bots

```lua
changeBot(string name, string pass) -- 🔄 Change the active bot
addBot(string guest) -- ➕ Add a guest bot
addBot(string name, string pass) -- ➕ Add a bot with a specific name and password
addBot(string name, string pass, string socks) -- ➕ Add a bot with a specific name, password and proxy
addBot(string name, true, string socks) -- ➕ Add a guest bot with a specific proxy
removeBot(string name) -- ➖ Remove a bot by name
```

## 🎣 Hooks

```lua
addHook(string fname, string name, function) -- 🖇️ Add a hook for a specific event
removeHooks() -- ❌ Remove all hooks
```

## 🌐 HTTP Requests

```lua
request(string method, string url) -- 📡 Send a HTTP request
sendDiscordWebhook(string url, string message) -- 📡 Send a message to a Discord webhook
```

## 📡 Proxy

```lua
setProxy(string ip, int port) -- 🌐 Set the bot's proxy
setProxyAuth(string username, string password) -- 🔐 Set the bot's proxy authentication
```

## 📄 Information
### 🤖 Bot Information
```lua
getBot(string name) -- 📂 Get a bot by name
getBot() -- 📂 Get the active bot
getBots() -- 📂 Get all bots
Bot = {} -- 📂 Represents a bot
Bot.name
Bot.netId
Bot.userId
Bot.world
Bot.status
Bot.x
Bot.y
Bot.level
Bot.slots
Bot.captcha
Bot.proxy
Bot.proxyStatus
```
### 🌐 Tile Information
```lua
getTile(x, y) -- 📂 Get the tile at a specific location
getTiles() -- 📂 Get all tiles
Tile = {} -- 📂 Represents a tile
Tile.fg
Tile.bg
Tile.ready
Tile.flags
Tile.x
Tile.y
```
### 🎮 Object Information
```lua
getObjects() -- 📂 Get all objects
Object = {} -- 📂 Represents an object
Object.id
Object.count
Object.x
Object.y
Object.oid
```
### 👥 Player Information
```lua
getPlayers() -- 📂 Get all players
Player = {} -- 📂 Represents a player
Player.name
Player.netid
Player.userid
Player.country
Player.x
Player.y
```
### 📦 Inventory Information
```lua
getInventory() -- 📂 Get the bot's inventory
Item = {} -- 📂 Represents an inventory item
Item.name
Item.id
Item.count
```
### 👕 Clothing Information
```lua
getClothes() -- 📂 Get the bot's clothes
Clothing = {} -- 📂 Represents a clothing item
Clothing.name
Clothing.id
```
### 🎁 Item Information
```lua
itemInfo(int id) -- 📂 Get info about an item by id
itemInfo(string name) -- 📂 Get info about an item by name
ItemInfo = {} -- 📂 Represents item info
ItemInfo.id
ItemInfo.name
ItemInfo.rarity
ItemInfo.growTime
ItemInfo.breakHit
ItemInfo.clothingType
ItemInfo.collis
