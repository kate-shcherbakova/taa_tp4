### DO NOT STOP THE DOCKER CONTAINER FOR KEYCLOAK

##### To get client secret
1. Clients - Client details - myspringbootapp
2. Client authentication + Service accounts roles

##### To get token
1. Required user actions - remove Update Password
2. In terminal
```
curl --location 'http://localhost:8080/realms/myspringbootapprealm/protocol/openid-connect/token' --header 'Content-Type: application/x-www-form-urlencoded' --data-urlencode 'username=myuser' --data-urlencode 'password=3677417' --data-urlencode 'grant_type=password' --data-urlencode 'client_id=myspringbootapp' --data-urlencode 'client_secret=ih7SbP9PLYErKiisHgLstMV2Ztrji0gC' --data-urlencode 'scope=openid'
```

**myuser**
```
{"access_token":"eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICItc1ZXMmpmUmVFUWZua3k2YmRRN1k2WjByQ0pqN0JQOGY5Y3JtNDdmMGxNIn0.eyJleHAiOjE3MDEzMDIxNDQsImlhdCI6MTcwMTMwMTg0NCwianRpIjoiYmRjZTI5Y2QtODZmYi00ZmI1LTkyMTUtNzg1ODYwYTUxZWZiIiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDgwL3JlYWxtcy9teXNwcmluZ2Jvb3RhcHByZWFsbSIsImF1ZCI6ImFjY291bnQiLCJzdWIiOiJjYjNlOWQwYS05MzlkLTRlZTAtYjM4OC00NTZmZTRmYjY4ZTEiLCJ0eXAiOiJCZWFyZXIiLCJhenAiOiJteXNwcmluZ2Jvb3RhcHAiLCJzZXNzaW9uX3N0YXRlIjoiZjI1Y2VlZDUtOTE1ZC00OGFjLTg3YTgtYTdiZGE0ZTk3YTdkIiwiYWNyIjoiMSIsImFsbG93ZWQtb3JpZ2lucyI6WyIvKiJdLCJyZWFsbV9hY2Nlc3MiOnsicm9sZXMiOlsib2ZmbGluZV9hY2Nlc3MiLCJ1bWFfYXV0aG9yaXphdGlvbiIsIlVTRVIiLCJkZWZhdWx0LXJvbGVzLW15c3ByaW5nYm9vdGFwcHJlYWxtIl19LCJyZXNvdXJjZV9hY2Nlc3MiOnsiYWNjb3VudCI6eyJyb2xlcyI6WyJtYW5hZ2UtYWNjb3VudCIsIm1hbmFnZS1hY2NvdW50LWxpbmtzIiwidmlldy1wcm9maWxlIl19fSwic2NvcGUiOiJvcGVuaWQgZW1haWwgcHJvZmlsZSIsInNpZCI6ImYyNWNlZWQ1LTkxNWQtNDhhYy04N2E4LWE3YmRhNGU5N2E3ZCIsImVtYWlsX3ZlcmlmaWVkIjpmYWxzZSwibmFtZSI6IkthdGVyeW5hIFNoY2hlcmJha292YSIsInByZWZlcnJlZF91c2VybmFtZSI6Im15dXNlciIsImdpdmVuX25hbWUiOiJLYXRlcnluYSIsImZhbWlseV9uYW1lIjoiU2hjaGVyYmFrb3ZhIn0.m3G0IRspBUvIR1swjqvccJQD0Gt7IQxe3kkbasE9SHiFJxL7enBpj1ppvlA6SXKmZXjRzTbEhuQaykuusfV0dUE43_7_6sQ9wrYWRnA5fBOVeIQLLoLz-8urZhAcqm9FDjWS8DcIA92CSN2jfwSJMQ1VoPFol0k3YHbqEzP2hYocR8MkWCmz8RRs6gn2IgMTaed3cZgE-Y7hWZir-8Lqz0_gTU9az2tofR1WTPMkLzs0LRXvxKj4ti0gI8MBxyRxE5pJdJ5vnJD07l_D0EF4FKUg7dbotXNMJQrEPEHc-SX244ZwlMFZgBLLf08hAa9p_DNkBqPBCXkmS9NRcDeERQ","expires_in":300,"refresh_expires_in":1800,"refresh_token":"eyJhbGciOiJIUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJiOTRkMmM0Zi02ODQ5LTQwYTYtYTQyNC01YmU2NWI5OTNkZGUifQ.eyJleHAiOjE3MDEzMDM2NDQsImlhdCI6MTcwMTMwMTg0NCwianRpIjoiZTUxNzQxNTctNjI1Yi00NGZkLTlhNTUtOWI3OTdiMGFlZjk5IiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDgwL3JlYWxtcy9teXNwcmluZ2Jvb3RhcHByZWFsbSIsImF1ZCI6Imh0dHA6Ly9sb2NhbGhvc3Q6ODA4MC9yZWFsbXMvbXlzcHJpbmdib290YXBwcmVhbG0iLCJzdWIiOiJjYjNlOWQwYS05MzlkLTRlZTAtYjM4OC00NTZmZTRmYjY4ZTEiLCJ0eXAiOiJSZWZyZXNoIiwiYXpwIjoibXlzcHJpbmdib290YXBwIiwic2Vzc2lvbl9zdGF0ZSI6ImYyNWNlZWQ1LTkxNWQtNDhhYy04N2E4LWE3YmRhNGU5N2E3ZCIsInNjb3BlIjoib3BlbmlkIGVtYWlsIHByb2ZpbGUiLCJzaWQiOiJmMjVjZWVkNS05MTVkLTQ4YWMtODdhOC1hN2JkYTRlOTdhN2QifQ.ME0kbdKbZRcHzGF8oBXH-rqHGCanrGfi-ZvcAXUNLZc","token_type":"Bearer","id_token":"eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICItc1ZXMmpmUmVFUWZua3k2YmRRN1k2WjByQ0pqN0JQOGY5Y3JtNDdmMGxNIn0.eyJleHAiOjE3MDEzMDIxNDQsImlhdCI6MTcwMTMwMTg0NCwiYXV0aF90aW1lIjowLCJqdGkiOiJjZGNlZDE2My0zNWEwLTQ0YjUtODgyYi00ZGU0OGQ4YTJlY2UiLCJpc3MiOiJodHRwOi8vbG9jYWxob3N0OjgwODAvcmVhbG1zL215c3ByaW5nYm9vdGFwcHJlYWxtIiwiYXVkIjoibXlzcHJpbmdib290YXBwIiwic3ViIjoiY2IzZTlkMGEtOTM5ZC00ZWUwLWIzODgtNDU2ZmU0ZmI2OGUxIiwidHlwIjoiSUQiLCJhenAiOiJteXNwcmluZ2Jvb3RhcHAiLCJzZXNzaW9uX3N0YXRlIjoiZjI1Y2VlZDUtOTE1ZC00OGFjLTg3YTgtYTdiZGE0ZTk3YTdkIiwiYXRfaGFzaCI6Ijhta3otTElUSWR3YkhmM2o3NlRtb1EiLCJhY3IiOiIxIiwic2lkIjoiZjI1Y2VlZDUtOTE1ZC00OGFjLTg3YTgtYTdiZGE0ZTk3YTdkIiwiZW1haWxfdmVyaWZpZWQiOmZhbHNlLCJuYW1lIjoiS2F0ZXJ5bmEgU2hjaGVyYmFrb3ZhIiwicHJlZmVycmVkX3VzZXJuYW1lIjoibXl1c2VyIiwiZ2l2ZW5fbmFtZSI6IkthdGVyeW5hIiwiZmFtaWx5X25hbWUiOiJTaGNoZXJiYWtvdmEifQ.eikFsVhZbXg8oJagMUSY8xFRM72ZZu8IFOtRGPugWRwPuAddvWQQ4ZI-F4f9-ziKhPigqlj22kkiGchdN7O3ifOFC5QmLfWOMyJ4VSL_CAauv4AXMbqOqunUNDkjHOb_F0CSdjPylh_SXhPplBDBVL7c29bFX-3iIEyDooi3kSUld7Ky7XDtNMUdoCRQjgbHnSm-VVpce-42HR-iKDv_SbV0lhf2ARum0D7MphCH02RGXukYtuMwNeElacDhcJy4_MTgUUJNCISWeb9bRw99dUU0B1QJJJpwQ_WQOiyKVFxBOMqGfmKsjBAPkZbFA82tJOSVTRVLvD9dcm-vzcD2xA","not-before-policy":0,"session_state":"f25ceed5-915d-48ac-87a8-a7bda4e97a7d","scope":"openid email profile"}
```

**myuser2**
```
{"access_token":"eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICItc1ZXMmpmUmVFUWZua3k2YmRRN1k2WjByQ0pqN0JQOGY5Y3JtNDdmMGxNIn0.eyJleHAiOjE3MDEzMDIyNjQsImlhdCI6MTcwMTMwMTk2NCwianRpIjoiMzNiZTViNmYtNjVlOC00NGUxLTgxNjktNDBkZTBkYTNlOWJmIiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDgwL3JlYWxtcy9teXNwcmluZ2Jvb3RhcHByZWFsbSIsImF1ZCI6ImFjY291bnQiLCJzdWIiOiJkZWU5ZWY4MC1hZTY5LTRkZTMtYTE3Yy0yMzI0Zjg3NGQ5ZTIiLCJ0eXAiOiJCZWFyZXIiLCJhenAiOiJteXNwcmluZ2Jvb3RhcHAiLCJzZXNzaW9uX3N0YXRlIjoiNWJkNTEyNmYtYTJkNy00NDMwLWJhNDYtOGI5NjU3NmIxYjcyIiwiYWNyIjoiMSIsImFsbG93ZWQtb3JpZ2lucyI6WyIvKiJdLCJyZWFsbV9hY2Nlc3MiOnsicm9sZXMiOlsib2ZmbGluZV9hY2Nlc3MiLCJ1bWFfYXV0aG9yaXphdGlvbiIsIkFETUlOIiwiZGVmYXVsdC1yb2xlcy1teXNwcmluZ2Jvb3RhcHByZWFsbSJdfSwicmVzb3VyY2VfYWNjZXNzIjp7ImFjY291bnQiOnsicm9sZXMiOlsibWFuYWdlLWFjY291bnQiLCJtYW5hZ2UtYWNjb3VudC1saW5rcyIsInZpZXctcHJvZmlsZSJdfX0sInNjb3BlIjoib3BlbmlkIGVtYWlsIHByb2ZpbGUiLCJzaWQiOiI1YmQ1MTI2Zi1hMmQ3LTQ0MzAtYmE0Ni04Yjk2NTc2YjFiNzIiLCJlbWFpbF92ZXJpZmllZCI6ZmFsc2UsIm5hbWUiOiJPbGVrc2lpIFRrYWNoZW5rbyIsInByZWZlcnJlZF91c2VybmFtZSI6Im15dXNlcjIiLCJnaXZlbl9uYW1lIjoiT2xla3NpaSIsImZhbWlseV9uYW1lIjoiVGthY2hlbmtvIn0.TQz21dTqz9_0ICWYg2kU9RFstwz-wl_mXC4MF3hHs7Yaj4bYPgMjCCRNSmRHvwDW8CLilXFPF8Z4OP52KdtjhphchutTQTQwcJr8P94BOGqwnaIdTFQ0Vhk6adBkqyGn8ywpDt8ktuXvhJal8hb6HnM8ge3vX_ncUOiAmG1shC3ZXGFLlIkQ7N86lQKQ8uYqsmp9s0xtcvrfTu5hKcOVSAxYj07B6NZ85VjDGnduMLkVZ7YdbwlvslENXAQ0u6M2rUTShMrhAEQZywbG8aPdBPwQNJOLkG-Sr0Cmf5pg00LZTRAXzB-t_ISDt6PnP1Di1w4ra0JPcJmla779UsIb1A","expires_in":300,"refresh_expires_in":1800,"refresh_token":"eyJhbGciOiJIUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJiOTRkMmM0Zi02ODQ5LTQwYTYtYTQyNC01YmU2NWI5OTNkZGUifQ.eyJleHAiOjE3MDEzMDM3NjQsImlhdCI6MTcwMTMwMTk2NCwianRpIjoiZWRlZTBlMTYtZjRlYy00ZGY4LWJlZTEtMWVhOTA4MzdjYWIxIiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDgwL3JlYWxtcy9teXNwcmluZ2Jvb3RhcHByZWFsbSIsImF1ZCI6Imh0dHA6Ly9sb2NhbGhvc3Q6ODA4MC9yZWFsbXMvbXlzcHJpbmdib290YXBwcmVhbG0iLCJzdWIiOiJkZWU5ZWY4MC1hZTY5LTRkZTMtYTE3Yy0yMzI0Zjg3NGQ5ZTIiLCJ0eXAiOiJSZWZyZXNoIiwiYXpwIjoibXlzcHJpbmdib290YXBwIiwic2Vzc2lvbl9zdGF0ZSI6IjViZDUxMjZmLWEyZDctNDQzMC1iYTQ2LThiOTY1NzZiMWI3MiIsInNjb3BlIjoib3BlbmlkIGVtYWlsIHByb2ZpbGUiLCJzaWQiOiI1YmQ1MTI2Zi1hMmQ3LTQ0MzAtYmE0Ni04Yjk2NTc2YjFiNzIifQ.j98Gd7nXGFL6qIpohFWXzp5pQmDVE7aS4q0XzLjQK3w","token_type":"Bearer","id_token":"eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICItc1ZXMmpmUmVFUWZua3k2YmRRN1k2WjByQ0pqN0JQOGY5Y3JtNDdmMGxNIn0.eyJleHAiOjE3MDEzMDIyNjQsImlhdCI6MTcwMTMwMTk2NCwiYXV0aF90aW1lIjowLCJqdGkiOiIzZGZlY2M4Ny01ZjFlLTQ4NDUtOTIzNy01ZWIyNDhmNzE5M2QiLCJpc3MiOiJodHRwOi8vbG9jYWxob3N0OjgwODAvcmVhbG1zL215c3ByaW5nYm9vdGFwcHJlYWxtIiwiYXVkIjoibXlzcHJpbmdib290YXBwIiwic3ViIjoiZGVlOWVmODAtYWU2OS00ZGUzLWExN2MtMjMyNGY4NzRkOWUyIiwidHlwIjoiSUQiLCJhenAiOiJteXNwcmluZ2Jvb3RhcHAiLCJzZXNzaW9uX3N0YXRlIjoiNWJkNTEyNmYtYTJkNy00NDMwLWJhNDYtOGI5NjU3NmIxYjcyIiwiYXRfaGFzaCI6Il9jRHVLZVd0TllLWnp5S1dkNXV4TFEiLCJhY3IiOiIxIiwic2lkIjoiNWJkNTEyNmYtYTJkNy00NDMwLWJhNDYtOGI5NjU3NmIxYjcyIiwiZW1haWxfdmVyaWZpZWQiOmZhbHNlLCJuYW1lIjoiT2xla3NpaSBUa2FjaGVua28iLCJwcmVmZXJyZWRfdXNlcm5hbWUiOiJteXVzZXIyIiwiZ2l2ZW5fbmFtZSI6Ik9sZWtzaWkiLCJmYW1pbHlfbmFtZSI6IlRrYWNoZW5rbyJ9.C1yXjQkV4mguywkjObgCvepjbX6v9wW5u7fxeah3KR_ciwdJcoSjsnrjDMMZd9oPaeTf8cNZRewv5aOnQMawKOVrCDmKA4rhXYQbOTNdsPwIErp0oyaxoZYEUCmxwztCoZN3ehoTmLJY2y0P9MEmrdaMT-Ug2cAbJI7yHfqK7nIweEwtwe39MQ6ZMdxLw9St6mC_1bJMF_CQu0ds_7bIoWehErW1dhPN59Vd3-OcKNotTiEHgSGd0hT6Mgq5Ey2-VYGShP_2r-M8DJfKS2W5eris3uGlZJjBmfQx8tBn268wx20oUn8DbZUEJ2iI0kg1DmDdUwV1i2EiOdfzgH4thg","not-before-policy":0,"session_state":"5bd5126f-a2d7-4430-ba46-8b96576b1b72","scope":"openid email profile"}
```

```
export TOKEN=$(curl --location 'http://localhost:8080/realms/myspringbootapprealm/protocol/openid-connect/token' --header 'Content-Type: application/x-www-form-urlencoded' --data-urlencode 'username=myuser' --data-urlencode 'password=3677417' --data-urlencode 'grant_type=password' --data-urlencode 'client_id=myspringbootapp' --data-urlencode 'client_secret=ih7SbP9PLYErKiisHgLstMV2Ztrji0gC' --data-urlencode 'scope=openid'| jq -r '.access_token')
```

##### To get TOKEN to send as the parameter of the auth
```
export TOKEN=$(curl --location 'http://localhost:8080/realms/myspringbootapprealm/protocol/openid-connect/token' --header 'Content-Type: application/x-www-form-urlencoded' --data-urlencode 'username=myuser' --data-urlencode 'password=3677417' --data-urlencode 'grant_type=password' --data-urlencode 'client_id=myspringbootapp' --data-urlencode 'client_secret=ih7SbP9PLYErKiisHgLstMV2Ztrji0gC' --data-urlencode 'scope=openid'| jq -r '.access_token')
```

---

## For `springbootpersonalrealm`

### kate-admin
```
curl --location 'http://localhost:8080/realms/springbootpersonalrealm/protocol/openid-connect/token' --header 'Content-Type: application/x-www-form-urlencoded' --data-urlencode 'username=kate-admin' --data-urlencode 'password=3677417' --data-urlencode 'grant_type=password' --data-urlencode 'client_id=springbootpersonal' --data-urlencode 'client_secret=NyC1XGjYSWfJ7sGgqqTkGxYmxRZ1fAmR' --data-urlencode 'scope=openid'
```

### oleksii-user
```
curl --location 'http://localhost:8080/realms/springbootpersonalrealm/protocol/openid-connect/token' --header 'Content-Type: application/x-www-form-urlencoded' --data-urlencode 'username=oleksii-user' --data-urlencode 'password=3677417' --data-urlencode 'grant_type=password' --data-urlencode 'client_id=springbootpersonal' --data-urlencode 'client_secret=NyC1XGjYSWfJ7sGgqqTkGxYmxRZ1fAmR' --data-urlencode 'scope=openid'
```

USER
export TOKEN=$(curl --location 'http://localhost:8080/realms/springbootpersonalrealm/protocol/openid-connect/token' --header 'Content-Type: application/x-www-form-urlencoded' --data-urlencode 'username=oleksii-user' --data-urlencode 'password=3677417' --data-urlencode 'grant_type=password' --data-urlencode 'client_id=springbootpersonal' --data-urlencode 'client_secret=NyC1XGjYSWfJ7sGgqqTkGxYmxRZ1fAmR' --data-urlencode 'scope=openid'| jq -r '.access_token')

kate@Stitch:~$ curl -X GET   http://localhost:8081/students   -H "Authorization: Bearer $TOKEN"
[{"id":1,"name":"Oleksii","group":"345","rdvs":[]}]kate@Stitch:~$ curl -X GET   http://localhost:8081/professors   -H "Authorization: Bearer $TOKEN"
[{"id":2,"name":"Olivier","department":"ISTIC","rdvs":[]}]kate@Stitch:~$ curl -X GET   http://localhost:8081/rdvs   -H "Authorization: Bearer $TOKEN"
kate@Stitch:~$ 

ADMIN
kate@Stitch:~$ export TOKEN=$(curl --location 'http://localhost:8080/realms/springbootpersonalrealm/protocol/openid-connect/token' --header 'Content-Type: application/x-www-form-urlencoded' --data-urlencode 'username=kate-admin' --data-urlencode 'password=3677417' --data-urlencode 'grant_type=password' --data-urlencode 'client_id=springbootpersonal' --data-urlencode 'client_secret=NyC1XGjYSWfJ7sGgqqTkGxYmxRZ1fAmR' --data-urlencode 'scope=openid'| jq -r '.access_token')
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  3595  100  3450  100   145  92572   3890 --:--:-- --:--:-- --:--:-- 97162
kate@Stitch:~$ curl -X GET   http://localhost:8081/rdvs   -H "Authorization: Bearer $TOKEN"
[{"id":1,"titlecurl -X GET   http://localhost:8081/professors   -H "Authorization: Bearer $TOKEN"
kate@Stitch:~$ curl -X GET   http://localhost:8081/students   -H "Authorization: Bearer $TOKEN"
kate@Stitch:~$ 




