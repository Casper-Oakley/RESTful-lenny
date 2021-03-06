# RESTful-**_Lenny_** 
Providing ( ͡° ͜ʖ ͡°) to a hack near you!

![RESTful Lenny](https://i.imgur.com/LzBTC4r.png)

_A **Lenny** API_. Use this to bring **_Lenny_** face to your applications!

---

To run the API, see SETUP.md.

---

# API Documentation #

* [Get the original **_Lenny_**](#original-lenny)
* [Get a random **_Lenny_**](#random-lenny)
* [Customise your **_Lenny_**](#customise-lenny)

<br>
<a name="original-lenny"></a>

## Original **_Lenny_** 

`GET https://api.lenny.today/v1/lenny`<br>
(_[Try it](https://api.lenny.today/v1/lenny)_)

**Response**

HTTP Status Code: 200 OK<br>
Content-Type: application/json

**Example Response Body**
```json
[
  {
    "face": "( ͡° ͜ʖ ͡°)"
  }
]
```

___
<br>
<a name="random-lenny"></a>

## Random **_Lenniez_**

`GET https://api.lenny.today/v1/random?limit=5`<br>
(_[Try it](https://api.lenny.today/v1/random?limit=5)_)<br>
_Maximum limit of 500 **Lenniez** per request_

**Response**

HTTP Status Code: 200 OK<br>
Content-Type: application/json

**Example Response Body**
```json
[
  {
    "seed": 1,
    "face": "ᕮ・□・ᕭ"
  },
  {
    "seed": 1,
    "face": "ᕙ(  ͌ ε   ͌)ᕗ"
  },
  {
    "seed": 1,
    "face": "(ง⪦ᨎ⪧)ง"
  },
  {
    "seed": 1,
    "face": "ᑫxロxᑷ"
  },
  {
    "seed": 1,
    "face": "(づ■⍊■)づ"
  }
]
```

### Error Responses
#### Invalid limit
If you try to request too many **_Lenniez_**.

HTTP Status Code: 400 BAD REQUEST<br>
Content-Type: application/json

**Response Body**<br>
```json
{
  "ლ(⏓益⏓ლ)": "┬─┬ノ( ´ᗝ`ノ)"
}
```

___
<br>
<a name="customise-lenny"></a>

## Customise **_Lenny_**

`GET https://api.lenny.today/v1/random?mouth=%E1%A8%93&eyes=*&limit=5`<br>
(_[Try it](https://api.lenny.today/v1/random?mouth=%E1%A8%93&eyes=*&limit=5)_)<br>
_This will generate 5 different **Lenniez** with ᨓ for the mouth and * for the eyes._

**Response**

HTTP Status Code: 200 OK<br>
Content-Type: application/json

**Example Response Body**
```json
[
  {
    "seed": 1,
    "face": "ヽ(*ᨓ*)ﾉ"
  },
  {
    "seed": 1,
    "face": "ᕮ*ᨓ*ᕭ"
  },
  {
    "seed": 1,
    "face": "ᕙ(*ᨓ*)ᕗ"
  },
  {
    "seed": 1,
    "face": "ლ(*ᨓ*ლ)"
  },
  {
    "seed": 1,
    "face": "|*ᨓ*|"
  }
]
```


### Description
When getting a random **_Lenny_**, you can specify what characters to use for the different parts of the face.<br>
Any parts of the face you don't specify will be random.

**Facial Features**
* leftear
* rightear
* ears (overrides leftear and rightear)
* lefteye
* righteye
* eyes (overrides lefteye and righteye)
* mouth 

Make sure to [URL Encode](https://www.google.co.uk/search?q=url+encoder) your query parameters. (Your web browser will do this for you _most_ of the time)
