# Jackbox_UGC
Featured Content of games: Quiplash 3, Drawful Animate. Created for Jackbox modifiers and translators. Taken from ecast.jackboxgames.com 

## How to change the Featured Content list
### Changing files
Go to directory `api/v2/ugc/list/`, at the moment you will see three files: `drawful-animated` - Drawful Animated; `quiplash3-tjsp`, `q3featured` - Quiplash 3. You can add, change, remove, whatever your soul desires. If you want to add and/or change the file(s), pay attention to the `contentId`, because you can't change the title itself, you have to create your own title in the game (or on [the website](https://sid3r.net/ContentManager/)) and insert/replace it.
### Putting it on a site
Then when you've done everything you want to do. You need to put it on your website. You can put it anywhere you want, but it's better to not take long directories. For example, you changed the file `drawful-animated`, and put it in the folder `ugc` and the site where you will put it `example.com`. That is, its directory will be `example.com/ugc/drawful-animated`. The next step will use this example directory.
### Putting in the game X
Go to `jackboxgames.X.actionpackages.ui.menu.ugc` in `X.swf`. Next, in **Quiplash 3 [TJPP7]** find line 198 and line 200. (In **Drawful Animate** the first line is 196, the second line is 198; In **Quiplash 3 [TJPS]** the first line is 200, the second line is 202).<br /><br />Instead of `var domainWithAPIVersion:String = domain + "/api/v2";`<br />replace with `var domainWithAPIVersion:String = "example.com";`.<br /><br />After that in second line<br />instead of `restAPI.GET("/ugc/list/" + this._listId,null,function(param1:Object):void`<br />replace with `restAPI.GET("/ugc/" + this._listId,null,function(param1:Object):void`.

==================================================================<br>You have crossed the finish line. That's it. If you have any problems you can go to the [Discord Server](https://www.discord.gg/FsfSdVKcwq).
- X - game title
- TJPP7 - The Jackbox Party Pack 7
- TJPS - The Jackbox Party Starter
