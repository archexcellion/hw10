# HW10

# task1
## create schema
RAW JSON:
 {"currency":"USD","customer":{"email":"sarah.johnson@example.com","name":"Sarah Johnson"},"items":[{"name":"Water Bottle","price":12.5,"qty":2,"sku":"WB001"},{"name":"Carrying Pouch","price":5,"qty":1,"sku":"CP001"}],"order_id":"A-1029","total":30}

Parsed:
 {
  "currency": "USD",
  "customer": {
    "email": "sarah.johnson@example.com",
    "name": "Sarah Johnson"
  },
  "items": [
    {
      "name": "Water Bottle",
      "price": 12.5,
      "qty": 2,
      "sku": "WB001"
    },
    {
      "name": "Carrying Pouch",
      "price": 5,
      "qty": 1,
      "sku": "CP001"
    }
  ],
  "order_id": "A-1029",
  "total": 30
}

# task3
## create converter & print RESULT JSON
=== INTERMEDIATE (turn 1) ===
name: convert
arguments: {"amount":100,"base":"USD","quote":"THB"}
RESULT JSON: {"amount": 100, "base": "USD", "quote": "THB", "rate": 35.0, "converted": 3500}
FINAL: The converted amount is 3500 THB.
=== INTERMEDIATE (turn 1) ===
name: convert
arguments: {"amount":250,"base":"THB","quote":"EUR"}
RESULT JSON: {"amount": 250, "base": "THB", "quote": "EUR", "rate": 0.025, "converted": 6.25}
=== INTERMEDIATE (turn 2) ===
name: resolve_currency
arguments: {"name_or_code":"baht"}
RESULT JSON: "THB"
FINAL: The conversion of 250 baht to euros is 6.25 euros.
