# SQL-project 👩‍💻
## This project explores cinema halls in Saudi Arabia using MySQL

- Retrieves all columns and rows
  ```
  SELECT * FROM saudi_arabia.ksa;
  ```
  ![image](https://github.com/user-attachments/assets/c76fded0-c15e-4a16-b054-d218420b8a51)
  

# ✨Qustions
## Q1- Count the total number of cinemas
```sql
SELECT COUNT(*) AS total_cinemas
FROM saudi_arabia.ksa;
```
<img src="https://github.com/user-attachments/assets/30f0bbe0-de69-437c-b1ce-7353a926bec4" alt="Value Counts Output" width="600"/>


## Q2- List all unique cinema locations
```sql
SELECT DISTINCT location
FROM saudi_arabia.ksa;
```
![image](https://github.com/user-attachments/assets/1fa76f2e-516e-41b8-99f9-710a68301ecc)



## Q3-  Find cinemas with a rating of 5
```sql
SELECT name, rating
FROM saudi_arabia.ksa
WHERE rating = 5;
```
![image](https://github.com/user-attachments/assets/10582623-d6f7-47b6-b595-9f1d6da959ab)

## Q4- Find cinemas with more than 50,000 reviews
```sql
SELECT name, review_count
FROM saudi_arabia.ksa
WHERE review_count > 50000;
```
![image](https://github.com/user-attachments/assets/46e6e240-bf74-494e-992b-aed7ed99fb5c)

## Q5-  Find cinemas with names starting with 'A' 
```sql
SELECT name
FROM saudi_arabia.ksa
WHERE name LIKE 'A%';
```
![image](https://github.com/user-attachments/assets/145c2a17-2971-4ad2-92e6-ad21ea7dbc65)


## Q6-  Calculate the average rating per location
```sql
SELECT location, AVG(rating) AS avg_rating 
FROM saudi_arabia.ksa 
GROUP BY location 
ORDER BY avg_rating DESC;
```
![image](https://github.com/user-attachments/assets/e151572b-691d-4d31-93bb-927e4772f0b4)

## Q7- Find cinemas where the best comment contains "comfortable"
```sql
SELECT name, best_comment 
FROM saudi_arabia.ksa 
WHERE best_comment LIKE '%comfortable%';
```
![image](https://github.com/user-attachments/assets/1fd4bd9d-b081-4929-b8a8-14314e308e0a)

## Q8-  Find the lowest-rated cinemas
```sql
SELECT name, rating 
FROM saudi_arabia.ksa 
ORDER BY rating ASC 
LIMIT 5;
```
![image](https://github.com/user-attachments/assets/fb2f4de1-6948-4c9c-bd04-6f6e4adc18eb)

## Q9-  Find the most common genre
```sql
SELECT genre, COUNT(*) AS genre_count 
FROM saudi_arabia.ksa 
GROUP BY genre 
ORDER BY genre_count DESC 
LIMIT 1;
```
![image](https://github.com/user-attachments/assets/aceef2ce-c0ea-4125-81a3-a6a4211df0f8)

## Q10- Find cinemas with reviews between 10,000 and 50,000
```sql
SELECT name, review_count 
FROM saudi_arabia.ksa 
WHERE review_count BETWEEN 10000 AND 50000;
```

![image](https://github.com/user-attachments/assets/d04e5dd6-c7e9-43a1-a782-378c32d71b49)





