# MockFast.io - Mock as a Service

[![Website](https://img.shields.io/badge/Visit-MockFast.io-blue)](https://mockfast.io)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<p align="center">
  <img src="./mockfast-og.png" alt="MockFast Logo" width="200"/>
</p>

## 🚀 What is MockFast?

MockFast is a "Mock as a Service" platform that lets developers create and deploy custom mock APIs in seconds without writing any backend code. Perfect for frontend development, testing, and API prototyping.

**With MockFast, you can:**
- Create realistic API endpoints by simply defining your data structure
- Access a rich library of data types from basic to specialized (names, addresses, analytics, etc.)
- Deploy instantly to a reliable, production-ready environment
- Generate complex, nested data structures with array multipliers

## 📚 Documentation

This repository contains the official documentation for MockFast.io. 

## 🔍 Quick Start

### 1. Define Your Template

```json
{
  "name": "string.name.firstname",
  "age": "number",
  "email": "string.mail.gmail"
}
```

### 2. Get Your API Endpoint

```
https://mockfast.io/api/YOUR_ID
```

### 3. Use Your API

```javascript
fetch('https://mockfast.io/api/YOUR_ID')
  .then(response => response.json())
  .then(data => console.log(data));
```

### 4. Get your data

```json
 {
    "name": "Sophie",
    "age": "545",
    "email": "user_160@gmail.com",
}
```

## 📋 Available Data Types

MockFast supports a wide range of data types:

### Basic Types
- `string` - Random text strings
- `number` - Random numbers
- `boolean` - True/false values
- `email` - Valid email addresses
- `uuid` - Unique identifiers
- `date` - Date strings
- `lorem` - Lorem ipsum text

### Advanced Types
- **Name types** - Generate realistic names (fullname, firstname, lastname)
- **Address types** - Generate address components or full addresses
- **Mail types** - Email addresses from various providers
- **Money types** - Currencies, symbols, and prices
- **Review types** - Rating numbers and review text
- **Country types** - Country information and metadata
- **Event types** - Event details including venues and dates
- **Color types** - Color codes in various formats
- **File types** - File metadata and path information
- **Weather types** - Weather conditions and location data
- **Analytics types** - Website analytics and metrics

## 💡 Advanced Features

### Array Multipliers

Generate multiple items dynamically with the special `__multiply` property:

```json
{
  "categories": [
    {
      "__multiply": "2-5",
      "name": "string",
      "id": "uuid"
    }
  ]
}
```

This generates between 2-5 category objects, each with random data.

### Complex Nested Structures

Create realistic API responses with nested objects and arrays:

```json
{
  "user": {
    "name": "string.name.fullname",
    "email": "email",
    "orders": [
      {
        "__multiply": "3-8",
        "orderId": "uuid",
        "total": "number.money.price",
        "items": [
          {
            "__multiply": "1-4",
            "productId": "uuid",
            "name": "string",
            "price": "number.money.price"
          }
        ]
      }
    ]
  }
}
```

## 🔄 Sorting Data

Sort your API responses easily with query parameters:

| Feature | Query Parameter | Example | Description |
|---------|----------------|---------|-------------|
| Basic Sorting | `?sort=fieldname` | `?sort=age` | Sort by a single field (ascending by default) |
| Explicit Direction | `?sort=fieldname:direction` | `?sort=age:desc` | Sort by a field with explicit direction (`asc` or `desc`) |
| Multi-Field Sorting | `?sort=field1&sort=field2` | `?sort=age&sort=name` | Sort by multiple fields (applied in order) |
| Mixed Direction | `?sort=field1:asc&sort=field2:desc` | `?sort=age:asc&sort=name:desc` | Sort by different fields with different directions |
| Default Direction | `?sort=field&order=direction` | `?sort=age&order=desc` | Set a default direction for fields without explicit direction |

### Example

For data like:
```json
[
  {
    "name": "Bob",
    "age": 25,
    "email": "bob@example.com"
  },
  {
    "name": "Charlie",
    "age": 30,
    "email": "charlie@example.com"
  },
  {
    "name": "Alice",
    "age": 30,
    "email": "alice@example.com"
  }

]
```

Using `?sort=age:asc&sort=name:desc` would return:
1. Bob (age 25) - lowest age first
2. Charlie (age 30) - then by name in descending order for same ages
3. Alice (age 30) - then by name in descending order for same ages

## 💼 Plans and Features

### Free Plan
- Create basic mock APIs with standard types
- Access public endpoints
- Use basic data types (string, number, etc.)

### Registered Account
- Advanced types (name, address, etc.)
- Private endpoints with authentication
- Custom delays and HTTP codes
- Usage tracking

## 🤝 Contributing

We welcome contributions to improve MockFast documentation! Please see our [Contributing Guide](./CONTRIBUTING.md) for more information.

## 📞 Support

Need help? Reach out to us:

- [Discord](https://discord.gg/JCFJ9MBcTr)
- [Visit MockFast.io](https://mockfast.io)
- [Buy Me a Coffee](https://ko-fi.com/mockfast)

## ⭐ Show Your Support

If MockFast has been helpful to you, please consider:
- Giving this repo a star ⭐
- Sharing feedback on our website
- Supporting the project by buying us a coffee

## 📜 License

This documentation is licensed under [MIT License](./LICENSE).

---

<p align="center">
  <a href="https://mockfast.io">MockFast.io</a> • 
  <a href="https://mockfast.io/documentation">Documentation</a> • 
  <a href="https://mockfast.io/roadmap">Roadmap</a>
</p>
