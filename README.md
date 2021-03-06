# Adjetiveisor as a service
This service allows you to add some adjectives to your sentences. It uses [adjetiveisor](https://github.com/agm-dev/adjetiveisor) package.

You can find an implementation of this code on [adjetiveisor.assa.services](https://adjetiveisor.assa.services)

# Usage
Send your sentences by POST request to the different endpoints as a JSON object:
> POST https://adjetiveisor.assa.services/puto

```{"text": "el coche"}```

You should get a response like this:

```
{
   "result": {
       "status": "OK",
       "code": 200,
       "count": 1
   },
   "data": [
       {
           "text": "el coche",
           "translation": "el puto coche",
           "translator": "puto"
       }
   ]
}
```

You can also check the translators available by `GET` request on `/translators` endpoint, and you should get an answer like this:

```
{
    "result": {
        "status": "OK",
        "code": 200,
        "count": 3
    },
    "data": [
        "jodido",
        "malpario",
        "maldito"
    ]
}
```

# Endpoints
Right now these are the endpoints configured:

> GET https://adjetiveisor.assa.services/translators
____

> GET https://adjetiveisor.assa.services/puto

> POST https://adjetiveisor.assa.services/puto
____

> GET https://adjetiveisor.assa.services/jodido

> POST https://adjetiveisor.assa.services/jodido
____

> GET https://adjetiveisor.assa.services/malpario

> POST https://adjetiveisor.assa.services/malpario
____
> GET https://adjetiveisor.assa.services/maldito

> POST https://adjetiveisor.assa.services/maldito
