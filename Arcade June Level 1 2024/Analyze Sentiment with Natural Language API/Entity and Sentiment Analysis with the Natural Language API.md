## Entity and Sentiment Analysis with the Natural Language API [GSP038]

### Create API key and Then Open VM Instances and Click SSH 

> Paste all the Command on [ SSH ] 

```
export API_KEY=
```

```
cat > request.json <<EOF
{
  "document":{
    "type":"PLAIN_TEXT",
    "content":"Joanne Rowling, who writes under the pen names J. K. Rowling and Robert Galbraith, is a British novelist and screenwriter who wrote the Harry Potter fantasy series."
  },
  "encodingType":"UTF8"
}
EOF

curl "https://language.googleapis.com/v1/documents:analyzeEntities?key=${API_KEY}" \
  -s -X POST -H "Content-Type: application/json" --data-binary @request.json > result.json



```

### !!! Done !!!
