## MAX, MIN, COUNT, SUM
 

### 가장 최근에 들어온 동물은 언제 들어왔는지 조회하는 SQL 문을 작성해주세요.
```sql
SELECT MAX(DATETIME) FROM ANIMAL_INS
```

### 동물 보호소에 가장 먼저 들어온 동물은 언제 들어왔는지 조회하는 SQL 문을 작성해주세요
```sql
SELECT MIN(DATETIME) FROM ANIMAL_INS
```

### 동물 보호소에 동물이 몇 마리 들어왔는지 조회하는 SQL 문을 작성해주세요.
```sql
SELECT COUNT(ANIMAL_ID) count
FROM ANIMAL_INS;
```

### 동물 보호소에 들어온 동물의 이름은 몇 개인지 조회하는 SQL 문을 작성해주세요. 이때 이름이 NULL인 경우는 집계하지 않으며 중복되는 이름은 하나로 칩니다.
```sql
SELECT COUNT(A.NAME) count
FROM (SELECT NAME FROM ANIMAL_INS GROUP BY NAME) AS A
WHERE NAME IS NOT NULL;
```

 
