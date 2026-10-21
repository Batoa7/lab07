# BUG-04: Invalid JSON returns HTTP 200 instead of 400

**Төрөл:** API / Input validation  
**Severity:** Medium

## Алдааг давтах алхмууд
1. Аппыг ажиллуулж `http://localhost:3000` руу орно.
2. Terminal нээнэ.
3. Дараах командыг ажиллуулна:

```bash
curl -i -X POST http://localhost:3000/api/books -H 'Content-Type: application/json' -d 'not-json'
```

## Хүлээгдэж буй үр дүн
API нь буруу JSON оролтод `HTTP 400 Bad Request` буцаана.

## Бодит үр дүн
API нь `HTTP 200 OK` болон `{"result":"OK"}` буцаасан.

## Нотолгоо
`evidence/api-invalid-json.txt`

## Төлөв
Reproducible — дахин шалгаж баталгаажуулах шаардлагатай.
