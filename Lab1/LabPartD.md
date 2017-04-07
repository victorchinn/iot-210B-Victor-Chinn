[IOT STUDENT HOME](https://gitlab.com/Gislason/iot-210B-student/blob/master/README.md)

# Lab1 - PartD (Curl and HTTP)

In this section of the lab you will

* Learn about REST and HTTP
* Learn to use curl with APIs and HTTP programs
* Take the quiz again using curl

These apps can be run from the Raspberry Pi in terminal windows, or on your PC

## Curl

Curl is a general purpose tool. Below are the important bits.

```
  curl https://frozen-castle-53348/api/v1/student/{name}/answer \
    -X POST \
    -H "Content-Type: application/json" \
    –d '{"1":"A"}'
    --verbose
```

The --verbose is not needed, but can help understand HTTP, and can be useful for
debugging.

The `Content-Type: application/json` header is not needed, as quizical.py assumes
JSON.

A very useful tool for checking JSON for correctness is online at [JSONLint](http://jsonlint.com)

## Experiment with Curl

Go ahead and experiment with curl. Try using curl with ipv4_tcp_server.py

In one terminal window, run:
```
$ python ipv4_tcp_server.py
```

```
$ curl localhost:5000/
```

Why doesn't curl exit? (you can exit curl with ctrl-c)

## Retake the Quiz

Try using Curl to retake the quiz

```
curl https:frozen-castle-53348.herokuapp.com/api/v1/login -X PUT -d '{"user":"me","pwd":"pass"}'
curl https:frozen-castle-53348.herokuapp.com/api/v1/student/me/question
curl https:frozen-castle-53348.herokuapp.com/api/v1/student/me/answer -X PUT -d '{"1":"A"}'
```


[IOT STUDENT HOME](https://gitlab.com/Gislason/iot-210B-student/blob/master/README.md)
