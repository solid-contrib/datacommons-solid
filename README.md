# datacommons-solid
Logic to provide a linked data view of datacommons.org data
There are various styles of API t chose from.

API Docs are at https://docs.datacommons.org/api/rest/


Found issues with datacommons at the time, prob temp problems. Eg


```
$ curl -X POST 'https://api.datacommons.org/query' -d '{"sparql": "SELECT ?name \
                WHERE { \
                  ?state typeOf State . \
                  ?state dcid geoId/06 . \
                  ?state name ?name \
                }"}'  > states.json
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   259    0    64  100   195     50    152  0:00:01  0:00:01 --:--:--   202
$
$ cat states.json
{"header":["?name"],"rows":[{"cells":[{"value":"California"}]}]}$
```
So only one state?
