This is just for testing - will never get in production without changing auth.
#### SHOW RECORDS:
```bash
curl --request GET \
  --url http://localhost:8080/customers \
  --header 'authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImtpZCI6Ik5EYzNRVE15TlRJNE5rVXhNRU01UXpBelEwWTRPRVpGTUVSQk1ERkRORGxCUkVKR1FUWkVNUSJ9.eyJpc3MiOiJodHRwczovL2Rldi01bnJhaHZlYi5ldS5hdXRoMC5jb20vIiwic3ViIjoiSjl4RGNpckZBWk9TbDl3R3hrbHhuWnV3SDBqZTg2c3RAY2xpZW50cyIsImF1ZCI6ImtvdGxpbi1qd3RzIiwiaWF0IjoxNTcwNTUwNzQxLCJleHAiOjE1NzA2MzcxNDEsImF6cCI6Iko5eERjaXJGQVpPU2w5d0d4a2x4blp1d0gwamU4NnN0IiwiZ3R5IjoiY2xpZW50LWNyZWRlbnRpYWxzIn0.coNHFD8mM1L1R3tSV36mArwN6NYlu7-cdR-hojpwt86HIgPZ8HahkEVc7eH8j9LmgjSqPwtU8heQ3Rb1dnCfeEyrTlp7LU3cBMwlAef3WjduJgRj1_3YQDlXonQop8B1w06ZELRbgJBSTtl0KTD7N_46u1X3vX78FyEihnVUokYrBND8MEKldD6K6X9qaAfxhzuKgd2XWEUIQp34KF-383m960pISK5CjTm2zqdzB5-v1ISIFZ3hTqdjJzg0ZLOt2V86-yH-pBNaaEhOkk0MGcZ_4lNGsNumBHdoKAYNt_unVcBjaLl6xa6nYOD_MLRZtMHQ4lp9yqFISkLCmpj90g'
```


#### ADD RECORD:
```bash
curl --request POST \
-H "Content-Type: application/json" \
-d '{
    "firstName": "Bruno",
    "lastName": "Krebs"
}' \
  --url http://localhost:8080/customers \
  --header 'authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImtpZCI6Ik5EYzNRVE15TlRJNE5rVXhNRU01UXpBelEwWTRPRVpGTUVSQk1ERkRORGxCUkVKR1FUWkVNUSJ9.eyJpc3MiOiJodHRwczovL2Rldi01bnJhaHZlYi5ldS5hdXRoMC5jb20vIiwic3ViIjoiSjl4RGNpckZBWk9TbDl3R3hrbHhuWnV3SDBqZTg2c3RAY2xpZW50cyIsImF1ZCI6ImtvdGxpbi1qd3RzIiwiaWF0IjoxNTcwNTUwNzQxLCJleHAiOjE1NzA2MzcxNDEsImF6cCI6Iko5eERjaXJGQVpPU2w5d0d4a2x4blp1d0gwamU4NnN0IiwiZ3R5IjoiY2xpZW50LWNyZWRlbnRpYWxzIn0.coNHFD8mM1L1R3tSV36mArwN6NYlu7-cdR-hojpwt86HIgPZ8HahkEVc7eH8j9LmgjSqPwtU8heQ3Rb1dnCfeEyrTlp7LU3cBMwlAef3WjduJgRj1_3YQDlXonQop8B1w06ZELRbgJBSTtl0KTD7N_46u1X3vX78FyEihnVUokYrBND8MEKldD6K6X9qaAfxhzuKgd2XWEUIQp34KF-383m960pISK5CjTm2zqdzB5-v1ISIFZ3hTqdjJzg0ZLOt2V86-yH-pBNaaEhOkk0MGcZ_4lNGsNumBHdoKAYNt_unVcBjaLl6xa6nYOD_MLRZtMHQ4lp9yqFISkLCmpj90g'
```


#### Old without auth::

```bash
curl http://localhost:8080/
```

```bash
curl -H "Content-Type: application/json" -X POST -d '{
    "firstName": "Bruno",
    "lastName": "Krebs"
}'  http://localhost:8080/
```


```bash
curl -X DELETE http://localhost:8080/1
```

```bash
curl -H "Content-Type: application/json" -X PUT -d '{
    "id": 6,
    "firstName": "Bruno",
    "lastName": "Simões Krebs"
}'  http://localhost:8080/6
```
