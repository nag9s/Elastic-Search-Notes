[https://qbox.io/blog/logstash-grok-filter-tutorial-patterns](https://qbox.io/blog/logstash-grok-filter-tutorial-patterns)



https://grokdebug.herokuapp.com/

Debug

55.3.244.1 GET /index.html 15824 0.043

beneath, u will paste 

%{IP:client} %{WORD:method} %{URIPATHPARAM:request} %{NUMBER:bytes} %{NUMBER:duration}



and choose "Named Captures Only"

You will see this in the last text area

```
{
```

```
  "client": [
    [
      "55.3.244.1"
    ]
  ],
  "method": [
    [
      "GET"
    ]
  ],
  "request": [
    [
      "/index.html"
    ]
  ],
  "bytes": [
    [
      "15824"
    ]
  ],
  "duration": [
    [
      "0.043"
    ]
  ]
}
```



