# MailHops API node
[www.MailHops.com](http://www.mailhops.com)

<img src="http://www.mailhops.com/images/logos/mailhops395.png" width="200" alt="MailHops logo" title="MailHops" align="right" />

A nodejs module for interacting with the MailHops API.

##Getting Started

###Installation

```
$ npm install mailhops
```

###Configuration
Simply require the mailhops module, instantiate a new MailHops object, configure it if necessary, and start making calls. 

New MailHops objects can be instantiated with configuration parameters. Here is an example:

```javascript
var MailHops = require("mailhops");
var mailhops = new MailHops({
    api_key: "aWN8Pb27Xj6GfV8D6ARsjokonYwbWUNbz9rM",
    api_version: 1,
    proxy: "http://myproxy:3128",
    app_name: "Node App v1.0.0",
    forecastio_api_key: "",
    show_client: 1
});
```

MailHops objects can also be configured via the ```.configure(options)``` method. Here is an exmaple:

```javascript
var MailHops = require("mailhops");
var mailhops = new MailHops();

var options = {
    api_key: "aWN8Pb27Xj6GfV8D6ARsjokonYwbWUNbz9rM"
}

mailhops.configure(options);

mailhops.lookup('216.58.217.46,98.138.253.109',function(err,response){
	console.log(response);
});

var mapUrl = mailhops.mapUrl('216.58.217.46,98.138.253.109');

```

###Running Tests
```
$ npm test
```

## Other MailHops projects
- [API](https://github.com/avantassel/mailhops-api)
- [Postbox & Thunderbird plugin](https://github.com/avantassel/mailhops-plugin)
- [Download](https://addons.mozilla.org/en-US/thunderbird/addon/mailhops/)