## SkyAuth JAVA Example

JAVA example for the https://skyproject.cc authentication system.

## **Bugs**

If the default example not added to your software isn't functioning how it should, please report a bug here https://skyproject.cc/app/?page=support


## **`SkyAuth` instance definition**

Visit https://skyproject.cc/app/ and select your application, then click on the **JAVA** tab

It'll provide you with the code which you should replace with in the `Application.java` file.

##### API 1.1 > Example is using Encryption so Request will be encrypted, and it needs to be decrypted before using.

-----------

##### **Filling SkyAuth Class Constructor**
```js
    private static String url = "";
    private static String ownerid = "";
    private static String appname = "";
    private static String version = "1.0";
    private static String responsemsg = "ON"; // RESPONSE BODY
```

##### **Initializing Application**
```js
await SkyAuth.init();
```
---

##### **General Features**
###### **Login**
```js
await SkyAuth.login("<USERNAME>", "<PASSWORD>");
```

###### **License Login**
```js
await SkyAuth.license("<LICENSE/KEY>");
```

###### **Upgrade an Account**
```js
await SkyAuth.upgrade("<USERNAME>", "<LICENSE/KEY>");
```

---
##### **Banning Logged in User**
```js
await SkyAuth.ban();
```

---
##### **Webhooks**

###### Normal Request with Params
```js
await SkyAuth.webhook("<WebId>", "<Params>")
```

###### Webhook Request with Body & Content Type
```js
await SkyAuth.webhook("<WebId>", "<Params>", "<Body>", "<Content Type>");
```

###### Discord Webhook Example
```js
await SkyAuth.webhook("<WebId>", "", "{\"content\": \"webhook message here\",\"embeds\": null}", "application/json");
```

##### **Sleep is ms(s)**
```js
await SkyAuth.sleep("<1 sec = 1000ms>")
```
