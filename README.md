# Node.js


Start application: 
```bash
npm install
npm start
curl localhost:5000/user
```

Testing:
```bash
curl localhost:5000/user/
curl localhost:5000/user/johnsmith@gamil.com
curl --request POST 'localhost:5000/user?firstName=Jon&lastName=Lovato&email=jonlovato@theworld.com&DOB=10/10/1995'
curl localhost:5000/user/jonlovato@theworld.com

curl --request PUT 'localhost:5000/user/johnsmith@gamil.com?DOB=1/1/1971'
curl localhost:5000/user/johnsmith@gamil.com

curl --request DELETE 'localhost:5000/user/johnsmith@gamil.com'
```

With authorization:
```bash
npm run start_auth
```

Postman check:
- Post:
    - URL: https://hxvinhhcmus-5000.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/login
    - body (raw): 
```yaml
{
    "user":{
        "name":"abc",
        "id":1
    }
} 
```

- Get:
    - URL: https://hxvinhhcmus-5000.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/user
    - URL: https://hxvinhhcmus-5000.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/user/johnsmith@gamil.com


- Post (params):
    - URL: https://hxvinhhcmus-5000.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/user?firstName=Bob&lastName=Smith&email=bobsmith@theworld.com&DOB=1/1/1975

- Put(params):
    - URL: https://hxvinhhcmus-5000.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/user/bobsmith@theworld.com?DOB=1/1/1975

- Delete:
    - URL: https://hxvinhhcmus-5000.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/user/bobsmith@theworld.com