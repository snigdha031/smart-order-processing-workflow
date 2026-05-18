# API Testing

## Test Endpoint

POST /webhook-test/new-order

## Successful Request

```json
{
  "order_id": "ORD-1001",
  "customer_name": "John Doe",
  "email": "john@example.com",
  "total_amount": 120
}
```

## Validation Failure Example

```json
{
  "order_id": "ORD-1002",
  "customer_name": "John Doe",
  "total_amount": 120
}
```

Response:

```json
{
  "success": false,
  "error": "Email is required"
}
```

## Duplicate Order Example

```json
{
  "success": false,
  "error": "Duplicate order ID"
}
```