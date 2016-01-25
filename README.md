In booting up my project  `METEOR@1.3-modules-beta.5` I get the following error:

```
ReferenceError: Contacts is not defined
  at meteorInstall.lib.collections.Contacts.js (lib/collections/Contacts.js:2:1)
  at fileEvaluate (packages/modules-runtime/.npm/package/node_modules/install/install.js:183:1)
  at require (packages/modules-runtime/.npm/package/node_modules/install/install.js:75:1)
  at /red/act/ed/.meteor/local/build/programs/server/app/app.js:704:1
  at /red/act/ed/.meteor/local/build/programs/server/boot.js:242:10
  at Array.forEach (native)
  at Function._.each._.forEach (/home/dev/.meteor/packages/meteor-tool/.1.1.12-modules.5.lsgx7o++os.linux.x86_64+web.browser+web.cordova/mt-os.linux.x86_64/dev_bundle/server-lib/node_modules/underscore/underscore.js:79:11)
  at /red/act/ed/.meteor/local/build/programs/server/boot.js:137:5
Exited with code: 8
```

File in question:

```javascript
/* lib/collections/Contacts.js */
Contacts = new Mongo.Collection('Contacts')
```

#### I've tried
`meteor reset`
`rm -rf .meteor/local/`
`rm -rf node_modules/; npm install;`

#### Simple reproduction
https://github.com/huttonr/meteor-global-variable-error
