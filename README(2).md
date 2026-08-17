# Projekt: Testování REST API

Ruční testování Student CRUD API pomocí Postmanu a kontrola dat v PostgreSQL databázi přes DBeaver.

## Obsah repozitáře
- `Testovani_REST_API_projekt.pdf` - finální projektová dokumentace
- `Testovani_REST_API.postman_collection.json` - sanitizovaná Postman collection bez tokenu a přihlašovacích údajů
- `README.md` - stručný popis projektu

## Rozsah testování
- autorizace přes `POST /login`
- `POST /students`
- `GET /students/{student_id}`
- `PUT /students/{student_id}`
- `DELETE /students/{student_id}`
- SQL kontroly pouze pomocí `SELECT`
- negativní testy autorizace a duplicitního e-mailu

## Hlavní nálezy
- **BUG-01:** při PUT se hodnota `isEuCitizen=true` neuložila správně a následně byla vrácena jako `false`
- **BUG-02:** DELETE vrátil úspěšnou odpověď, ale student zůstal dostupný přes GET i v databázi

Přihlašovací údaje ani Bearer token nejsou v odevzdávaných souborech zveřejněny.
